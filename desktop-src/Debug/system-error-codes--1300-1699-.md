---
description: Descrive i codici di errore 1300-1699 definiti nel file di intestazione WinError.h ed è destinato agli sviluppatori.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Codici di errore di sistema (1300-1699) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7aeb1c3642331db8ed3215d55a6d77e1e7b2a98c3859a5eb64a1d5b60350d24a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119310921"
---
# <a name="system-error-codes-1300-1699"></a>Codici di errore di sistema (1300-1699)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che ese tracciano errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella [pagina Codici di](system-error-codes.md) errore.

Nell'elenco seguente vengono descritti [i codici di errore di](system-error-codes.md) sistema per gli errori da 1300 a 1699. Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la [**funzione FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il flag **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERRORE \_ NON \_ ASSEGNATO \_**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



Non tutti i privilegi o i gruppi a cui si fa riferimento vengono assegnati al chiamante.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERRORE \_ DI CUI NON È STATO ESEGUITO IL \_ \_ MAPPING**
</dt> <dd> <dl> <dt>

1301 (0x515)
</dt> <dt>



Non è stato eseguito il mapping tra i nomi di account e gli ID di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERRORE \_ NESSUNA QUOTA PER \_ \_ \_ L'ACCOUNT**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



Nessun limite di quota di sistema è impostato in modo specifico per questo account.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERRORE \_ CHIAVE SESSIONE UTENTE \_ \_ \_ LOCALE**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



Non è disponibile alcuna chiave di crittografia. È stata restituita una chiave di crittografia nota.


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERRORE \_ PASSWORD \_ LM \_ NULL**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



La password è troppo complessa per essere convertita in una password di LAN Manager. La password di LAN Manager restituita è una **stringa NULL.**


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERRORE \_ REVISIONE \_ SCONOSCIUTA**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



Il livello di revisione è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**MANCATA \_ CORRISPONDENZA \_ REVISIONE ERRORE**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



Indica che due livelli di revisione non sono compatibili.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERRORE PROPRIETARIO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



Questo ID di sicurezza non può essere assegnato come proprietario di questo oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERRORE GRUPPO \_ \_ PRIMARIO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



Questo ID di sicurezza non può essere assegnato come gruppo primario di un oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERRORE \_ NESSUN TOKEN DI \_ \_ RAPPRESENTAZIONE**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



È stato effettuato un tentativo di operare su un token di rappresentazione da parte di un thread che attualmente non rappresenta un client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERRORE IMPOSSIBILE \_ \_ DISABILITARE \_ OBBLIGATORIO**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



Il gruppo potrebbe non essere disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERRORE \_ NESSUN SERVER DI \_ \_ ACCESSO**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



Attualmente non sono disponibili server di accesso per la gestione della richiesta di accesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR \_ NO \_ SUCH \_ LOGON \_ SESSION**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



Una sessione di accesso specificata non esiste. È possibile che sia già stata terminata.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERRORE \_ NESSUN \_ \_ PRIVILEGIO DI QUESTO TIPO**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



Un privilegio specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**PRIVILEGIO \_ \_ DI ERRORE NON \_ MANTENUTO**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



Il client non dispone di un privilegio necessario.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERRORE NOME \_ \_ ACCOUNT NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1315 (0x523)
</dt> <dt>



Il nome specificato non è un nome di account formulato correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERRORE \_ UTENTE \_ ESISTENTE**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



L'account specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERRORE \_ NESSUN UTENTE DI QUESTO \_ \_ TIPO**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



L'account specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**IL \_ GRUPPO DI ERRORI \_ ESISTE**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



Il gruppo specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERRORE \_ NESSUN GRUPPO DI QUESTO \_ \_ TIPO**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



Il gruppo specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**MEMBRO \_ ERROR \_ NEL \_ GRUPPO**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



L'account utente specificato è già membro del gruppo specificato oppure il gruppo specificato non può essere eliminato perché contiene un membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**MEMBRO \_ DI ERRORE NON IN UN \_ \_ \_ GRUPPO**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



L'account utente specificato non è un membro dell'account di gruppo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERRORE \_ ULTIMO \_ AMMINISTRATORE**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



Questa operazione non è consentita perché potrebbe causare la disabilitazione, l'eliminazione o l'impossibilità di accedere a un account di amministrazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERRORE \_ PASSWORD \_ ERRATA**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



Impossibile aggiornare la password. Il valore specificato come password corrente non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERRORE \_ DURANTE IL FORMATO NON CORRETTO DELLA \_ \_ PASSWORD**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



Impossibile aggiornare la password. Il valore fornito per la nuova password contiene valori non consentiti nelle password.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**RESTRIZIONE \_ PASSWORD \_ DI ERRORE**
</dt> <dd> <dl> <dt>

1325 (0x52D)
</dt> <dt>



Impossibile aggiornare la password. Il valore fornito per la nuova password non soddisfa i requisiti di lunghezza, complessità o cronologia del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERRORE DURANTE \_ \_ L'ACCESSO**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



Il nome utente o la password non sono corretti.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**RESTRIZIONE \_ DELL'ACCOUNT \_ DI ERRORE**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



Le restrizioni dell'account impediscono all'utente di eseguire l'accesso. Ad esempio: le password vuote non sono consentite, i tempi di accesso sono limitati o è stata applicata una restrizione dei criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERRORE ORE \_ DI \_ ACCESSO NON \_ VALIDE**
</dt> <dd> <dl> <dt>

1328 (0x530)
</dt> <dt>



L'account ha restrizioni di tempo che non esere possibile accedere in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERRORE \_ WORKSTATION \_ NON VALIDA**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



Questo utente non è autorizzato ad accedere a questo computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**PASSWORD \_ DI ERRORE \_ SCADUTA**
</dt> <dd> <dl> <dt>

