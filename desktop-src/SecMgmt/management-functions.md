---
description: Elenca le funzioni di supporto fornite dal set di strumenti di configurazione della sicurezza.
ms.assetid: 5a771014-1706-490f-8540-ec516652cb83
title: Funzioni di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df5c905207b707a21a97842c62385969fb2ac2d32279b9c7fa9f5a32c4fbbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968937"
---
# <a name="security-management-functions"></a>Funzioni di gestione della sicurezza

Questa sezione contiene argomenti per i gruppi di funzioni seguenti:

-   [Funzioni di callback degli allegati](#attachment-callback-functions)
-   [Funzioni del motore degli allegati](#attachment-engine-functions)
-   [Funzioni dei criteri LSA](#lsa-policy-functions)
    -   [Funzioni dei criteri](#lsa-policy-functions)
    -   [Funzioni di account](#account-functions)
    -   [Funzioni di dominio trusted](#trusted-domain-functions)
    -   [Funzioni di dati privati](#private-data-functions)
    -   [Funzioni varie](#miscellaneous-functions)
-   [Funzioni dell'account del servizio gestito](#managed-service-account-functions)
-   [Funzioni di filtro password](#password-filter-functions)
-   [Funzioni più sicure](#safer-functions)

## <a name="attachment-callback-functions"></a>Funzioni di callback degli allegati

Le funzioni di supporto seguenti vengono fornite dal set di strumenti di configurazione della sicurezza e possono essere usate dai motori degli allegati e dagli snap-in di estensione per leggere e scrivere i dati di configurazione.



| Funzione di callback                                         | Descrizione                                                                                 |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**INFORMAZIONI GRATUITE DI PFSCE \_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_free_info)<br/>   | Usato per liberare la memoria allocata da queste funzioni di supporto.<br/>                        |
| [**INFORMAZIONI DI LOG DI PFSCE \_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_log_info)<br/>     | Utilizzato per registrare il messaggio nel file di log di configurazione o nel file di log di analisi.<br/>          |
| [**INFORMAZIONI QUERY PFSCE \_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)<br/> | Consente di eseguire query sulle informazioni di configurazione e analisi per un servizio specifico.<br/> |
| [**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)<br/>     | Consente di impostare le informazioni di configurazione e analisi per un servizio specifico.<br/>       |



 

## <a name="attachment-engine-functions"></a>Funzioni del motore degli allegati



| Funzione                                                              | Descrizione                                                                                                                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)<br/> | Implementato dalla DLL del motore degli allegati. Il motore di configurazione della sicurezza chiama questa funzione quando viene analizzato il sistema.<br/>                                                           |
| [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)<br/>   | Implementato dalla DLL del motore degli allegati. Il motore di configurazione della sicurezza chiama questa funzione quando il sistema è configurato.<br/>                                                         |
| [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)<br/>   | Implementato dalla DLL del motore degli allegati. Il motore di configurazione della sicurezza chiama questa funzione quando riceve una richiesta di aggiornamento della configurazione dall'estensione dello snap-in degli allegati.<br/> |



 

## <a name="lsa-policy-functions"></a>Funzioni dei criteri LSA

Negli argomenti seguenti vengono fornite informazioni di riferimento per le [*funzioni dei*](/windows/desktop/SecGloss/l-gly) criteri dell'autorità di sicurezza locale (LSA).



| Argomento                               | Descrizione                                                                                                                                                                                   |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funzioni dei criteri<br/>         | Informazioni dettagliate sulle funzioni usate per aprire [**l'oggetto Criteri**](policy-object.md) locale e per impostare o recuperare informazioni sui criteri globali.<br/>                                                  |
| Funzioni di account<br/>        | Informazioni dettagliate sulle funzioni usate per gestire le autorizzazioni dell'account e per creare ed eliminare account utente.<br/>                                                                                       |
| Funzioni di dominio trusted<br/> | Vengono fornite informazioni dettagliate sulle funzioni usate per creare ed eliminare relazioni di dominio trusted e per impostare e recuperare informazioni su tali domini trusted.<br/>                                          |
| Funzioni di dati privati<br/>   | Non usare le funzioni di dati privati LSA. Usare invece le [**funzioni CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)<br/> |
| Funzioni varie<br/>  | Funzioni dettagliate non descritte altrove.<br/>                                                                                                                                         |



 

### <a name="policy-functions"></a>Funzioni dei criteri

Le funzioni seguenti enumerano gli account utente e i domini trusted, ricevono notifiche di modifica dei criteri e ricercano nomi di account e SID.



| Funzione                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)<br/>         | Enumera tutti gli account con un'autorizzazione utente specificata.<br/>                                                                                                                                                                                                                                                                         |
| [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/>                   | Enumera i domini trusted.<br/>                                                                                                                                                                                                                                                                                                            |
| [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames)<br/>                                               | Mappe i nomi specificati ai relativi SID. Restituisce il SID come coppia RID/SID di dominio.<br/>                                                                                                                                                                                                                                                         |
| [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2)<br/>                                             | Mappe i nomi specificati ai relativi SID. Restituisce il SID come elemento singolo.<br/>                                                                                                                                                                                                                                                               |
| [**LsaLookupPrivilegeValue**](/windows/desktop/api/ntlsa/nf-ntlsa-lsalookupprivilegevalue)<br/>                             | Recupera [*l'identificatore univoco locale*](/windows/desktop/SecGloss/l-gly) (LUID) usato dall'autorità di sicurezza locale (LSA) per rappresentare il nome del privilegio specificato. [](/windows/desktop/SecGloss/l-gly)<br/> |
| [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)<br/>                                                 | Mappe i nomi di account specificati ai relativi SID.<br/>                                                                                                                                                                                                                                                                                            |
| [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification)<br/>     | Registra un oggetto evento per ricevere notifiche quando le informazioni sui criteri locali vengono cambiate.<br/>                                                                                                                                                                                                                                              |
| [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification)<br/> | Annulla la registrazione di un oggetto evento che riceve notifiche di modifica dei criteri.<br/>                                                                                                                                                                                                                                                                 |



 

### <a name="account-functions"></a>Funzioni di account

Le funzioni seguenti aggiungono, enumerano ed eliminano le autorizzazioni per un account.



| Funzione                                                                  | Descrizione                                                                                                  |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights)<br/>             | Aggiungere autorizzazioni a un account. Se l'account non esiste già, viene creato.<br/>              |
| [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)<br/> | Enumerare le autorizzazioni concesse a un account.<br/>                                                  |
| [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)<br/>       | Rimuovere le autorizzazioni da un account. Quando vengono rimosse tutte le autorizzazioni, l'account viene eliminato.<br/> |



 

### <a name="trusted-domain-functions"></a>Funzioni di dominio trusted

Le funzioni seguenti creano, enumerano ed eliminano domini trusted e impostano e recuperano informazioni sui domini trusted.



| Funzione                                                                                                                                                    | Descrizione                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex)<br/>                                                                                     | Crea un nuovo [**oggetto TrustedDomain.**](trusteddomain-object.md)<br/>            |
| [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)<br/>                                                                                         | Rimuove un [**oggetto TrustedDomain.**](trusteddomain-object.md)<br/>                |
| [**LsaEnumerateTrustedDomains**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains)<br/> [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/> | Enumera i domini attualmente considerati attendibili dal sistema locale.<br/>                  |
| [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname)<br/>                                                                                 | Apre un handle per un [**oggetto TrustedDomain.**](trusteddomain-object.md)<br/>      |
| [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo)<br/>                                                                                   | Recupera informazioni su un dominio trusted. Il dominio è specificato dal SID.<br/>  |
| [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)<br/>                                                                       | Recupera informazioni su un dominio trusted. Il dominio viene specificato in base al nome.<br/> |
| [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)<br/>                                                                           | Imposta le informazioni per un dominio trusted. Il dominio viene specificato in base al nome.<br/>        |
| [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation)<br/>                                                                         | Imposta le informazioni per un dominio trusted. Il dominio è specificato dal SID.<br/>         |



 

### <a name="private-data-functions"></a>Funzioni di dati privati

Non usare le funzioni di dati privati LSA. Usare invece le [**funzioni CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)



| Funzione                                                            | Descrizione                                 |
|---------------------------------------------------------------------|---------------------------------------------|
| [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)<br/> | Recupera e decrittografa una stringa.<br/> |
| [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)<br/>       | Crittografa e archivia una stringa.<br/>    |



 

### <a name="miscellaneous-functions"></a>Funzioni varie

L'API criteri LSA include le tre funzioni seguenti che non rientrano in nessuna delle altre categorie di funzioni criteri LSA.



| Funzione                                                          | Descrizione                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)<br/>                           | Chiude un handle a un [**oggetto Policy**](policy-object.md) o a un [**oggetto TrustedDomain.**](trusteddomain-object.md)<br/> |
| [**LsaFreeMemory**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreememory)<br/>                 | Libera un buffer allocato da una funzione LSA.<br/>                                                                           |
| [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)<br/> | Converte un **valore NTSTATUS** in un Windows di errore.<br/>                                                                |



 

## <a name="managed-service-account-functions"></a>Funzioni dell'account del servizio gestito

Le funzioni seguenti vengono usate per creare, enumerare, trovare ed eliminare gli account del servizio gestito.



| Funzione                                                                      | Descrizione                                                                                                                 |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NetAddServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netaddserviceaccount)<br/>               | Crea un account del servizio gestito.<br/>                                                                               |
| [**NetEnumerateServiceAccounts**](/windows/desktop/api/Lmaccess/nf-lmaccess-netenumerateserviceaccounts)<br/> | Enumera gli account del server nel server specificato.<br/>                                                          |
| [**NetIsServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netisserviceaccount)<br/>                 | Verifica se l'account del servizio specificato esiste nell'archivio Netlogon nel server specificato.<br/>                |
| [**NetRemoveServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netremoveserviceaccount)<br/>         | Elimina l'account del servizio specificato dal database [di Active Directory.](/windows/desktop/AD/active-directory-domain-services)<br/> |



 

## <a name="password-filter-functions"></a>Funzioni di filtro password

Le funzioni di [*filtro delle password*](/windows/desktop/SecGloss/p-gly) seguenti vengono implementate dalle DLL di filtro delle password personalizzate per fornire il filtro delle password e la notifica di modifica della password.



| Funzione                                                            | Descrizione                                                     |
|---------------------------------------------------------------------|-----------------------------------------------------------------|
| [**InitializeChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_init_notification_routine)<br/> | Indica che viene inizializzata una DLL di filtro delle password.<br/> |
| [**PasswordChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_notification_routine)<br/>     | Indica che una password è stata modificata.<br/>          |
| [**Filtro password**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_filter_routine)<br/>                 | Convalida una nuova password in base ai criteri password.<br/>   |



 

## <a name="safer-functions"></a>Funzioni più sicure

Le funzioni Safer seguenti possono essere usate per controllare il livello più sicuro di qualsiasi eseguibile e per registrare gli eventi.



| Funzione                                                         | Descrizione                                                                                                                                                                          |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaferCloseLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercloselevel)                       | Chiude un HANDLE SAFER \_ LEVEL aperto usando la funzione \_ [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) o [**la funzione SaferCreateLevel.**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)<br/> |
| [**SaferComputeTokenFromLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercomputetokenfromlevel) | Limita un token usando le restrizioni specificate da un HANDLE SAFER \_ \_ LEVEL.<br/>                                                                                                 |
| [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)                     | Apre un HANDLE DI \_ LIVELLO \_ PIÙ SICURO.<br/>                                                                                                                                             |
| [**SaferGetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)     | Recupera informazioni su un livello di criteri.<br/>                                                                                                                               |
| [**SaferGetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetpolicyinformation)   | Recupera informazioni su un criterio.<br/>                                                                                                                                     |
| [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                 | Recupera informazioni su un livello.<br/>                                                                                                                                      |
| [**SaferiIsExecutableFileType**](/windows/desktop/api/WinSafer/nf-winsafer-saferiisexecutablefiletype) | Determina se un file specificato è un file eseguibile.<br/>                                                                                                                |
| [**SaferRecordEventLogEntry**](/windows/desktop/api/WinSafer/nf-winsafer-saferrecordeventlogentry)     | Invia un messaggio al registro eventi.<br/>                                                                                                                                         |
| [**SaferSetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safersetlevelinformation)     | Imposta le informazioni su un livello di criteri.<br/>                                                                                                                                |
| [**SaferSetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)    | Imposta i controlli dei criteri globali.<br/>                                                                                                                                          |



 

 

