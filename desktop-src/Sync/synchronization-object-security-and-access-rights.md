---
description: Il modello di sicurezza di Windows consente di controllare l'accesso agli oggetti evento, mutex, semaforo e timer da attendere. Le code del timer, le variabili Interlocked e gli oggetti della sezione critica non sono entità a protezione diretta. Per ulteriori informazioni, vedere Access-Control Model.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Sicurezza e diritti di accesso degli oggetti di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c4bfdb17a6e1c4d99a3e9722e67a3b48a3c788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312752"
---
# <a name="synchronization-object-security-and-access-rights"></a>Sicurezza e diritti di accesso degli oggetti di sincronizzazione

Il modello di sicurezza di Windows consente di controllare l'accesso agli oggetti evento, mutex, semaforo e timer da attendere. Le code del timer, le variabili Interlocked e gli oggetti della sezione critica non sono entità a protezione diretta. Per altre informazioni, vedere [modello di controllo di accesso](../secauthz/access-control-model.md).

È possibile specificare un [descrittore di sicurezza](../secauthz/security-descriptors.md) per un oggetto di sincronizzazione interprocesso quando si chiama la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) . Se si specifica **null**, l'oggetto ottiene un descrittore di sicurezza predefinito. Gli [elenchi di controllo di accesso (ACL)](../secauthz/access-control-lists.md) nel descrittore di sicurezza predefinito per un oggetto di sincronizzazione provengono dal token primario o di rappresentazione del creatore.

Per ottenere o impostare il descrittore di sicurezza di un evento, un mutex, un semaforo o un oggetto timer waitable, chiamare le funzioni [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)o [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Gli handle restituiti da [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)e [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) hanno accesso completo al nuovo oggetto. Quando si chiamano le funzioni [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**errore in OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)e [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto.

I diritti di accesso validi per gli oggetti di sincronizzazione interprocesso includono i [diritti di accesso standard](../secauthz/standard-access-rights.md) e alcuni diritti di accesso specifici per gli oggetti. La tabella seguente elenca i diritti di accesso standard usati da tutti gli oggetti.

| Valore                           | Significato                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Elimina** (0x00010000L)        | Obbligatorio per eliminare l'oggetto.                                                                                                                                                                                                                                                           |
| **Leggi \_ CONTROLLO** (0x00020000L) | Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, escluse le informazioni nell'elenco SACL. Per leggere o scrivere il SACL, è necessario richiedere il diritto di accesso alla **\_ \_ sicurezza del sistema di accesso** . Per ulteriori informazioni, vedere il [diritto di accesso SACL](../secauthz/sacl-access-right.md). |
| **Sincronizza** (0x00100000L)   | Diritto di utilizzare l'oggetto per la sincronizzazione. Ciò consente a un thread di attendere fino a quando l'oggetto non è nello stato segnalato.                                                                                                                                                                |
| **Scrivi \_ Applicazione livello dati** (0x00040000L)    | Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                                   |
| **Scrivi \_ PROPRIETARIO** (0x00080000L)  | Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                                  |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto per gli oggetti evento. Questi diritti sono supportati oltre ai diritti di accesso standard.



| Valore                             | Significato                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ Tutti gli \_ accessi** (0x1F0003) | Tutti i diritti di accesso possibili per un oggetto evento. Utilizzare questo diritto solo se l'applicazione richiede l'accesso oltre a quello concesso dai diritti di accesso standard e **\_ \_ dallo stato di modifica degli eventi**. L'uso di questo diritto di accesso aumenta la possibilità che l'applicazione debba essere eseguita da un amministratore. |
| **Evento \_ MODIFICA \_ stato** (0x0002) | Modificare l'accesso allo stato, che è necessario per le funzioni [**seevent**](/windows/win32/api/synchapi/nf-synchapi-setevent), [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) e [**PulseEvent**](/windows/desktop/api/WinBase/nf-winbase-pulseevent) .                                                                                                                                    |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto per gli oggetti mutex. Questi diritti sono supportati oltre ai diritti di accesso standard.



| Valore                             | Significato                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mutex \_ Tutti gli \_ accessi** (0x1F0001) | Tutti i diritti di accesso possibili per un oggetto mutex. Utilizzare questo diritto solo se l'applicazione richiede l'accesso oltre a quello concesso dai diritti di accesso standard. L'uso di questo diritto di accesso aumenta la possibilità che l'applicazione debba essere eseguita da un amministratore. |
| **Mutex \_ MODIFICA \_ stato** (0x0001) | Riservato per utilizzi futuri.                                                                                                                                                                                                                                           |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto per gli oggetti semaforo. Questi diritti sono supportati oltre ai diritti di accesso standard.



| Valore                                 | Significato                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Semaforo \_ Tutti gli \_ accessi** (0x1F0003) | Tutti i diritti di accesso possibili per un oggetto semaforo. Usare questo diritto solo se l'applicazione richiede l'accesso oltre a quello concesso dai diritti di accesso standard e **\_ \_ dallo stato di modifica del semaforo**. L'uso di questo diritto di accesso aumenta la possibilità che l'applicazione debba essere eseguita da un amministratore. |
| **Semaforo \_ MODIFICA \_ stato** (0x0002) | Modificare l'accesso allo stato, che è necessario per la funzione [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) .                                                                                                                                                                                                   |



 

Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto per gli oggetti timer in attesa. Questi diritti sono supportati oltre ai diritti di accesso standard.



| Valore                             | Significato                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Timer \_ di Tutti gli \_ accessi** (0x1F0003) | Tutti i diritti di accesso possibili per un oggetto timer in attesa. Utilizzare questo diritto solo se l'applicazione richiede l'accesso oltre a quello concesso dai diritti di accesso standard e **\_ \_ dallo stato di modifica del timer**. L'uso di questo diritto di accesso aumenta la possibilità che l'applicazione debba essere eseguita da un amministratore. |
| **Timer \_ di MODIFICA \_ stato** (0x0002) | Modificare l'accesso allo stato, che è necessario per le funzioni [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) e [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) .                                                                                                                                            |
| **Timer \_ di \_Stato query** (0x0001)  | Riservato per utilizzi futuri.                                                                                                                                                                                                                                                                                 |



 

Per leggere o scrivere l'elenco SACL di un oggetto di sincronizzazione interprocesso, è necessario richiedere il diritto di accesso alla **\_ \_ sicurezza del sistema di accesso** . Per altre informazioni, vedere [elenchi di controllo di accesso (ACL)](../secauthz/access-control-lists.md) e [accesso SACL diritto](../secauthz/sacl-access-right.md).

 

 