1330 (0x532)
</dt> <dt>



La password per questo account è scaduta.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**ACCOUNT \_ DI ERRORE \_ DISABILITATO**
</dt> <dd> <dl> <dt>

1331 (0x533)
</dt> <dt>



Questo utente non può accedere perché questo account è attualmente disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERRORE \_ NON \_ MAPPATO**
</dt> <dd> <dl> <dt>

1332 (0x534)
</dt> <dt>



Non è stato eseguito alcun mapping tra i nomi di account e gli ID di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERRORE \_ TROPPI \_ \_ LUIDS \_ RICHIESTI**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



Troppi identificatori utente locali (LUID) sono stati richiesti contemporaneamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERRORE \_ LUIDS \_ ESAURITO**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



Non sono disponibili altri IDENTIFICATORI UTENTE LOCALI (LUID).


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERRORE \_ AUTORITÀ SECONDARIA NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

1335 (0x537)
</dt> <dt>



La parte di sottoautorità di un ID di sicurezza non è valida per questo uso specifico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERRORE \_ \_ ACL NON VALIDO**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



La struttura dell'elenco di controllo di accesso (ACL) non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERRORE \_ \_ SID NON VALIDO**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



La struttura dell'ID di sicurezza non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERRORE \_ \_ DESCR DI \_ SICUREZZA NON VALIDO**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



La struttura del descrittore di sicurezza non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERRORE \_ \_ ACL DI \_ EREDITARIETÀ NON ERTA**
</dt> <dd> <dl> <dt>

1340 (0x53C)
</dt> <dt>



Impossibile creare l'elenco di controllo di accesso (ACL) ereditato o la voce di controllo di accesso (ACE).


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**SERVER \_ DEGLI ERRORI \_ DISABILITATO**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



Il server è attualmente disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**\_SERVER DI ERRORE NON \_ \_ DISABILITATO**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



Il server è attualmente abilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERRORE AUTORITÀ \_ \_ ID NON \_ VALIDA**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



Il valore fornito è un valore non valido per un'autorità identificatore.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**LO \_ SPAZIO ASSEGNATO PER \_ L'ERRORE \_ È STATO SUPERATO**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



Non è disponibile altra memoria per gli aggiornamenti delle informazioni di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERRORE ATTRIBUTI \_ GRUPPO \_ NON \_ VALIDI**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



Gli attributi specificati non sono validi o non sono compatibili con gli attributi per l'intero gruppo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERRORE \_ LIVELLO DI \_ RAPPRESENTAZIONE NON \_ ERTA**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



Non è stato fornito il livello richiesto di rappresentazione di client oppure il livello di rappresentazione fornito non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERRORE \_ CANT \_ OPEN \_ ANONYMOUS**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



Impossibile aprire un token di sicurezza a livello anonimo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**CLASSE \_ DI CONVALIDA ERRORE NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



La classe di informazioni di convalida richiesta non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERRORE \_ TIPO DI TOKEN NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



Il tipo del token non è appropriato per il tentativo di utilizzo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERRORE \_ NESSUNA SICUREZZA PER \_ \_ \_ L'OGGETTO**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



Impossibile eseguire un'operazione di sicurezza su un oggetto a cui non è associata alcuna sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERRORE \_ CANT \_ ACCESS DOMAIN \_ \_ INFO**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



Impossibile leggere le informazioni di configurazione dal controller di dominio, perché il computer non è disponibile o l'accesso è stato negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERRORE \_ STATO DEL SERVER NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



Lo stato del account manager di sicurezza (SAM) o dell'autorità di sicurezza locale (LSA) non è corretto per eseguire l'operazione di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERRORE \_ STATO DI DOMINIO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



Lo stato del dominio non è corretto per eseguire l'operazione di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERRORE \_ RUOLO DI DOMINIO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



Questa operazione è consentita solo per il controller di dominio primario del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERRORE \_ NESSUN DOMINIO DI QUESTO \_ \_ TIPO**
</dt> <dd> <dl> <dt>

1355 (0x54B)
</dt> <dt>



Il dominio specificato non esiste o non è stato possibile contattarci.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**IL \_ DOMINIO DI ERRORE \_ ESISTE**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



Il dominio specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**LIMITE \_ DI DOMINIO DI ERRORE \_ \_ SUPERATO**
</dt> <dd> <dl> <dt>

1357 (0x54D)
</dt> <dt>



È stato effettuato un tentativo di superare il limite per il numero di domini per server.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERRORE \_ INTERNO \_ DEL \_ DATABASE**
</dt> <dd> <dl> <dt>

1358 (0x54E)
</dt> <dt>



Impossibile completare l'operazione richiesta a causa di un errore irreversibile del supporto o di un danneggiamento della struttura dei dati sul disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERRORE \_ INTERNO \_**
</dt> <dd> <dl> <dt>

1359 (0x54F)
</dt> <dt>



An internal error occurred.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERRORE \_ GENERICO \_ NON \_ MAPPATO**
</dt> <dd> <dl> <dt>

1360 (0x550)
</dt> <dt>



I tipi di accesso generici erano contenuti in una maschera di accesso che deve essere già mappata a tipi non generici.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERRORE \_ FORMATO \_ DESCRITTORE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1361 (0x551)
</dt> <dt>



Un descrittore di sicurezza non è nel formato corretto (assoluto o self-relative).


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERRORE \_ NON PROCESSO DI \_ \_ ACCESSO**
</dt> <dd> <dl> <dt>

1362 (0x552)
</dt> <dt>



L'azione richiesta è limitata per l'uso solo da parte dei processi di accesso. Il processo chiamante non è stato registrato come processo di accesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERRORE \_ DURANTE \_ L'ACCESSO ALLA \_ SESSIONE ESISTENTE**
</dt> <dd> <dl> <dt>

