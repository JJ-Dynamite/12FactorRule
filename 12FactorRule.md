The `Twelve-Factor` App methodology can be applied to apps written in any programming language, including React Native. Here's how you can apply the Twelve-Factor principles to a React Native application:

1. **Codebase**: Maintain a single codebase for your app, tracked in version control. Different versions and environments should be managed through branche.

2. **Dependencies**: Declare all dependencies explicitly in a package.json file. Use npm or yarn to manage them.

3. **Config**: Store config in the environment. You can use libraries like `react-native-config` to manage environment variables.

4. **Backing Services**: Treat all backing services as attached resources. This includes your databases, messaging/queueing systems, and caching systems.

5. **Build, Release, Run**: Strictly separate the stages of building your app, releasing it, and running it. Tools like Fastlane can help automate this process.

6. **Processes**: Execute your app as one or more stateless processes. Ensure that any data that needs to persist is stored in a stateful backing service, like a database.

7. **Port Binding**: While this factor is more relevant to backend services, you can interpret it for React Native as using explicit contracts for APIs and services your app depends on.

8. **Concurrency**: Scale out your app via the process model. In the context of React Native, this could mean scaling your backend services based on demand.

9. **Disposability**: Maximize robustness with fast startup and graceful shutdown. Ensure that your app can handle unexpected terminations gracefully.

10. **Dev/Prod Parity**: Keep development, staging, and production environments as similar as possible. This can be achieved through the use of environment configuration and containerization.

11. **Logs**: Treat logs as event streams. Tools like `react-native-logs` can be used for logging in React Native apps.

12. **Admin Processes**: Run admin/management tasks as one-off processes. These could be data migration scripts or administrative tasks.

Source:
- The Twelve-Factor App. https://12factor.net/.
