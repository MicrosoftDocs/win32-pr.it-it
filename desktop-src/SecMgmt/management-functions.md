---
description: Elenca le funzioni di supporto fornite dal set di strumenti di configurazione della sicurezza.
ms.assetid: 5a771014-1706-490f-8540-ec516652cb83
title: Funzioni di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c17efd55b1dbb806295ac0a83763257ffcc97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884282"
---
# <a name="security-management-functions"></a>Funzioni di gestione della sicurezza

In questa sezione sono contenuti gli argomenti per i gruppi di funzioni seguenti:

-   [Funzioni di callback degli allegati](#attachment-callback-functions)
-   [Funzioni del motore degli allegati](#attachment-engine-functions)
-   [Funzioni dei criteri LSA](#lsa-policy-functions)
    -   [Funzioni dei criteri](#lsa-policy-functions)
    -   [Funzioni account](#account-functions)
    -   [Funzioni di dominio trusted](#trusted-domain-functions)
    -   [Funzioni di dati private](#private-data-functions)
    -   [Funzioni varie](#miscellaneous-functions)
-   [Funzioni dell'account del servizio gestito](#managed-service-account-functions)
-   [Funzioni di filtro password](#password-filter-functions)
-   [Funzioni più sicure](#safer-functions)

## <a name="attachment-callback-functions"></a>Funzioni di callback degli allegati

Le funzioni di supporto seguenti sono fornite dal set di strumenti di configurazione della sicurezza e possono essere usate dai motori degli allegati e dagli snap-in di estensione per leggere e scrivere i dati di configurazione.



| Funzione di callback                                         | Descrizione                                                                                 |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_informazioni gratuite di PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_free_info)<br/>   | Utilizzato per liberare la memoria allocata da queste funzioni di supporto.<br/>                        |
| [**\_informazioni log \_ PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_log_info)<br/>     | Utilizzato per registrare il messaggio nel file di log di configurazione o nel file di log di analisi.<br/>          |
| [**\_informazioni query \_ PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)<br/> | Utilizzato per eseguire una query sulle informazioni di configurazione e analisi per un servizio specifico.<br/> |
| [**\_informazioni sul set di PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)<br/>     | Consente di impostare le informazioni di configurazione e analisi per un servizio specifico.<br/>       |



 

## <a name="attachment-engine-functions"></a>Funzioni del motore degli allegati



| Funzione                                                              | Descrizione                                                                                                                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)<br/> | Implementata dalla DLL del motore degli allegati. Il motore di configurazione della sicurezza chiama questa funzione quando il sistema viene analizzato.<br/>                                                           |
| [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)<br/>   | Implementata dalla DLL del motore degli allegati. Il motore di configurazione della sicurezza chiama questa funzione quando il sistema è configurato.<br/>                                                         |
| [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)<br/>   | Implementata dalla DLL del motore degli allegati. Il motore di configurazione della sicurezza chiama questa funzione quando riceve una richiesta di aggiornamento della configurazione dall'estensione dello snap-in allegato.<br/> |



 

## <a name="lsa-policy-functions"></a>Funzioni dei criteri LSA

Negli argomenti seguenti vengono fornite informazioni di riferimento per le funzioni dei criteri dell' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA).



| Argomento                               | Descrizione                                                                                                                                                                                   |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funzioni dei criteri<br/>         | Funzioni Details utilizzate per aprire l'oggetto [**criteri**](policy-object.md) locale e per impostare o recuperare informazioni sui criteri globali.<br/>                                                  |
| Funzioni account<br/>        | Funzioni Details utilizzate per gestire le autorizzazioni dell'account e per creare ed eliminare gli account utente.<br/>                                                                                       |
| Funzioni di dominio trusted<br/> | Funzioni Details utilizzate per creare ed eliminare relazioni di dominio trusted e per impostare e recuperare informazioni su tali domini trusted.<br/>                                          |
| Funzioni di dati private<br/>   | Non usare funzioni di dati private LSA. Usare invece le funzioni [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) .<br/> |
| Funzioni varie<br/>  | Funzioni Details non descritte altrove.<br/>                                                                                                                                         |



 

### <a name="policy-functions"></a>Funzioni dei criteri

Le funzioni seguenti enumerano gli account utente e i domini trusted, ricevono le notifiche di modifica dei criteri e i nomi e i SID degli account di ricerca.



| Funzione                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)<br/>         | Enumera tutti gli account che dispongono di un'autorizzazione utente specificata.<br/>                                                                                                                                                                                                                                                                         |
| [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/>                   | Enumera i domini trusted.<br/>                                                                                                                                                                                                                                                                                                            |
| [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames)<br/>                                               | Esegue il mapping dei nomi specificati ai SID. Restituisce il SID come coppia di SID RID/dominio.<br/>                                                                                                                                                                                                                                                         |
| [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2)<br/>                                             | Esegue il mapping dei nomi specificati ai SID. Restituisce il SID come singolo elemento.<br/>                                                                                                                                                                                                                                                               |
| [**LsaLookupPrivilegeValue**](/windows/desktop/api/ntlsa/nf-ntlsa-lsalookupprivilegevalue)<br/>                             | Recupera l' [*identificatore univoco locale*](/windows/desktop/SecGloss/l-gly) (LUID) usato dall' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) per rappresentare il nome del privilegio specificato.<br/> |
| [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)<br/>                                                 | Esegue il mapping tra i nomi di account specificati e i SID.<br/>                                                                                                                                                                                                                                                                                            |
| [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification)<br/>     | Registra un oggetto evento per ricevere notifiche quando le informazioni sui criteri locali cambiano.<br/>                                                                                                                                                                                                                                              |
| [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification)<br/> | Annulla la registrazione di un oggetto evento che riceve notifiche di modifica dei criteri.<br/>                                                                                                                                                                                                                                                                 |



 

### <a name="account-functions"></a>Funzioni account

Le funzioni seguenti aggiungono, enumerano ed eliminano le autorizzazioni per un account.



| Funzione                                                                  | Descrizione                                                                                                  |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights)<br/>             | Aggiungere le autorizzazioni a un account. Se l'account non esiste già, viene creato.<br/>              |
| [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)<br/> | Enumerare le autorizzazioni concesse a un account.<br/>                                                  |
| [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)<br/>       | Rimuovere le autorizzazioni da un account. Quando vengono rimosse tutte le autorizzazioni, l'account viene eliminato.<br/> |



 

### <a name="trusted-domain-functions"></a>Funzioni di dominio trusted

Le funzioni seguenti creano, enumerano ed eliminano domini trusted e impostano e recuperano informazioni sul dominio attendibile.



| Funzione                                                                                                                                                    | Descrizione                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex)<br/>                                                                                     | Crea un nuovo oggetto [**trustedDomain**](trusteddomain-object.md) .<br/>            |
| [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)<br/>                                                                                         | Rimuove un oggetto [**trustedDomain**](trusteddomain-object.md) .<br/>                |
| [**LsaEnumerateTrustedDomains**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains)<br/> [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/> | Enumera i domini attualmente considerati attendibili dal sistema locale.<br/>                  |
| [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname)<br/>                                                                                 | Apre un handle per un oggetto [**trustedDomain**](trusteddomain-object.md) .<br/>      |
| [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo)<br/>                                                                                   | Recupera le informazioni su un dominio trusted. Il dominio è specificato da SID.<br/>  |
| [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)<br/>                                                                       | Recupera le informazioni su un dominio trusted. Il dominio viene specificato in base al nome.<br/> |
| [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)<br/>                                                                           | Imposta le informazioni per un dominio trusted. Il dominio viene specificato in base al nome.<br/>        |
| [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation)<br/>                                                                         | Imposta le informazioni per un dominio trusted. Il dominio è specificato da SID.<br/>         |



 

### <a name="private-data-functions"></a>Funzioni di dati private

Non usare funzioni di dati private LSA. Usare invece le funzioni [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) .



| Funzione                                                            | Descrizione                                 |
|---------------------------------------------------------------------|---------------------------------------------|
| [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)<br/> | Recupera e decrittografa una stringa.<br/> |
| [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)<br/>       | Crittografa e archivia una stringa.<br/>    |



 

### <a name="miscellaneous-functions"></a>Funzioni varie

L'API dei criteri LSA presenta le tre funzioni seguenti che non rientrano nelle altre categorie di funzioni dei criteri LSA.



| Funzione                                                          | Descrizione                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)<br/>                           | Chiude un handle a un oggetto [**criteri**](policy-object.md) o a un oggetto [**trustedDomain**](trusteddomain-object.md) .<br/> |
| [**LsaFreeMemory**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreememory)<br/>                 | Libera un buffer allocato da una funzione LSA.<br/>                                                                           |
| [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)<br/> | Converte un valore **NTSTATUS** in un codice di errore di Windows.<br/>                                                                |



 

## <a name="managed-service-account-functions"></a>Funzioni dell'account del servizio gestito

Le funzioni seguenti vengono utilizzate per creare, enumerare, trovare ed eliminare gli account dei servizi gestiti.



| Funzione                                                                      | Descrizione                                                                                                                 |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NetAddServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netaddserviceaccount)<br/>               | Consente di creare un account del servizio gestito.<br/>                                                                               |
| [**NetEnumerateServiceAccounts**](/windows/desktop/api/Lmaccess/nf-lmaccess-netenumerateserviceaccounts)<br/> | Enumera gli account del server nel server specificato.<br/>                                                          |
| [**NetIsServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netisserviceaccount)<br/>                 | Verifica se l'account di servizio specificato esiste nell'archivio Netlogon sul server specificato.<br/>                |
| [**NetRemoveServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netremoveserviceaccount)<br/>         | Elimina l'account di servizio specificato dal database [Active Directory](/windows/desktop/AD/active-directory-domain-services) .<br/> |



 

## <a name="password-filter-functions"></a>Funzioni di filtro password

Le funzioni di [*filtro password*](/windows/desktop/SecGloss/p-gly) seguenti sono implementate dalle DLL del filtro password personalizzate per fornire il filtro delle password e la notifica di modifica della password.



| Funzione                                                            | Descrizione                                                     |
|---------------------------------------------------------------------|-----------------------------------------------------------------|
| [**InitializeChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_init_notification_routine)<br/> | Indica che è stata inizializzata una DLL di filtro delle password.<br/> |
| [**PasswordChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_notification_routine)<br/>     | Indica che è stata modificata una password.<br/>          |
| [**PasswordFilter**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_filter_routine)<br/>                 | Convalida una nuova password in base ai criteri delle password.<br/>   |



 

## <a name="safer-functions"></a>Funzioni più sicure

Le funzioni più sicure riportate di seguito possono essere usate per verificare il livello più sicuro di qualsiasi eseguibile e registrare gli eventi.



| Funzione                                                         | Descrizione                                                                                                                                                                          |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaferCloseLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercloselevel)                       | Chiude un \_ handle di livello più sicuro \_ aperto utilizzando la funzione [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) o la funzione [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel) .<br/> |
| [**SaferComputeTokenFromLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercomputetokenfromlevel) | Limita un token usando le restrizioni specificate da un handle di \_ livello più sicuro \_ .<br/>                                                                                                 |
| [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)                     | Apre un handle di livello più sicuro \_ \_ .<br/>                                                                                                                                             |
| [**SaferGetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)     | Recupera le informazioni relative a un livello di criteri.<br/>                                                                                                                               |
| [**SaferGetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetpolicyinformation)   | Recupera le informazioni relative a un criterio.<br/>                                                                                                                                     |
| [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                 | Recupera informazioni su un livello.<br/>                                                                                                                                      |
| [**SaferiIsExecutableFileType**](/windows/desktop/api/WinSafer/nf-winsafer-saferiisexecutablefiletype) | Determina se un file specificato è un file eseguibile.<br/>                                                                                                                |
| [**SaferRecordEventLogEntry**](/windows/desktop/api/WinSafer/nf-winsafer-saferrecordeventlogentry)     | Invia un messaggio al registro eventi.<br/>                                                                                                                                         |
| [**SaferSetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safersetlevelinformation)     | Imposta le informazioni relative a un livello di criteri.<br/>                                                                                                                                |
| [**SaferSetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)    | Imposta i controlli dei criteri globali.<br/>                                                                                                                                          |



 

 