1363 (0x553)
</dt> <dt>



Impossibile avviare una nuova sessione di accesso con un ID già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERRORE \_ NESSUN PACCHETTO DI QUESTO \_ \_ TIPO**
</dt> <dd> <dl> <dt>

1364 (0x554)
</dt> <dt>



Un pacchetto di autenticazione specificato è sconosciuto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERRORE \_ DI STATO SESSIONE DI ACCESSO NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1365 (0x555)
</dt> <dt>



La sessione di accesso non è in uno stato coerente con l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERRORE DI \_ \_ COLLISIONE DELLA SESSIONE DI \_ ACCESSO**
</dt> <dd> <dl> <dt>

1366 (0x556)
</dt> <dt>



L'ID sessione di accesso è già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERRORE \_ TIPO DI ACCESSO NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1367 (0x557)
</dt> <dt>



Una richiesta di accesso conteneva un valore di tipo di accesso non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**IMPOSSIBILE \_ RAPPRESENTARE \_ L'ERRORE**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



Non è possibile rappresentare usando un named pipe finché i dati non vengono letti da tale pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERRORE \_ RXACT \_ STATO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1369 (0x559)
</dt> <dt>



Lo stato della transazione di un sottoalbero del Registro di sistema non è compatibile con l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERRORE \_ DI COMMIT RXACT \_ \_**
</dt> <dd> <dl> <dt>

1370 (0x55A)
</dt> <dt>



È stato rilevato un danneggiamento del database di sicurezza interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ACCOUNT \_ SPECIALE \_ ERRORE**
</dt> <dd> <dl> <dt>

1371 (0x55B)
</dt> <dt>



Impossibile eseguire questa operazione sugli account predefiniti.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERRORE \_ GRUPPO \_ SPECIALE**
</dt> <dd> <dl> <dt>

1372 (0x55C)
</dt> <dt>



Impossibile eseguire questa operazione su questo gruppo speciale predefinito.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERRORE \_ UTENTE \_ SPECIALE**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



Impossibile eseguire questa operazione su questo utente speciale incorporato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**GRUPPO \_ PRIMARIO MEMBRI \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



L'utente non può essere rimosso da un gruppo perché il gruppo è attualmente il gruppo primario dell'utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**\_TOKEN DI ERRORE GIÀ IN \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

1375 (0x55F)
</dt> <dt>



Il token è già in uso come token primario.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERRORE \_ NESSUN ALIAS DI QUESTO \_ \_ TIPO**
</dt> <dd> <dl> <dt>

1376 (0x560)
</dt> <dt>



Il gruppo locale specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**MEMBRO \_ DI ERRORE NON IN \_ \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



Il nome dell'account specificato non è un membro del gruppo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**MEMBRO \_ DI ERRORE \_ \_ NELL'ALIAS**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



Il nome dell'account specificato è già membro del gruppo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ALIAS \_ DI \_ ERRORE ESISTENTE**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



Il gruppo locale specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERRORE \_ DI ACCESSO NON \_ \_ CONCESSO**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



Errore di accesso: all'utente non è stato concesso il tipo di accesso richiesto in questo computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERRORE \_ TROPPI \_ \_ SEGRETI**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



È stato superato il numero massimo di segreti che possono essere archiviati in un singolo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**SEGRETO \_ ERRORE \_ TROPPO \_ LUNGO**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



La lunghezza di un segreto supera la lunghezza massima consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERRORE \_ INTERNO \_ DEL \_ DATABASE**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



Il database dell'autorità di sicurezza locale contiene un'incoerenza interna.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERRORE \_ TROPPI ID DI \_ \_ \_ CONTESTO**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



Durante un tentativo di accesso, il contesto di sicurezza dell'utente ha accumulato troppi ID di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**TIPO \_ DI ACCESSO ERRORE NON \_ \_ \_ CONCESSO**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



Errore di accesso: all'utente non è stato concesso il tipo di accesso richiesto in questo computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERRORE \_ NT CROSS ENCRYPTION \_ \_ \_ REQUIRED**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



Per modificare una password utente, è necessaria una password cross-encrypted.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERRORE \_ NESSUN MEMBRO DI QUESTO \_ \_ TIPO**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



Impossibile aggiungere o rimuovere un membro dal gruppo locale perché il membro non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERRORE \_ MEMBRO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



Non è stato possibile aggiungere un nuovo membro a un gruppo locale perché il tipo di account è errato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERRORE \_ TROPPI \_ \_ SID**
</dt> <dd> <dl> <dt>

1389 (0x56D)
</dt> <dt>



Sono stati specificati troppi ID di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERRORE \_ DI CRITTOGRAFIA INCROCIATA LM \_ \_ \_ RICHIESTA**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



Per modificare la password utente, è necessaria una password cross-encrypted.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERRORE \_ NESSUNA \_ EREDITARIETÀ**
</dt> <dd> <dl> <dt>

1391 (0x56F)
</dt> <dt>



Indica che un elenco di controllo di accesso non contiene componenti ereditabili.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**FILE \_ DI ERRORE \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



Il file o la directory è danneggiato e illeggibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERRORE \_ DEL DISCO \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



La struttura del disco è danneggiata e illeggibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERRORE \_ NESSUNA CHIAVE DI SESSIONE \_ \_ \_ UTENTE**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



Non esiste alcuna chiave di sessione utente per la sessione di accesso specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**QUOTA \_ DI LICENZA DI ERRORE \_ \_ SUPERATA**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



The service being accessed is licensed for a particular number of connections. Non è possibile eseguire altre connessioni al servizio in questo momento perché sono già presenti tutte le connessioni che il servizio può accettare.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERRORE \_ NOME \_ DESTINAZIONE \_ ERRATO**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



Il nome dell'account di destinazione non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERRORE \_ DI AUTENTICAZIONE \_ \_ RECIPROCA NON RIUSCITA**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



