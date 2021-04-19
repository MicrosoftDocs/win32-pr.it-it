---
description: Il modello di sicurezza di Microsoft Windows consente di controllare l'accesso agli oggetti processo. Per ulteriori informazioni sulla sicurezza, vedere Access-Control Model.
ms.assetid: 8d212292-f087-41e4-884e-cec4423dac49
title: Sicurezza dell'oggetto processo e diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5207e459bab2ae444282355844401e0b82e9c
ms.sourcegitcommit: 18023a15a4312c653a8dcc0feef23e3413a7f5dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/25/2021
ms.locfileid: "106320082"
---
# <a name="job-object-security-and-access-rights"></a>Sicurezza dell'oggetto processo e diritti di accesso

Il modello di sicurezza di Microsoft Windows consente di controllare l'accesso agli oggetti processo. Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](../secauthz/access-control-model.md).

È possibile specificare un [descrittore di sicurezza](../secauthz/security-descriptors.md) per un oggetto processo quando si chiama la funzione [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Se si specifica NULL, l'oggetto processo ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per un oggetto processo provengono dal token primario o di rappresentazione del creatore.

Per ottenere o impostare il descrittore di sicurezza per un oggetto processo, chiamare la funzione [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)o [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

I diritti di accesso validi per gli oggetti processo includono i [diritti di accesso standard](../secauthz/standard-access-rights.md) e alcuni diritti di accesso specifici del processo. La tabella seguente elenca i diritti di accesso standard usati da tutti gli oggetti.

| Valore                           | Significato                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Elimina** (0x00010000L)        | Obbligatorio per eliminare l'oggetto.                                                                                                                                                                                                                                                           |
| **Leggi \_ CONTROLLO** (0x00020000L) | Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, escluse le informazioni nell'elenco SACL. Per leggere o scrivere il SACL, è necessario richiedere il diritto di accesso alla **\_ \_ sicurezza del sistema di accesso** . Per ulteriori informazioni, vedere il [diritto di accesso SACL](../secauthz/sacl-access-right.md). |
| **Sincronizza** (0x00100000L)   | Diritto di utilizzare l'oggetto per la sincronizzazione. Ciò consente a un thread di attendere fino a quando l'oggetto non è nello stato segnalato.                                                                                                                                                                |
| **Scrivi \_ Applicazione livello dati** (0x00040000L)    | Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                                   |
| **Scrivi \_ PROPRIETARIO** (0x00080000L)  | Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.                                                                                                                                                                                                                  |



 

Nella tabella seguente sono elencati i diritti di accesso specifici del processo.



| Valore                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Processo \_ di \_ \_ Accesso a tutti gli oggetti** (0x1F001F)             | Combina tutti i diritti di accesso agli oggetti processo validi.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Processo \_ di \_ \_ Processo di assegnazione di oggetti** (0x0001)           | Obbligatorio per chiamare la funzione [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) per assegnare processi all'oggetto processo.                                                                                                                                                                                                                                                                                                                                                                |
| **Processo \_ di \_Query di oggetto** (0x0004)                     | Obbligatorio per recuperare determinate informazioni su un oggetto processo, ad esempio gli attributi e le informazioni di contabilità (vedere [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) e [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)).                                                                                                                                                                                                                                                                    |
| **Processo \_ di \_ \_ Attributi set di oggetti** (0x0002)           | Obbligatorio per chiamare la funzione [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) per impostare gli attributi dell'oggetto processo.                                                                                                                                                                                                                                                                                                                                                                |
| **Processo \_ di \_Attributi di \_ sicurezza \_ del set di oggetti** (0x0010) | Questo flag non è supportato. È necessario impostare le limitazioni di sicurezza singolarmente per ogni processo associato a un oggetto processo. **Windows Server 2003 e Windows XP:** Obbligatorio per chiamare la funzione [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la classe di informazioni **JobObjectSecurityLimitInformation** per impostare le limitazioni di sicurezza per i processi associati all'oggetto processo. Il supporto per questo flag è stato rimosso in Windows Vista e Windows Server 2008. <br/> |
| **Processo \_ di OGGETTO \_ terminato** (0x0008)                 | Obbligatorio per chiamare la funzione [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) per terminare tutti i processi nell'oggetto processo.                                                                                                                                                                                                                                                                                                                                                                     |



 

L'handle restituito da [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) dispone di un **oggetto processo che \_ \_ \_ accede** all'oggetto processo. Quando si chiama la funzione [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto. Se un oggetto processo si trova in una gerarchia di [processi annidati](nested-jobs.md), un chiamante con accesso all'oggetto processo può accedere in modo implicito a tutti i relativi processi figlio nella gerarchia.

È possibile richiedere il diritto di accesso di **\_ \_ sicurezza del sistema di accesso** a un oggetto processo se si desidera leggere o scrivere il SACL dell'oggetto. Per altre informazioni, vedere [elenchi di controllo di accesso (ACL)](../secauthz/access-control-lists.md) e [accesso SACL diritto](../secauthz/sacl-access-right.md).

È necessario impostare le limitazioni di sicurezza singolarmente per ogni processo associato a un oggetto processo, anziché impostarle per l'oggetto processo stesso. Per informazioni, vedere [sicurezza del processo e diritti di accesso](process-security-and-access-rights.md).

**Windows Server 2003 e Windows XP:** È possibile utilizzare la funzione [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) per impostare limitazioni di sicurezza per l'oggetto processo. Questa funzionalità è stata rimossa in Windows Vista e Windows Server 2008.

 

 
