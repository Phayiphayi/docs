---
title: 配置速率限制
intro: '您可以使用 {% data variables.enterprise.management_console %} 为 {% data variables.product.prodname_ghe_server %} 配置速率限制。'
redirect_from:
  - /enterprise/admin/installation/configuring-rate-limits
versions:
  enterprise-server: '*'
---

### 为 {% data variables.product.prodname_enterprise_api %} 启用速率限制

在 {% data variables.product.prodname_enterprise_api %} 上启用速率限制可以防止个别用户或未通过身份验证的用户过度使用资源。 For more information, see "[Rate Limiting](/enterprise/{{ currentVersion }}/v3/#rate-limiting)."

{% note %}

**注**：{% data variables.enterprise.management_console %} 列出了每种速率限制的时限（按分钟或按小时）。

{% endnote %}

{% data reusables.enterprise_site_admin_settings.access-settings %}
{% data reusables.enterprise_site_admin_settings.management-console %}
2. 在“Rate Limiting”下，选择 **Enable API Rate Limiting**。 ![用于启用 API 速率限制的复选框](/assets/images/enterprise/management-console/api-rate-limits-checkbox.png)
3. 输入对每个 API 的已验证和未验证请求的限制，或者接受预先填入的默认限制。
{% data reusables.enterprise_management_console.save-settings %}

### 启用滥用率限制

设置滥用率限制可保护 {% data variables.product.product_location_enterprise %} 上的整体服务等级。

{% data reusables.enterprise_site_admin_settings.access-settings %}
{% data reusables.enterprise_site_admin_settings.management-console %}
2. 在“Rate Limiting”下，选择 **Enable Abuse Rate Limiting**。 ![用于启用滥用率限制的复选框](/assets/images/enterprise/management-console/abuse-rate-limits-checkbox.png)
3. 输入总请求限制、CPU 限制或对搜索的 CPU 限制，或接受预先填入的默认限制。
{% data reusables.enterprise_management_console.save-settings %}

### 启用 Git 速率限制

您可以按仓库网络或用户 ID 应用 Git 速率限制。 Git 速率限制以每分钟并行操作数表示，不过会根据当前 CPU 负荷进行调整。

{% data reusables.enterprise_site_admin_settings.access-settings %}
{% data reusables.enterprise_site_admin_settings.management-console %}
2. 在“Rate Limiting”下，选择 **Enable Git Rate Limiting**。 ![用于启用 Git 速率限制的复选框](/assets/images/enterprise/management-console/git-rate-limits-checkbox.png)
3. 输入对每个仓库网络或用户 ID 的限制。 ![仓库网络和用户 ID 限制的字段](/assets/images/enterprise/management-console/example-git-rate-limits.png)
{% data reusables.enterprise_management_console.save-settings %}