Autenticazione reciproca non riuscita. La password del server non è aggiornata nel controller di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**A \_ \_ INCLINAZIONE DELL'ORA DEGLI ERRORI**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



Esiste una differenza di ora e/o data tra il client e il server.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERRORE \_ DOMINIO CORRENTE NON \_ \_ \_ CONSENTITO**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



Questa operazione non può essere eseguita nel dominio corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERRORE HANDLE \_ \_ DI FINESTRA NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



Handle di finestra non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERRORE HANDLE \_ \_ DI MENU NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



Handle di menu non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERRORE HANDLE \_ \_ DI \_ CURSORE NON VALIDO**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



Handle di cursore non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERRORE \_ HANDLE \_ ACCEL NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



Handle di tabella dei tasti di scelta rapida non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERRORE \_ HANDLE HOOK NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1404 (0x57C)
</dt> <dt>



Handle hook non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERRORE \_ HANDLE \_ DWP NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



Handle non valido per una struttura di posizione a più finestre.


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERRORE \_ TLW \_ CON \_ WSCHILD**
</dt> <dd> <dl> <dt>

1406 (0x57E)
</dt> <dt>



Impossibile creare una finestra figlio di primo livello.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**IMPOSSIBILE \_ TROVARE LA CLASSE \_ \_ \_ WND**
</dt> <dd> <dl> <dt>

1407 (0x57F)
</dt> <dt>



Impossibile trovare la classe della finestra.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**FINESTRA \_ DI ERRORE DI UN ALTRO \_ \_ \_ THREAD**
</dt> <dd> <dl> <dt>

1408 (0x580)
</dt> <dt>



Finestra non valida. appartiene ad altri thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**TASTO \_ DI SCELTA RAPIDA DI ERRORE GIÀ \_ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

1409 (0x581)
</dt> <dt>



Il tasto di scelta rapida è già registrato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**LA \_ CLASSE ERROR ESISTE \_ \_ GIÀ**
</dt> <dd> <dl> <dt>

1410 (0x582)
</dt> <dt>



La classe esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**LA \_ CLASSE ERROR NON \_ \_ \_ ESISTE**
</dt> <dd> <dl> <dt>

1411 (0x583)
</dt> <dt>



La classe non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**LA CLASSE \_ ERROR \_ INCLUDE \_ WINDOWS**
</dt> <dd> <dl> <dt>

1412 (0x584)
</dt> <dt>



La classe ha ancora finestre aperte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERRORE \_ INDICE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1413 (0x585)
</dt> <dt>



Indice non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERRORE \_ HANDLE ICONA NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

1414 (0x586)
</dt> <dt>



Handle icona non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**INDICE \_ DELLA FINESTRA DI DIALOGO PRIVATA DEGLI \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

1415 (0x587)
</dt> <dt>



Uso di parole della finestra DIALOG private.


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ID \_ ELENCO ERRORI NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

1416 (0x588)
</dt> <dt>



L'identificatore della casella di riepilogo non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERRORE \_ NESSUN \_ CARATTERE \_ JOLLY**
</dt> <dd> <dl> <dt>

1417 (0x589)
</dt> <dt>



Non sono stati trovati caratteri jolly.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**GLI \_ APPUNTI DEGLI ERRORI NON SONO \_ \_ APERTI**
</dt> <dd> <dl> <dt>

1418 (0x58A)
</dt> <dt>



Il thread non ha gli Appunti aperti.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**TASTO \_ DI SCELTA RAPIDA ERRORE NON \_ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

1419 (0x58B)
</dt> <dt>



Il tasto di scelta rapida non è registrato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**FINESTRA DI \_ ERRORE NON FINESTRA DI \_ \_ DIALOGO**
</dt> <dd> <dl> <dt>

1420 (0x58C)
</dt> <dt>



La finestra non è una finestra di dialogo valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ID \_ CONTROLLO ERRORI NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

1421 (0x58D)
</dt> <dt>



ID controllo non trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERRORE \_ MESSAGGIO \_ COMBOBOX NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1422 (0x58E)
</dt> <dt>



Messaggio non valido per una casella combinata perché non dispone di un controllo di modifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**FINESTRA \_ DI ERRORE NON \_ \_ COMBOBOX**
</dt> <dd> <dl> <dt>

1423 (0x58F)
</dt> <dt>



La finestra non è una casella combinata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERRORE - \_ ALTEZZA DI MODIFICA NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

1424 (0x590)
</dt> <dt>



L'altezza deve essere minore di 256.


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERRORE \_ CONTROLLER DI DOMINIO NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

1425 (0x591)
</dt> <dt>



Handle del contesto di dispositivo (DC) non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERRORE \_ FILTRO HOOK NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1426 (0x592)
</dt> <dt>



Tipo di routine hook non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERRORE \_ PROCEDURA FILTRO NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

1427 (0x593)
</dt> <dt>



Procedura hook non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**\_L'HOOK DI ERRORE RICHIEDE \_ \_ HMOD**
</dt> <dd> <dl> <dt>

1428 (0x594)
</dt> <dt>



Impossibile impostare hook non locali senza un handle di modulo.


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERRORE \_ HOOK \_ SOLO \_ GLOBALE**
</dt> <dd> <dl> <dt>

1429 (0x595)
</dt> <dt>



Questa procedura hook può essere impostata solo a livello globale.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**ERROR \_ JOURNAL \_ HOOK \_ SET**
</dt> <dd> <dl> <dt>

1430 (0x596)
</dt> <dt>



La procedura hook journal è già installata.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**HOOK \_ DEGLI ERRORI NON \_ \_ INSTALLATO**
</dt> <dd> <dl> <dt>

1431 (0x597)
</dt> <dt>



