# CAS-OAuth2.0

CAS 集成 OAuth2.0


auth用户返回默认配置（）
{
  @class: org.jasig.cas.support.oauth.services.OAuthCallbackAuthorizeService
  serviceId: https://sso.castest.com:8443/cas/oauth2.0/callbackAuthorize
  name: OAuth Callback url
  id: 266014601361812
  description: OAuth Wrapper Callback Url
  logoutType: BACK_CHANNEL
  accessStrategy:
  {
    @class: org.jasig.cas.services.DefaultRegisteredServiceAccessStrategy
    enabled: true
    ssoEnabled: true
    requireAllAttributes: true
    caseInsensitive: true
  }
  
}


自定义注册服务：
{
  "@class" : "org.jasig.cas.support.oauth.services.OAuthRegisteredService",
  "clientId": "key",                 
  "clientSecret": "secret",
  "bypassApprovalPrompt": false,
  "serviceId" : "^https://mos.zhizhangyi.com",（返回服务地址）
  "name" : "keyName",
  "id" : 10000005,
  "attributeReleasePolicy" : {
    "@class" : "org.jasig.cas.services.ReturnAllowedAttributeReleasePolicy",
    "allowedAttributes" : [ "java.util.ArrayList", [ "id", "account", "username", "valid", "password" ] ] （表示：返回字段）
  }
}

