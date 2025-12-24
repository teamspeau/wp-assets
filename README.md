SPE Team Web Assets
This repository serves as a centralized host for web assets and custom styling used by the SPE team. It provides a global codebase for maintaining visual consistency across various internal and external web projects.

Usage
The assets in this repository are served via CDN for use across multiple platforms. To include the global login styles in a WordPress project, add the following snippet to your functions.php or a site-specific plugin:

PHP

/**
 * Load Global Login CSS from CDN
 */
add_action('login_enqueue_scripts', function() {
    $cdn_url = 'https://cdn.jsdelivr.net/gh/[YOUR_GITHUB_USERNAME]/[REPO_NAME]/global-login.css';
    wp_enqueue_style('spe-global-login', $cdn_url, array(), '1.0.0');
});
Maintenance
By utilizing this central repository, the SPE team can:

Deploy Instantly: Updates made to the master branch are reflected across all connected sites.

Maintain Consistency: Ensure branding, layouts, and UI elements remain uniform.

Streamline Workflow: Reduce redundant code by managing styles from a single source of truth.

Maintained by the SPE Team.