La procedura hook non è installata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERRORE \_ MESSAGGIO \_ LB NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1432 (0x598)
</dt> <dt>



Messaggio non valido per la casella di riepilogo a selezione singola.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR \_ SETCOUNT \_ ON \_ BAD \_ LB**
</dt> <dd> <dl> <dt>

1433 (0x599)
</dt> <dt>



LB \_ SETCOUNT inviato alla casella di riepilogo non differita.


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERRORE \_ LB \_ SENZA \_ TABULAZIONITOPS**
</dt> <dd> <dl> <dt>

1434 (0x59A)
</dt> <dt>



Questa casella di riepilogo non supporta i tabulazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERRORE DURANTE \_ \_ L'ELIMINAZIONE \_ \_ DELL'OGGETTO DI UN ALTRO \_ THREAD**
</dt> <dd> <dl> <dt>

1435 (0x59B)
</dt> <dt>



Impossibile eliminare l'oggetto creato da un altro thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_MENU FINESTRA FIGLIO \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

1436 (0x59C)
</dt> <dt>



Le finestre figlio non possono avere menu.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERRORE \_ NESSUN MENU DI \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

1437 (0x59D)
</dt> <dt>



La finestra non dispone di un menu di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERRORE \_ STILE \_ MSGBOX \_ NON VALIDO**
</dt> <dd> <dl> <dt>

1438 (0x59E)
</dt> <dt>



Stile della finestra di messaggio non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERRORE \_ - VALORE SPI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1439 (0x59F)
</dt> <dt>



Parametro SPI (System-Wide) \_ \* non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**SCHERMATA \_ DI ERRORE GIÀ \_ \_ BLOCCATA**
</dt> <dd> <dl> <dt>

1440 (0x5A0)
</dt> <dt>



Schermata già bloccata.


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**GLI \_ HWND DI \_ ERRORE HANNO UN ELEMENTO PADRE \_ DIFF \_**
</dt> <dd> <dl> <dt>

1441 (0x5A1)
</dt> <dt>



Tutti gli handle delle finestre in una struttura di posizione a più finestre devono avere lo stesso elemento padre.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**FINESTRA \_ DI ERRORE NON \_ \_ FIGLIO**
</dt> <dd> <dl> <dt>

1442 (0x5A2)
</dt> <dt>



La finestra non è una finestra figlio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERRORE \_ COMANDO \_ GW NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1443 (0x5A3)
</dt> <dt>



Comando GW non \_ \* valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERRORE ID \_ \_ THREAD NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1444 (0x5A4)
</dt> <dt>



Identificatore di thread non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**FINESTRA \_ DI ERRORE NON \_ \_ MDICHILD**
</dt> <dd> <dl> <dt>

1445 (0x5A5)
</dt> <dt>



Impossibile elaborare un messaggio da una finestra che non è una finestra dell'interfaccia a documenti multipli (MDI).


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**POPUP \_ DI ERRORE GIÀ \_ \_ ATTIVO**
</dt> <dd> <dl> <dt>

1446 (0x5A6)
</dt> <dt>



Menu popup già attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERRORE \_ NESSUNA BARRA DI \_ SCORRIMENTO**
</dt> <dd> <dl> <dt>

1447 (0x5A7)
</dt> <dt>



La finestra non dispone di barre di scorrimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERRORE INTERVALLO \_ BARRA \_ DI SCORRIMENTO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1448 (0x5A8)
</dt> <dt>



L'intervallo della barra di scorrimento non può essere maggiore di MAXLONG.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERRORE: \_ COMANDO \_ SHOWWIN NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1449 (0x5A9)
</dt> <dt>



Impossibile visualizzare o rimuovere la finestra nel modo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERRORE \_ NESSUNA RISORSA DI \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

1450 (0x5AA)
</dt> <dt>



Risorse di sistema insufficienti per completare il servizio richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERRORE \_ RISORSE DI SISTEMA NON DI \_ \_ PAGINA**
</dt> <dd> <dl> <dt>

1451 (0x5AB)
</dt> <dt>



Risorse di sistema insufficienti per completare il servizio richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**RISORSE \_ DI SISTEMA DI CUI È STATO \_ PAGINATO L'ERRORE \_**
</dt> <dd> <dl> <dt>

1452 (0x5AC)
</dt> <dt>



Risorse di sistema insufficienti per completare il servizio richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERRORE NELLA \_ QUOTA \_ DEL WORKING \_ SET**
</dt> <dd> <dl> <dt>

1453 (0x5AD)
</dt> <dt>



Quota insufficiente per completare il servizio richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERRORE \_ PAGEFILE \_ QUOTA**
</dt> <dd> <dl> <dt>

1454 (0x5AE)
</dt> <dt>



Quota insufficiente per completare il servizio richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**LIMITE \_ IMPEGNO \_ ERRORI**
</dt> <dd> <dl> <dt>

1455 (0x5AF)
</dt> <dt>



Il file di paging è troppo piccolo per il completamento dell'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**VOCE \_ DI MENU ERRORE NON \_ \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

1456 (0x5B0)
</dt> <dt>



Non è stata trovata una voce di menu.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERRORE HANDLE \_ DI \_ TASTIERA NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1457 (0x5B1)
</dt> <dt>



Handle di layout di tastiera non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**TIPO \_ HOOK DI ERRORE NON \_ \_ \_ CONSENTITO**
</dt> <dd> <dl> <dt>

1458 (0x5B2)
</dt> <dt>



Tipo hook non consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**\_L'ERRORE \_ RICHIEDE \_ WINDOWSTATION INTERATTIVO**
</dt> <dd> <dl> <dt>

1459 (0x5B3)
</dt> <dt>



Questa operazione richiede una stazione finestra interattiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**TIMEOUT \_ ERRORE**
</dt> <dd> <dl> <dt>

1460 (0x5B4)
</dt> <dt>



