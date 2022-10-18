1. get-started 前端项目进入module-federation
2. 安装工具包 "@angular-architects/module-federation": "^12.1.2",
3. 配置angular.json文件，
4. "builder": "ngx-build-plus:browser",
5. "extraWebpackConfig": "apps/dashboard/webpack.config.js",
6. serve
7. "builder": "ngx-build-plus:dev-server",
8. "extraWebpackConfig": "apps/dashboard/webpack.config.js"
9. 生成home library
10.路由的修改 {
    path: 'theme',
    loadChildren: () =>
      loadRemoteModule({
        remoteName: "sampleSolution",
        remoteEntry: 'http://localhost:4700/remoteEntry.js',
        exposedModule: 'ThemeModule',
      }).then((m) => {return m.ThemeModule}),
  },
  {
    path: 'app2-1',
    loadChildren: () =>
      loadRemoteModule({
        remoteName: "sampleSolution",
        remoteEntry: 'http://localhost:4700/remoteEntry.js',
        exposedModule: 'ThemeModule',
      }).then((m) => {return m.ThemeModule}),
  },
  
