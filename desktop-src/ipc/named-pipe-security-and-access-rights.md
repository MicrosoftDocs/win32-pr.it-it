---
description: È possibile specificare un descrittore di sicurezza per un named pipe quando si chiama la funzione CreateNamedPipe. Il descrittore di sicurezza controlla l'accesso alle entità finali client e server del named pipe.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Diritti di accesso e sicurezza della named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cada606d8197ac2f64943aa742bbfd614fa4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313056"
---
# <a name="named-pipe-security-and-access-rights"></a>Diritti di accesso e sicurezza della named pipe

La sicurezza di Windows consente di controllare l'accesso alle named pipe. Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).

È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per un named pipe quando si chiama la funzione [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . Il descrittore di sicurezza controlla l'accesso alle entità finali client e server del named pipe. Se si specifica **null**, il named pipe ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per un named pipe concedere il controllo completo all'account LocalSystem, agli amministratori e al proprietario dell'autore. Inoltre, concede l'accesso in lettura ai membri del gruppo Everyone e dell'account anonimo.

Per recuperare il descrittore di sicurezza di un named pipe, chiamare la funzione [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Per modificare il descrittore di sicurezza di un named pipe, chiamare la funzione [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Quando un thread chiama [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) per aprire un handle per l'entità finale del server di un named pipe esistente, il sistema esegue un controllo di accesso prima di restituire l'handle. Il controllo dell'accesso confronta il token di accesso del thread e i [diritti di accesso](/windows/desktop/SecAuthZ/access-rights-and-access-masks) richiesti rispetto a DACL nel descrittore di sicurezza del named pipe. Oltre ai diritti di accesso richiesti, l'elenco DACL deve consentire al FILE del thread \_ chiamante \_ di creare l' \_ istanza di pipe per l'accesso alla named pipe.

Analogamente, quando un client chiama la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) per connettersi al lato client di una named pipe, il sistema esegue un controllo di accesso prima di concedere l'accesso al client.

L'handle restituito dalla funzione [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) ha sempre l'accesso Synchronize. Dispone inoltre \_ di lettura generica, \_ scrittura generica o entrambi, a seconda della modalità di apertura della pipe. Di seguito sono riportati i diritti di accesso per ogni modalità di apertura.



| Modalità di apertura                           | Diritti di accesso                                              |
|-------------------------------------|------------------------------------------------------------|
| Accesso tramite PIPE \_ \_ duplex (0x00000003)   | FILE \_ \_ letto generico, \_ scrittura generica file \_ e sincronizzazione |
| Accesso tramite PIPE in \_ \_ ingresso (0x00000001)  | \_ \_ Lettura e sincronizzazione file generici                        |
| Accesso PIPE in \_ \_ uscita (0x00000002) | \_ \_ Scrittura e sincronizzazione di file generici                       |



 

\_Accesso in \_ lettura generico file per un named pipe combina i diritti per leggere i dati dalla pipe, leggere gli attributi della pipe, leggere gli attributi estesi e leggere il DACL della pipe.

\_Accesso in \_ scrittura generico file per un named pipe combina i diritti per scrivere i dati nella pipe, accodare i dati, scrivere attributi pipe, scrivere attributi estesi e leggere il DACL della pipe. Poiché \_ \_ l'istanza di file Accoda dati e file \_ Create \_ pipe \_ ha la stessa definizione, quindi file \_ Generic \_ Write Abilita l'autorizzazione per la creazione della pipe. Per evitare questo problema, utilizzare i singoli diritti anziché utilizzare la \_ scrittura generica del file \_ .

È possibile richiedere il \_ \_ diritto di accesso di sicurezza del sistema di accesso a un oggetto named pipe se si desidera leggere o scrivere il SACL dell'oggetto. Per altre informazioni, vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [accesso SACL diritto](/windows/desktop/SecAuthZ/sacl-access-right).

Per impedire agli utenti remoti o agli utenti di un'altra sessione di Servizi terminal di accedere a una named pipe, utilizzare il SID di accesso nell'elenco DACL per la pipe. Il SID di accesso viene utilizzato anche negli accessi RunAs. si tratta del SID usato per proteggere lo spazio dei nomi dell'oggetto per sessione. Per ulteriori informazioni, vedere [recupero del SID di accesso in C++](/previous-versions//aa446670(v=vs.85)).

 

 