Questa operazione ha restituito perché il periodo di timeout è scaduto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERRORE HANDLE \_ DI \_ MONITORAGGIO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1461 (0x5B5)
</dt> <dt>



Handle di monitoraggio non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**DIMENSIONI \_ NON CORRETTE \_ DELL'ERRORE**
</dt> <dd> <dl> <dt>

1462 (0x5B6)
</dt> <dt>



Argomento di dimensione non corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**CLASSE \_ ERROR SYMLINK \_ \_ DISABILITATA**
</dt> <dd> <dl> <dt>

1463 (0x5B7)
</dt> <dt>



Il collegamento simbolico non può essere seguito perché il tipo è disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERRORE \_ SYMLINK \_ NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

1464 (0x5B8)
</dt> <dt>



Questa applicazione non supporta l'operazione corrente sui collegamenti simbolici.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERRORE \_ DI ANALISI \_ \_ XML**
</dt> <dd> <dl> <dt>

1465 (0x5B9)
</dt> <dt>



Windows impossibile analizzare i dati XML richiesti.


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERRORE \_ XMLDSIG \_ ERROR**
</dt> <dd> <dl> <dt>

1466 (0x5BA)
</dt> <dt>



Si è verificato un errore durante l'elaborazione di una firma digitale XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERRORE DURANTE \_ IL RIAVVIO \_ DELL'APPLICAZIONE**
</dt> <dd> <dl> <dt>

1467 (0x5BB)
</dt> <dt>



Questa applicazione deve essere riavviata.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERRORE \_ RAGGRUPPAMENTO \_ ERRATO**
</dt> <dd> <dl> <dt>

1468 (0x5BC)
</dt> <dt>



Il chiamante ha effettuato la richiesta di connessione nel raggruppamento di routing errato.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERRORE \_ DI AUTENTICAZIONE \_**
</dt> <dd> <dl> <dt>

1469 (0x5BD)
</dt> <dt>



Si è verificato un errore AuthIP durante il tentativo di connessione all'host remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERRORE \_ NESSUNA \_ RISORSA \_ NVRAM**
</dt> <dd> <dl> <dt>

1470 (0x5BE)
</dt> <dt>



Risorse NVRAM insufficienti per completare il servizio richiesto. Potrebbe essere necessario riavviare il computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERRORE \_ NON \_ PROCESSO \_ GUI**
</dt> <dd> <dl> <dt>

1471 (0x5BF)
</dt> <dt>



Impossibile completare l'operazione richiesta perché il processo specificato non è un processo GUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERRORE \_ FILE EVENTLOG \_ \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

1500 (0x5DC)
</dt> <dt>



Il file di log eventi è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERRORE \_ EVENTLOG \_ CANT \_ START**
</dt> <dd> <dl> <dt>

1501 (0x5DD)
</dt> <dt>



Non è stato possibile aprire alcun file di registro eventi, quindi il servizio di registrazione eventi non è stato avviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**FILE \_ DI LOG DEGLI ERRORI \_ \_ PIENO**
</dt> <dd> <dl> <dt>

1502 (0x5DE)
</dt> <dt>



Il file del registro eventi è pieno.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**FILE \_ EVENTLOG \_ DEGLI ERRORI \_ MODIFICATO**
</dt> <dd> <dl> <dt>

1503 (0x5DF)
</dt> <dt>



Il file di log eventi è stato modificato tra le operazioni di lettura.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERRORE \_ NOME ATTIVITÀ NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



Il nome dell'attività specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERRORE INDICE \_ ATTIVITÀ \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



L'indice dell'attività specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**THREAD \_ DI ERRORE GIÀ IN \_ \_ \_ ATTIVITÀ**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



Il thread specificato sta già partecipando a un'attività.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DEL \_ SERVIZIO**
</dt> <dd> <dl> <dt>

1601 (0x641)
</dt> <dt>



Impossibile accedere Windows del programma di installazione. Ciò può verificarsi se il Windows di installazione non è installato correttamente. Per assistenza, contattare il personale di supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERRORE \_ DURANTE \_ L'INSTALLAZIONE DI USEREXIT**
</dt> <dd> <dl> <dt>

1602 (0x642)
</dt> <dt>



Installazione annullata dall'utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE**
</dt> <dd> <dl> <dt>

1603 (0x643)
</dt> <dt>



Errore irreversibile durante l'installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERRORE DURANTE LA \_ SOSPENSIONE \_ DELL'INSTALLAZIONE**
</dt> <dd> <dl> <dt>

1604 (0x644)
</dt> <dt>



Installazione sospesa, incompleta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERRORE \_ PRODOTTO \_ SCONOSCIUTO**
</dt> <dd> <dl> <dt>

1605 (0x645)
</dt> <dt>



Questa azione è valida solo per i prodotti attualmente installati.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**FUNZIONALITÀ \_ DI ERRORE \_ SCONOSCIUTA**
</dt> <dd> <dl> <dt>

1606 (0x646)
</dt> <dt>



ID funzionalità non registrato.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERRORE \_ COMPONENTE \_ SCONOSCIUTO**
</dt> <dd> <dl> <dt>

1607 (0x647)
</dt> <dt>



ID componente non registrato.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**PROPRIETÀ \_ ERROR UNKNOWN \_**
</dt> <dd> <dl> <dt>

1608 (0x648)
</dt> <dt>



Proprietà sconosciuta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERRORE \_ STATO HANDLE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1609 (0x649)
</dt> <dt>



L'handle è in uno stato non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERRORE \_ CONFIGURAZIONE \_ NON VALIDA**
</dt> <dd> <dl> <dt>

1610 (0x64A)
</dt> <dt>



I dati di configurazione per questo prodotto sono danneggiati. Contattare il personale di supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**INDICE \_ DEGLI ERRORI \_ ASSENTE**
</dt> <dd> <dl> <dt>

