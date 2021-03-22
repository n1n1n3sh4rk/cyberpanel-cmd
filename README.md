<div class="entry-content" itemprop="text"><p>A quicklist guide of useful server commands for CyberPanel web server control panel.<span id="more-3380"></span></p>
<p><strong>Installation (on CentOS):</strong></p>
<ul>
<li><code>yum update</code>, <code>y</code> and [ENTER] key when prompted.</li>
<li>Change LS console pass with <code class="c-mrkdwn__code" data-stringify-type="code">cd /usr/local/lsws/admin/misc</code>&nbsp;and&nbsp;<code class="c-mrkdwn__code" data-stringify-type="code">./admpass.sh</code>, and follow prompt.</li>
<li>Can follow my <a href="https://wpjohnny.com/cyberpanel-openlitespeed-high-performance-web-server-for-wordpress/">CyberPanel install guide</a> if needed.</li>
</ul>
<p>Need to upgrade CyberPanel? Follow the <a href="https://cyberpanel.net/docs/upgrading-cyberpanel/">latest instructions</a>.</p>
<p><strong>Recommended configurations after installation:</strong></p>
<ul>
<li>Go to CP security/firewall page, and open port 7080 for LS console.</li>
<li>Get&nbsp;mysql root password with&nbsp;<code class="c-mrkdwn__code" data-stringify-type="code">cat /etc/cyberpanel/mysqlPassword</code> (required for logging into phpMyAdmin later).</li>
<li>Increase php.ini limits for PHP 7.0 (from CP &gt; PHP &gt; edit PHP configs).</li>
<li>Change LS console pass with <code class="c-mrkdwn__code" data-stringify-type="code">cd /usr/local/lsws/admin/misc</code>&nbsp;and&nbsp;<code class="c-mrkdwn__code" data-stringify-type="code">./admpass.sh</code></li>
<li>Log into LS console and enable brotli, WP security throttle (if you have LS ent).</li>
<li>Tweak your PHP and security settings as needed.</li>
<li>Change SSH port setting from CP &gt; Security &gt; Secure SSH.</li>
</ul>
<p><strong>CyberPanel file/config locations:</strong></p>
<ul>
<li>Changing server IP – <code>/etc/cyberpanel/machineIP</code></li>
<li>Changing MySQL root password – <code>/etc/cyberpanel/machineIP</code></li>
<li>SSL certifications – <code>/etc/letsencrypt/live</code>, then go into domain you want</li>
<li>Restore location (when importing backups) – <code>/home/backup</code></li>
</ul>
<p><strong>CyberPanel commands:</strong></p>
<ul>
<li>Restart MariaDB –</li>
<li></li>
</ul>
<p><strong>Logs:</strong></p>
<ul>
<li>Error logs –&nbsp;<code>cat /home/cyberpanel/error-logs.txt</code>&nbsp;(<a href="https://cyberpanel.net/docs/log-files-on-cyberpanel/">log files on CyberPanel</a>)</li>
<li>Backup logs – <code>cd /usr/local/lscp/logs</code></li>
<li>Cron schedules –&nbsp;<code>/etc/crontab</code>&nbsp;clear out unnecessary cronjobs eating up server resources (backups)</li>
<li>https://&lt;IP Address&gt;:8090/serverstatus/cyberCPMainLogFile</li>
</ul>
<p><strong>Backups:</strong></p>
<ul>
<li>Manually running scheduled backups – <code>python /usr/local/CyberCP/plogical/backupScheduleLocal.py</code>, read <a href="https://forums.cyberpanel.net/discussion/557/backup-website-doesnt-appear-to-be-working">this</a> for more info</li>
<li><a href="https://www.teksupport.in/script-to-upload-cyberpanel-backups-to-google-drive/">Cool script</a> to upload CP backups to Google Drive</li>
</ul>
<div class="scriptlesssocialsharing"><h3 class="scriptlesssocialsharing__heading">Share this post:</h3><div class="scriptlesssocialsharing-buttons no-icons"><a class="button facebook" target="_blank" href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fwpjohnny.com%2Fcyberpanel-server-commands-and-important-directories%2F" rel="noopener noreferrer nofollow"><span class="sss-name"><span class="screen-reader-text">Share on </span>Facebook</span></a><a class="button twitter" target="_blank" href="https://twitter.com/intent/tweet?text=CyberPanel%20server%20commands%20and%20important%20directories&amp;url=https%3A%2F%2Fwpjohnny.com%2Fcyberpanel-server-commands-and-important-directories%2F&amp;via=wpjohnnycom&amp;related=wpjohnnycom" rel="noopener noreferrer nofollow"><span class="sss-name"><span class="screen-reader-text">Share on </span>Twitter</span></a><a class="button linkedin" target="_blank" href="https://www.linkedin.com/shareArticle?mini=1&amp;url=https%3A%2F%2Fwpjohnny.com%2Fcyberpanel-server-commands-and-important-directories%2F&amp;title=CyberPanel%20server%20commands%20and%20important%20directories&amp;source=https%3A%2F%2Fwpjohnny.com" rel="noopener noreferrer nofollow"><span class="sss-name"><span class="screen-reader-text">Share on </span>LinkedIn</span></a><a class="button whatsapp" target="_blank" href="https://api.whatsapp.com/send?text=CyberPanel%20server%20commands%20and%20important%20directories%20%E2%80%94%20https%3A%2F%2Fwpjohnny.com%2Fcyberpanel-server-commands-and-important-directories%2F" rel="noopener noreferrer nofollow"><span class="sss-name"><span class="screen-reader-text">Share on </span>WhatsApp</span></a><a class="button email" href="mailto:?body=I%20read%20this%20helpful%20WordPress%20post%20and%20wanted%20to%20share%20it%20with%20you.%20Here%27s%20the%20link%3A%20https%3A%2F%2Fwpjohnny.com%2Fcyberpanel-server-commands-and-important-directories%2F&amp;subject=Shared%20post%20from%20WPjohnny.com%3A%20CyberPanel%20server%20commands%20and%20important%20directories" rel="noopener noreferrer nofollow"><span class="sss-name"><span class="screen-reader-text">Share on </span>Email</span></a><a class="button sms" target="_blank" href="sms:?&amp;body=CyberPanel%20server%20commands%20and%20important%20directories%20https%3A%2F%2Fwpjohnny.com%2Fcyberpanel-server-commands-and-important-directories%2F" rel="noopener noreferrer nofollow"><span class="sss-name"><span class="screen-reader-text">Share on </span>SMS</span></a></div></div><!--<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
			xmlns:dc="http://purl.org/dc/elements/1.1/"
			xmlns:trackback="http://madskills.com/public/xml/rss/module/trackback/">
		<rdf:Description rdf:about="https://wpjohnny.com/cyberpanel-server-commands-and-important-directories/"
    dc:identifier="https://wpjohnny.com/cyberpanel-server-commands-and-important-directories/"
    dc:title="CyberPanel server commands and important directories"
    trackback:ping="https://wpjohnny.com/cyberpanel-server-commands-and-important-directories/trackback/" />
</rdf:RDF>-->
</div>
