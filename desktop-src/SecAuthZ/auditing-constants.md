---
description: Rappresentano le categorie e le sottocategorie degli eventi dei criteri di controllo.
ms.assetid: e3b12139-947d-4922-91fd-f9833c069011
title: Costanti di controllo (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4134313fe9eab6d487937105535a4417fa9554b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883334"
---
# <a name="auditing-constants"></a>Costanti di controllo

Le costanti seguenti rappresentano le categorie e le sottocategorie degli eventi dei criteri di controllo.

Le costanti seguenti rappresentano le categorie di eventi dei criteri di controllo. Queste costanti sono definite come strutture **GUID** in Ntsecapi. h.

<dl> <dt>

<span id="Audit_System"></span><span id="audit_system"></span><span id="AUDIT_SYSTEM"></span>**Sistema di controllo \_**
</dt> <dd> <dl> <dt>

69979848-797a-11d9-bed3-505054503030
</dt> <dt>



Il controllo tenta di arrestare o riavviare il computer. Inoltre, eventi di controllo che interessano la sicurezza del sistema o il registro di sicurezza.


</dt> </dl> </dd> <dt>

<span id="Audit_Logon"></span><span id="audit_logon"></span><span id="AUDIT_LOGON"></span>**Controlla \_ accesso**
</dt> <dd> <dl> <dt>

69979849-797a-11d9-bed3-505054503030
</dt> <dt>



Il controllo tenta di accedere o disconnettersi dal sistema. Inoltre, il controllo tenta di effettuare una connessione di rete.


</dt> </dl> </dd> <dt>

<span id="Audit_ObjectAccess"></span><span id="audit_objectaccess"></span><span id="AUDIT_OBJECTACCESS"></span>**ObjectAccess di controllo \_**
</dt> <dd> <dl> <dt>

6997984a-797a-11d9-bed3-505054503030
</dt> <dt>



Il controllo tenta di accedere agli oggetti a protezione diretta.


</dt> </dl> </dd> <dt>

<span id="Audit_PrivilegeUse"></span><span id="audit_privilegeuse"></span><span id="AUDIT_PRIVILEGEUSE"></span>**PrivilegeUse di controllo \_**
</dt> <dd> <dl> <dt>

6997984b-797a-11d9-bed3-505054503030
</dt> <dt>



Il controllo tenta di utilizzare i [*privilegi*](/windows/desktop/SecGloss/p-gly).


</dt> </dl> </dd> <dt>

<span id="Audit_DetailedTracking"></span><span id="audit_detailedtracking"></span><span id="AUDIT_DETAILEDTRACKING"></span>**DetailedTracking di controllo \_**
</dt> <dd> <dl> <dt>

6997984c-797a-11d9-bed3-505054503030
</dt> <dt>



Eventi specifici del controllo, ad esempio l'attivazione del programma, alcune forme di duplicazione dell'handle, l'accesso indiretto a un oggetto e l'uscita del processo.


</dt> </dl> </dd> <dt>

<span id="Audit_PolicyChange"></span><span id="audit_policychange"></span><span id="AUDIT_POLICYCHANGE"></span>**PolicyChange di controllo \_**
</dt> <dd> <dl> <dt>

6997984d-797a-11d9-bed3-505054503030
</dt> <dt>



Il controllo tenta di modificare le regole dell'oggetto [**criteri**](/windows/desktop/SecMgmt/the-policy-object-type) .


</dt> </dl> </dd> <dt>

<span id="Audit_AccountManagement"></span><span id="audit_accountmanagement"></span><span id="AUDIT_ACCOUNTMANAGEMENT"></span>**Controllo \_ AccountManagement**
</dt> <dd> <dl> <dt>

6997984e-797a-11d9-bed3-505054503030
</dt> <dt>



Audit tenta di creare, eliminare o modificare gli account utente o di gruppo. Controllare anche le modifiche delle password.


</dt> </dl> </dd> <dt>

<span id="Audit_DirectoryServiceAccess"></span><span id="audit_directoryserviceaccess"></span><span id="AUDIT_DIRECTORYSERVICEACCESS"></span>**DirectoryServiceAccess di controllo \_**
</dt> <dd> <dl> <dt>

6997984f-797a-11d9-bed3-505054503030
</dt> <dt>



Il controllo tenta di accedere al servizio directory.


</dt> </dl> </dd> <dt>

<span id="Audit_AccountLogon"></span><span id="audit_accountlogon"></span><span id="AUDIT_ACCOUNTLOGON"></span>**AccountLogon di controllo \_**
</dt> <dd> <dl> <dt>

69979850-797a-11d9-bed3-505054503030
</dt> <dt>



Controllare i tentativi di accesso da parte degli account con privilegi che accedono al controller di dominio. Questi eventi di controllo vengono generati quando il [*centro distribuzione chiavi*](/windows/desktop/SecGloss/k-gly) Kerberos (KDC) accede al controller di dominio.


</dt> </dl> </dd> </dl>

Le costanti seguenti rappresentano le sottocategorie degli eventi dei criteri di controllo. Queste costanti sono definite come strutture **GUID** in Ntsecapi. h.

<dl> <span id="Audit_System_SecurityStateChange"></span><span id="audit_system_securitystatechange"></span><span id="AUDIT_SYSTEM_SECURITYSTATECHANGE"></span>**Controllo \_ di System \_ SecurityStateChange** (0cce9210-69ae-11d9-BED3-505054503030) <span id="Audit_System_SecuritySubsystemExtension"></span> <span id="audit_system_securitysubsystemextension"></span> <span id="AUDIT_SYSTEM_SECURITYSUBSYSTEMEXTENSION"></span> **Audit \_ System \_ SecuritySubsystemExtension** (0cce9211-69ae-11d9-BED3-505054503030) <span id="Audit_System_Integrity"></span> <span id="audit_system_integrity"></span> <span id="AUDIT_SYSTEM_INTEGRITY"></span> **Audit \_ System \_ Integrity** (0cce9212-69ae-11d9-BED3-505054503030) audit System <span id="Audit_System_IPSecDriverEvents"></span> <span id="audit_system_ipsecdriverevents"></span> <span id="AUDIT_SYSTEM_IPSECDRIVEREVENTS"></span> **\_ \_ IPSecDriverEvents** (0cce9213-69ae-11d9-BED3-505054503030) audit System others (0cce9214-69ae-11d9-BED3-505054503030) Audit logon logon (0cce9215-69ae-11d9-BED3-505054503030) Audit Login <span id="Audit_System_Others"></span> <span id="audit_system_others"></span> <span id="AUDIT_SYSTEM_OTHERS"></span> **\_ \_** <span id="Audit_Logon_Logon"></span> <span id="audit_logon_logon"></span> <span id="AUDIT_LOGON_LOGON"></span> **\_ \_** <span id="Audit_Logon_Logoff"></span> <span id="audit_logon_logoff"></span> <span id="AUDIT_LOGON_LOGOFF"></span> **\_ \_ disconnessione** (0cce9216-69ae-11d9-BED3-505054503030) Audit logon <span id="Audit_Logon_AccountLockout"></span> <span id="audit_logon_accountlockout"></span> <span id="AUDIT_LOGON_ACCOUNTLOCKOUT"></span> **\_ \_ AccountLockout** (0cce9217-69ae-11d9-BED3-505054503030) audit <span id="Audit_Logon_IPSecMainMode"></span> <span id="audit_logon_ipsecmainmode"></span> <span id="AUDIT_LOGON_IPSECMAINMODE"></span> **\_ Logon \_ IPSecMainMode** (0cce9218-69ae-11d9-BED3-505054503030) <span id="Audit_Logon_IPSecQuickMode"></span> <span id="audit_logon_ipsecquickmode"></span> <span id="AUDIT_LOGON_IPSECQUICKMODE"></span> **Audit \_ login \_ IPSecQuickMode** (0cce9219-69ae-11d9-BED3-505054503030) <span id="Audit_Logon_IPSecUserMode"></span> <span id="audit_logon_ipsecusermode"></span> <span id="AUDIT_LOGON_IPSECUSERMODE"></span> **Audit \_ Logon \_ IPSecUserMode** (0cce921a-69ae-11d9-BED3-505054503030) Audit logon <span id="Audit_Logon_SpecialLogon"></span> <span id="audit_logon_speciallogon"></span> <span id="AUDIT_LOGON_SPECIALLOGON"></span> **\_ \_ SpecialLogon** (0cce921b-69ae-11d9-BED3-505054503030) Audit logon <span id="Audit_Logon_Others"></span> <span id="audit_logon_others"></span> <span id="AUDIT_LOGON_OTHERS"></span> **\_ \_ others** (0cce921c-69ae-11d9-BED3-505054503030) <span id="Audit_ObjectAccess_FileSystem"></span> <span id="audit_objectaccess_filesystem"></span> <span id="AUDIT_OBJECTACCESS_FILESYSTEM"></span> **Audit \_ ObjectAccess \_ filesystem** (0cce921d-69ae-11d9-BED3-505054503030) audit <span id="Audit_ObjectAccess_Registry"></span> <span id="audit_objectaccess_registry"></span> <span id="AUDIT_OBJECTACCESS_REGISTRY"></span> **\_ ObjectAccess \_ Registry** (0cce921e-69ae-11d9-BED3-505054503030) audit ObjectAccess <span id="Audit_ObjectAccess_Kernel"></span> <span id="audit_objectaccess_kernel"></span> <span id="AUDIT_OBJECTACCESS_KERNEL"></span> **\_ \_ kernel** (0cce921f-69ae-11d9-BED3-505054503030) <span id="Audit_ObjectAccess_Sam"></span> <span id="audit_objectaccess_sam"></span> <span id="AUDIT_OBJECTACCESS_SAM"></span> **Audit \_ ObjectAccess \_ Sam** (0cce9220-69ae-11d9-BED3-505054503030) <span id="Audit_ObjectAccess_CertificationServices"></span> <span id="audit_objectaccess_certificationservices"></span> <span id="AUDIT_OBJECTACCESS_CERTIFICATIONSERVICES"></span> **Audit \_ ObjectAccess \_ CertificationServices** (0cce9221-69ae-11d9-BED3-505054503030) <span id="Audit_ObjectAccess_ApplicationGenerated"></span> <span id="audit_objectaccess_applicationgenerated"></span> <span id="AUDIT_OBJECTACCESS_APPLICATIONGENERATED"></span> **Audit \_ ObjectAccess \_ ApplicationGenerated** (0cce9222-69ae-11d9-BED3-505054503030) audit <span id="Audit_ObjectAccess_Handle"></span> <span id="audit_objectaccess_handle"></span> <span id="AUDIT_OBJECTACCESS_HANDLE"></span> **\_ ObjectAccess \_ handle** (0cce9223-69ae-11d9-BED3-505054503030) audit <span id="Audit_ObjectAccess_Share"></span> <span id="audit_objectaccess_share"></span> <span id="AUDIT_OBJECTACCESS_SHARE"></span> **\_ ObjectAccess \_ share** (0cce9224-69ae-11d9-BED3-505054503030) audit <span id="Audit_ObjectAccess_FirewallPacketDrops"></span> <span id="audit_objectaccess_firewallpacketdrops"></span> <span id="AUDIT_OBJECTACCESS_FIREWALLPACKETDROPS"></span> **\_ ObjectAccess \_ FirewallPacketDrops** (0cce9225-69ae-11d9-BED3-505054503030) audit ObjectAccess FirewallConnection <span id="Audit_ObjectAccess_FirewallConnection"></span> <span id="audit_objectaccess_firewallconnection"></span> <span id="AUDIT_OBJECTACCESS_FIREWALLCONNECTION"></span> (0cce9226-69ae-11d9-BED3-505054503030) audit **\_ \_** <span id="Audit_ObjectAccess_Other"></span> <span id="audit_objectaccess_other"></span> <span id="AUDIT_OBJECTACCESS_OTHER"></span> **\_ ObjectAccess \_ other** (0cce9227-69ae-11d9-BED3-505054503030) audit <span id="Audit_PrivilegeUse_Sensitive"></span> <span id="audit_privilegeuse_sensitive"></span> <span id="AUDIT_PRIVILEGEUSE_SENSITIVE"></span> **\_ PrivilegeUse \_ sensitive** (0cce9228-69ae-11d9-BED3-505054503030) audit <span id="Audit_PrivilegeUse_NonSensitive"></span> <span id="audit_privilegeuse_nonsensitive"></span> <span id="AUDIT_PRIVILEGEUSE_NONSENSITIVE"></span> **\_ PrivilegeUse \_ nonsensitive** (0cce9229-69ae-11d9-BED3-505054503030) audit PrivilegeUse <span id="Audit_PrivilegeUse_Others"></span> <span id="audit_privilegeuse_others"></span> <span id="AUDIT_PRIVILEGEUSE_OTHERS"></span> **\_ \_ others** (0cce922a-69ae-11d9-BED3-505054503030) <span id="Audit_DetailedTracking_ProcessCreation"></span> <span id="audit_detailedtracking_processcreation"></span> <span id="AUDIT_DETAILEDTRACKING_PROCESSCREATION"></span> **Audit \_ DetailedTracking \_** ProcessCreation (0cce922b-69ae-11d9-BED3-505054503030) audit <span id="Audit_DetailedTracking_ProcessTermination"></span> <span id="audit_detailedtracking_processtermination"></span> <span id="AUDIT_DETAILEDTRACKING_PROCESSTERMINATION"></span> **\_ DetailedTracking \_ ProcessTermination** (0cce922c-69ae-11d9-BED3-505054503030) <span id="Audit_DetailedTracking_DpapiActivity"></span> <span id="audit_detailedtracking_dpapiactivity"></span> <span id="AUDIT_DETAILEDTRACKING_DPAPIACTIVITY"></span> **Audit \_ \_** DetailedTracking DpapiActivity ( 0cce922d-69ae-11d9-BED3-505054503030) <span id="Audit_DetailedTracking_RpcCall"></span> <span id="audit_detailedtracking_rpccall"></span> <span id="AUDIT_DETAILEDTRACKING_RPCCALL"></span> **Audit \_ DetailedTracking \_ RpcCall** (0cce922e-69ae-11d9-BED3-505054503030) audit <span id="Audit_PolicyChange_AuditPolicy"></span> <span id="audit_policychange_auditpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUDITPOLICY"></span> **\_ PolicyChange \_** AuditPolicy (0cce922f-69ae-11d9-BED3-505054503030) <span id="Audit_PolicyChange_AuthenticationPolicy"></span> <span id="audit_policychange_authenticationpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUTHENTICATIONPOLICY"></span> **Audit \_ PolicyChange \_** AuthenticationPolicy (0cce9230-69ae-11d9-BED3-505054503030) audit <span id="Audit_PolicyChange_AuthorizationPolicy"></span> <span id="audit_policychange_authorizationpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUTHORIZATIONPOLICY"></span> **\_ PolicyChange \_ AuthorizationPolicy** (0cce9231-69ae-11d9-BED3-505054503030) <span id="Audit_PolicyChange_MpsscvRulePolicy"></span> <span id="audit_policychange_mpsscvrulepolicy"></span> <span id="AUDIT_POLICYCHANGE_MPSSCVRULEPOLICY"></span> **Audit \_ PolicyChange \_ MpsscvRulePolicy** (0cce9232-69ae-11d9-BED3-505054503030) audit <span id="Audit_PolicyChange_WfpIPSecPolicy"></span> <span id="audit_policychange_wfpipsecpolicy"></span> <span id="AUDIT_POLICYCHANGE_WFPIPSECPOLICY"></span> **\_ PolicyChange \_ WfpIPSecPolicy** (0cce9233-69ae-11d9-BED3-505054503030) audit PolicyChange <span id="Audit_PolicyChange_Others"></span> <span id="audit_policychange_others"></span> <span id="AUDIT_POLICYCHANGE_OTHERS"></span> **\_ \_ others** (0cce9234-69ae-11d9-BED3-505054503030) audit AccountManagement <span id="Audit_AccountManagement_UserAccount"></span> <span id="audit_accountmanagement_useraccount"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_USERACCOUNT"></span> **\_ \_ AccountUtente** (0cce9235-69ae-11d9-BED3-505054503030) audit <span id="Audit_AccountManagement_ComputerAccount"></span> <span id="audit_accountmanagement_computeraccount"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_COMPUTERACCOUNT"></span> **\_ AccountManagement \_ ComputerAccount** (0cce9236-69ae-11d9-BED3-505054503030) audit AccountManagement <span id="Audit_AccountManagement_SecurityGroup"></span> <span id="audit_accountmanagement_securitygroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_SECURITYGROUP"></span> **\_ \_ SecurityGroup** (0cce9237-69ae-11d9-BED3-505054503030) audit <span id="Audit_AccountManagement_DistributionGroup"></span> <span id="audit_accountmanagement_distributiongroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_DISTRIBUTIONGROUP"></span> **\_ AccountManagement \_ DistributionGroup** (0cce9238-69ae-11d9-BED3-505054503030) audit <span id="Audit_AccountManagement_ApplicationGroup"></span> <span id="audit_accountmanagement_applicationgroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_APPLICATIONGROUP"></span> **\_ AccountManagement \_ ApplicationGroup** (0cce9239-69ae-11d9-BED3-505054503030) <span id="Audit_AccountManagement_Others"></span> <span id="audit_accountmanagement_others"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_OTHERS"></span> **Audit AccountManagement \_ \_ others** (0cce923a-69ae-11d9-BED3-505054503030) <span id="Audit_DSAccess_DSAccess"></span> <span id="audit_dsaccess_dsaccess"></span> <span id="AUDIT_DSACCESS_DSACCESS"></span> **Audit \_ DSAccess \_ DSAccess** (0cce923b-69ae-11d9-BED3-505054503030) audit <span id="Audit_DsAccess_AdAuditChanges"></span> <span id="audit_dsaccess_adauditchanges"></span> <span id="AUDIT_DSACCESS_ADAUDITCHANGES"></span> **\_ DSAccess \_ AdAuditChanges** (0cce923c-69ae-11d9-BED3-505054503030) audit <span id="Audit_Ds_Replication"></span> <span id="audit_ds_replication"></span> <span id="AUDIT_DS_REPLICATION"></span> **\_ DS \_ Replication** (0cce923d-69ae-11d9-BED3-505054503030) audit <span id="Audit_Ds_DetailedReplication"></span> <span id="audit_ds_detailedreplication"></span> <span id="AUDIT_DS_DETAILEDREPLICATION"></span> **\_ DS \_ DetailedReplication** (0cce923e-69ae-11d9-BED3-505054503030) <span id="Audit_AccountLogon_CredentialValidation"></span> <span id="audit_accountlogon_credentialvalidation"></span> <span id="AUDIT_ACCOUNTLOGON_CREDENTIALVALIDATION"></span> **Audit \_ accountlogon \_ CredentialValidation** (0cce923f-69ae-11d9-BED3-505054503030) audit <span id="Audit_AccountLogon_Kerberos"></span> <span id="audit_accountlogon_kerberos"></span> <span id="AUDIT_ACCOUNTLOGON_KERBEROS"></span> **\_ accountlogon \_ Kerberos** (0cce9240-69ae-11d9-BED3-505054503030) <span id="Audit_AccountLogon_Others"></span> <span id="audit_accountlogon_others"></span> <span id="AUDIT_ACCOUNTLOGON_OTHERS"></span> **Audit \_ accountlogon \_ others** (0cce9241-69ae-11d9-BED3-505054503030) <span id="Audit_AccountLogon_KerbCredentialValidation"></span> <span id="audit_accountlogon_kerbcredentialvalidation"></span> <span id="AUDIT_ACCOUNTLOGON_KERBCREDENTIALVALIDATION"></span> **Audit \_ accountlogon \_ KerbCredentialValidation** (0cce9242-69ae-11d9-BED3-505054503030) audit <span id="Audit_Logon_NPS"></span> <span id="audit_logon_nps"></span> <span id="AUDIT_LOGON_NPS"></span> **\_ Logon \_ NPS** (0cce9243-69ae-11d9-BED3-505054503030)
</dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



 