1611 (0x64B)
</dt> <dt>



Qualificatore del componente non presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DELL'ORIGINE \_ ASSENTE**
</dt> <dd> <dl> <dt>

1612 (0x64C)
</dt> <dt>



L'origine di installazione per questo prodotto non è disponibile. Verificare che l'origine esista e che sia possibile accedervi.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DELLA VERSIONE DEL \_ PACCHETTO**
</dt> <dd> <dl> <dt>

1613 (0x64D)
</dt> <dt>



Questo pacchetto di installazione non può essere installato dal Windows installer. È necessario installare un Windows service pack che contiene una versione più recente del servizio Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERRORE \_ PRODOTTO \_ DISINSTALLATO**
</dt> <dd> <dl> <dt>

1614 (0x64E)
</dt> <dt>



Il prodotto viene disinstallato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**SINTASSI \_ DI \_ QUERY NON \_ VALIDA**
</dt> <dd> <dl> <dt>

1615 (0x64F)
</dt> <dt>



SQL sintassi di query non valida o non supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERRORE \_ CAMPO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1616 (0x650)
</dt> <dt>



Il campo record non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**DISPOSITIVO \_ DI ERRORE \_ RIMOSSO**
</dt> <dd> <dl> <dt>

1617 (0x651)
</dt> <dt>



Il dispositivo è stato rimosso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE GIÀ \_ IN ESECUZIONE**
</dt> <dd> <dl> <dt>

1618 (0x652)
</dt> <dt>



È già in corso un'altra installazione. Completare l'installazione prima di procedere con questa installazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERRORE DURANTE \_ \_ L'APERTURA DEL PACCHETTO DI INSTALLAZIONE NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

1619 (0x653)
</dt> <dt>



Impossibile aprire questo pacchetto di installazione. Verificare che il pacchetto esista e che sia possibile accedervi oppure contattare il fornitore dell'applicazione per verificare che si tratta di un pacchetto Windows Installer valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERRORE \_ DURANTE \_ L'INSTALLAZIONE DEL PACCHETTO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1620 (0x654)
</dt> <dt>



Impossibile aprire questo pacchetto di installazione. Contattare il fornitore dell'applicazione per verificare che si tratta di un pacchetto Windows installer valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERRORE DURANTE \_ L'INSTALLAZIONE \_ DELL'INTERFACCIA \_ UTENTE**
</dt> <dd> <dl> <dt>

1621 (0x655)
</dt> <dt>



Si è verificato un errore durante l'avvio dell'Windows utente del servizio Installazione applicazioni. Contattare il personale di supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE DEL \_ LOG**
</dt> <dd> <dl> <dt>

1622 (0x656)
</dt> <dt>



Errore durante l'apertura del file di log di installazione. Verificare che il percorso del file di log specificato esista e che sia possibile scrivervi.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERRORE \_ DURANTE \_ L'INSTALLAZIONE \_ DEL LINGUAGGIO NON SUPPORTATO**
</dt> <dd> <dl> <dt>

1623 (0x657)
</dt> <dt>



La lingua di questo pacchetto di installazione non è supportata dal sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERRORE DURANTE \_ L'INSTALLAZIONE \_ DELLA \_ TRASFORMAZIONE**
</dt> <dd> <dl> <dt>

1624 (0x658)
</dt> <dt>



Errore durante l'applicazione delle trasformazioni. Verificare che i percorsi di trasformazione specificati siano validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERRORE \_ DURANTE \_ L'INSTALLAZIONE \_ DEL PACCHETTO RIFIUTATO**
</dt> <dd> <dl> <dt>

1625 (0x659)
</dt> <dt>



Questa installazione non è consentita dai criteri di sistema. Contattare l'amministratore del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**FUNZIONE \_ ERROR \_ NON \_ CHIAMATA**
</dt> <dd> <dl> <dt>

1626 (0x65A)
</dt> <dt>



Impossibile eseguire la funzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**FUNZIONE \_ ERROR \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

1627 (0x65B)
</dt> <dt>



Funzione non riuscita durante l'esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERRORE \_ TABELLA NON \_ VALIDA**
</dt> <dd> <dl> <dt>

1628 (0x65C)
</dt> <dt>



Specificata tabella non valida o sconosciuta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**TIPO \_ DI DATI DI ERRORE NON \_ CORRISPONDENTE**
</dt> <dd> <dl> <dt>

1629 (0x65D)
</dt> <dt>



I dati forniti sono di tipo errato.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**TIPO \_ DI ERRORE NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

1630 (0x65E)
</dt> <dt>



I dati di questo tipo non sono supportati.


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERRORE \_ DURANTE LA CREAZIONE NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

1631 (0x65F)
</dt> <dt>



Impossibile avviare Windows del programma di installazione. Contattare il personale di supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERRORE \_ DURANTE \_ L'INSTALLAZIONE DI TEMP \_ UNWRITABLE**
</dt> <dd> <dl> <dt>

1632 (0x660)
</dt> <dt>



La cartella Temp si trova in un'unità piena o inaccessibile. Liberare spazio nell'unità o verificare di disporre dell'autorizzazione di scrittura per la cartella Temp.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERRORE \_ DURANTE \_ L'INSTALLAZIONE \_ DELLA PIATTAFORMA NON SUPPORTATA**
</dt> <dd> <dl> <dt>

1633 (0x661)
</dt> <dt>



Questo pacchetto di installazione non è supportato da questo tipo di processore. Contattare il fornitore del prodotto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERRORE \_ DURANTE \_ L'INSTALLAZIONE NON IN USO**
</dt> <dd> <dl> <dt>

1634 (0x662)
</dt> <dt>



Componente non usato in questo computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**\_L'APERTURA DEL PACCHETTO DI PATCH DEGLI ERRORI NON È \_ \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

