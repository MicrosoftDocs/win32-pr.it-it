---
description: Il Windows di sicurezza consente di controllare l'accesso agli oggetti evento, mutex, semaforo e timer waitable. Le code timer, le variabili interlock e gli oggetti sezione critica non sono a protezione diretta. Per altre informazioni, vedere Access-Control modello.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Sicurezza degli oggetti di sincronizzazione e diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85ca76002a92e305983ab97d46dfde2f36f9ae49a779e091a072d3090ceb976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739291"
---
# <a name="synchronization-object-security-and-access-rights"></a>Sicurezza degli oggetti di sincronizzazione e diritti di accesso

Il Windows di sicurezza consente di controllare l'accesso agli oggetti evento, mutex, semaforo e timer waitable. Le code timer, le variabili interlock e gli oggetti sezione critica non sono a protezione diretta. Per altre informazioni, vedere [Modello di controllo di accesso](../secauthz/access-control-model.md).

È possibile [specificare un](../secauthz/security-descriptors.md) descrittore di sicurezza per un oggetto di sincronizzazione interprocesso quando si chiama la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) Se si specifica **NULL,** l'oggetto ottiene un descrittore di sicurezza predefinito. Gli [elenchi di controllo di accesso (ACL)](../secauthz/access-control-lists.md) nel descrittore di sicurezza predefinito per un oggetto di sincronizzazione provengono dal token di rappresentazione o primario dell'autore.

Per ottenere o impostare il descrittore di sicurezza di un evento, mutex, semaforo o oggetto timer waitable, chiamare le funzioni [**GetNamedSecurityInfo,**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) [**SetNamedSecurityInfo,**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)o [**SetSecurityInfo.**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo)

Gli handle restituiti da [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)e [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) hanno accesso completo al nuovo oggetto. Quando si chiamano le funzioni [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)e [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto.

I diritti di accesso validi per gli oggetti di sincronizzazione interprocesso includono i diritti di accesso [standard](../secauthz/standard-access-rights.md) e alcuni diritti di accesso specifici degli oggetti. Nella tabella seguente sono elencati i diritti di accesso standard usati da tutti gli oggetti.

| Valore                           | Significato                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DELETE** (0x00010000L)        | Obbligatorio per eliminare l'oggetto.                                                                                                                                                                                                                                                           |
| **LETTURA \_ CONTROL** (0x00020000L) | Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, senza includere le informazioni nel SACL. Per leggere o scrivere il SACL, è necessario richiedere il diritto **di accesso ACCESS SYSTEM \_ \_ SECURITY.** Per altre informazioni, vedere [Diritto di accesso SACL.](../secauthz/sacl-access-right.md) |
| **SYNCHRONIZE** (0x00100000L)   | Diritto di utilizzare l'oggetto per la sincronizzazione. Ciò consente a un thread di attendere finché l'oggetto non si trova nello stato segnalato.                                                                                                                                                                |
| **WRITE \_ Applicazione livello dati** (0x00040000L)    | Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                                   |
| **WRITE \_ OWNER** (0x00080000L)  | Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                                  |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto per gli oggetti evento. Questi diritti sono supportati oltre ai diritti di accesso standard.



| Valore                             | Significato                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ ALL \_ ACCESS** (0x1F0003) | Tutti i diritti di accesso possibili per un oggetto evento. Usare questo diritto solo se l'applicazione richiede l'accesso oltre a quello concesso dai diritti di accesso standard e **EVENT \_ MODIFY \_ STATE**. L'uso di questo diritto di accesso aumenta la possibilità che l'applicazione sia eseguita da un amministratore. |
| **EVENTO \_ MODIFY \_ STATE** (0x0002) | Modificare l'accesso allo stato, necessario per le [**funzioni SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent), [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) [**e PulseEvent.**](/windows/desktop/api/WinBase/nf-winbase-pulseevent)                                                                                                                                    |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto per gli oggetti mutex. Questi diritti sono supportati oltre ai diritti di accesso standard.



| Valore                             | Significato                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MUTEX \_ ALL \_ ACCESS** (0x1F0001) | Tutti i diritti di accesso possibili per un oggetto mutex. Usare questo diritto solo se l'applicazione richiede l'accesso oltre a quello concesso dai diritti di accesso standard. L'uso di questo diritto di accesso aumenta la possibilità che l'applicazione sia eseguita da un amministratore. |
| **MUTEX \_ MODIFY \_ STATE** (0x0001) | Riservato per utilizzi futuri.                                                                                                                                                                                                                                           |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto per gli oggetti semaforo. Questi diritti sono supportati oltre ai diritti di accesso standard.



| Valore                                 | Significato                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SEMAFORO \_ ALL \_ ACCESS** (0x1F0003) | Tutti i diritti di accesso possibili per un oggetto semaforo. Usare questo diritto solo se l'applicazione richiede l'accesso oltre a quello concesso dai diritti di accesso standard **e SEMAPHORE \_ MODIFY \_ STATE**. L'uso di questo diritto di accesso aumenta la possibilità che l'applicazione sia eseguita da un amministratore. |
| **SEMAFORO \_ MODIFY \_ STATE** (0x0002) | Modificare l'accesso allo stato, necessario per la [**funzione ReleaseSemaphore.**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore)                                                                                                                                                                                                   |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto per gli oggetti timer waitable. Questi diritti sono supportati oltre ai diritti di accesso standard.



| Valore                             | Significato                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TIMER \_ ALL \_ ACCESS** (0x1F0003) | Tutti i diritti di accesso possibili per un oggetto timer waitable. Usare questo diritto solo se l'applicazione richiede l'accesso oltre a quello concesso dai diritti di accesso standard e **TIMER \_ MODIFY \_ STATE**. L'uso di questo diritto di accesso aumenta la possibilità che l'applicazione sia eseguita da un amministratore. |
| **TIMER \_ MODIFY \_ STATE** (0x0002) | Modificare l'accesso allo stato, necessario per le [**funzioni SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) [**e CancelWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer)                                                                                                                                            |
| **TIMER \_ STATO \_ QUERY** (0x0001)  | Riservato per utilizzi futuri.                                                                                                                                                                                                                                                                                 |



 

Per leggere o scrivere il SACL di un oggetto di sincronizzazione interprocesso, è necessario richiedere il diritto **di accesso ACCESS SYSTEM \_ \_ SECURITY.** Per altre informazioni, vedere [Elenchi di controllo di accesso (ACL)](../secauthz/access-control-lists.md) e Diritto di accesso [SACL.](../secauthz/sacl-access-right.md)

 

 
