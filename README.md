# Angular-SageRoots
Process for AngularJS with SageRoots

Process (WP + Sage):
- Install WP
- Import dummy data
- Install Sage in wp-content/themes/ folder
	- Method 1 from Composer (composer create-project roots/sage your-theme-name)
	- Method 2 from Github (git clone https://github.com/roots/sage.git your-theme-name)
		- Update `resources/assets/config.json` `devUrl` to `http://localhost`
		- Install Composer (composer install)
		- Install Node Modules (npm install)
		- Add html-loader module to Webpack (for Angular template to render)
		- Disable 'eslint' from `resources/assets/build/webpack.config.js` line 45
		- Start Webpack server (npm start);
- Install AngularJS using NPM (npm install angular)
	- https://github.com/JulienMelissas/sage/commit/d15508c8a05c1fbe9d6132478c18eaf9f276f360#diff-2f6122efd8ec361e239562ca4874a9e0R5
- Add Angular APP to Index and 404 page
      <div ng-app="app">
        <siteurl url="'<?php echo site_url(); ?>'"></siteurl>
        <ui-view></ui-view>
      </div>
- Add `site_url` in javascript variable to head
- Add Angular App Folder
- Import angular app in `main.js`