1635 (0x663)
</dt> <dt>



Impossibile aprire questo pacchetto di aggiornamento. Verificare che il pacchetto di aggiornamento esista e che sia possibile accedervi oppure contattare il fornitore dell'applicazione per verificare che si tratta di un pacchetto di aggiornamento Windows installer valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**PACCHETTO \_ DI PATCH DEGLI ERRORI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1636 (0x664)
</dt> <dt>



Impossibile aprire questo pacchetto di aggiornamento. Contattare il fornitore dell'applicazione per verificare che si tratta di un pacchetto di aggiornamento Windows installer valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**PACCHETTO \_ DI PATCH DEGLI ERRORI NON \_ \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

1637 (0x665)
</dt> <dt>



Questo pacchetto di aggiornamento non può essere elaborato dal Windows installer. È necessario installare un Windows Service Pack che contiene una versione più recente del servizio Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERRORE \_ VERSIONE \_ DEL PRODOTTO**
</dt> <dd> <dl> <dt>

1638 (0x666)
</dt> <dt>



Un'altra versione di questo prodotto è già installata. Non è possibile continuare l'installazione di questa versione. Per configurare o rimuovere la versione esistente di questo prodotto, usare Installazione applicazioni nel Pannello di controllo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERRORE \_ DELLA RIGA DI COMANDO NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

1639 (0x667)
</dt> <dt>



Argomento della riga di comando non valido. Per informazioni dettagliate sulla riga di comando, vedere Windows Installer SDK.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERRORE \_ DURANTE \_ \_ L'INSTALLAZIONE REMOTA NON CONSENTITA**
</dt> <dd> <dl> <dt>

1640 (0x668)
</dt> <dt>



Solo gli amministratori hanno l'autorizzazione per aggiungere, rimuovere o configurare il software server durante una sessione remota di Servizi terminal. Per installare o configurare il software nel server, contattare l'amministratore di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**AVVIO \_ DEL \_ RIAVVIO CON ESITO POSITIVO \_ DELL'ERRORE**
</dt> <dd> <dl> <dt>

1641 (0x669)
</dt> <dt>



L'operazione richiesta è stata completata correttamente. Il sistema verrà riavviato in modo che le modifiche possano essere applicate.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**DESTINAZIONE \_ DELLA PATCH DI ERRORE NON \_ \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

1642 (0x66A)
</dt> <dt>



L'aggiornamento non può essere installato dal servizio Windows Installer perché il programma da aggiornare potrebbe non essere presente oppure è possibile che l'aggiornamento aggiornerà una versione diversa del programma. Verificare che il programma da aggiornare esista nel computer e che l'aggiornamento sia corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**PACCHETTO \_ PATCH DI ERRORE \_ \_ RIFIUTATO**
</dt> <dd> <dl> <dt>

1643 (0x66B)
</dt> <dt>



Il pacchetto di aggiornamento non è consentito dai criteri di restrizione software.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE \_ DELLA TRASFORMAZIONE RIFIUTATA**
</dt> <dd> <dl> <dt>

1644 (0x66C)
</dt> <dt>



Una o più personalizzazioni non sono consentite dai criteri di restrizione software.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE \_ REMOTA NON CONSENTITA**
</dt> <dd> <dl> <dt>

1645 (0x66D)
</dt> <dt>



Il Windows non consente l'installazione da un Connessione Desktop remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**RIMOZIONE \_ DELLA PATCH DI ERRORE NON \_ \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

1646 (0x66E)
</dt> <dt>



La disinstallazione del pacchetto di aggiornamento non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERRORE \_ PATCH \_ SCONOSCIUTA**
</dt> <dd> <dl> <dt>

1647 (0x66F)
</dt> <dt>



L'aggiornamento non viene applicato a questo prodotto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERRORE \_ PATCH \_ NESSUNA \_ SEQUENZA**
</dt> <dd> <dl> <dt>

1648 (0x670)
</dt> <dt>



Non è stata trovata alcuna sequenza valida per il set di aggiornamenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**RIMOZIONE \_ PATCH DI ERRORE NON \_ \_ CONSENTITA**
</dt> <dd> <dl> <dt>

1649 (0x671)
</dt> <dt>



La rimozione degli aggiornamenti non è consentita dai criteri.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERRORE XML \_ \_ PATCH NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1650 (0x672)
</dt> <dt>



I dati di aggiornamento XML non sono validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**PATCH \_ DEGLI ERRORI PRODOTTO ANNUNCIATO \_ \_ \_ GESTITO**
</dt> <dd> <dl> <dt>

1651 (0x673)
</dt> <dt>



Windows Il programma di installazione non consente l'aggiornamento dei prodotti annunciati gestiti. Prima di applicare l'aggiornamento, è necessario installare almeno una funzionalità del prodotto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERRORE DURANTE \_ \_ L'INSTALLAZIONE \_ DI SAFEBOOT DEL SERVIZIO**
</dt> <dd> <dl> <dt>

1652 (0x674)
</dt> <dt>



Il Windows Installer non è accessibile in modalità Cassaforte predefinita. Riprovare quando il computer non è in modalità Cassaforte oppure è possibile usare Ripristino configurazione di sistema per riportare il computer a uno stato valido precedente.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR \_ FAIL \_ FAST \_ EXCEPTION**
</dt> <dd> <dl> <dt>

1653 (0x675)
</dt> <dt>



Si è verificata un'eccezione rapida di errore. I gestori di eccezioni non verranno richiamati e il processo verrà terminato immediatamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERRORE \_ DURANTE \_ L'INSTALLAZIONE RIFIUTATA**
</dt> <dd> <dl> <dt>

1654 (0x676)
</dt> <dt>



L'app che si sta tentando di eseguire non è supportata in questa versione di Windows.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winerror</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore di sistema](system-error-codes.md)
</dt> </dl>

 

 




