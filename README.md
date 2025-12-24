# SPE Team Web Assets

This repository serves as a centralized host for web assets and custom styling used by the **SPE Team**. It provides a global codebase for maintaining visual consistency across various internal and external web projects, ensuring that updates to branding and layout can be deployed efficiently across the team's entire digital portfolio.

---

## 🚀 Implementation

To use these assets, link to them via the jsDelivr CDN. This ensures high-speed delivery and 100% uptime across all projects.

### WordPress Integration
Add this snippet to your `functions.php` file to sync your login page with the global SPE styles:

```php
/**
 * Enqueue SPE Team Global Login Assets
 */
add_action('login_enqueue_scripts', function() {
    // Replace [username] and [repo] with your actual GitHub details
    $url = '[https://cdn.jsdelivr.net/gh/](https://cdn.jsdelivr.net/gh/)[username]/[repo]/global-login.css';
    
    wp_enqueue_style('spe-global-styles', $url, array(), '1.0.0');
});
