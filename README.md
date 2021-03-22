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
</div>
