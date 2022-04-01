nest new Server
nest g module task
# del unnecesary stuff
nest g controller task --no-spec
nest g service task --no-spec

0. DI the service into the controller:
    constructor(private taskService: TaskService){}

0. expose a local array in the service (later to connect to db):
task.service.ts --
export class TaskService {
    private tasks = [];
    getAllTasks(){
        return this.tasks;
    }
}
task.controller.ts --
export class TaskController {
    constructor(private taskService: TaskService){}
        @Get()
        getAllTasks(){
            return this.taskService.getAllTasks()
        }
    }

0. temp interface- later a class : 
task.model.ts --
export interface Task {
    id : string,
    title: string,
    description: string,
    status: TaskStatus
}
enum TaskStatus {
        OPEN = 'OPEN',
        IN_PROGRESS = 'IN_PROGRESS',
        DONE = 'DONE'
}
import into the service --
    private tasks:Task[]  = [];

0. yarn add uuid
