---
description: È possibile specificare un descrittore di sicurezza per named pipe quando si chiama la funzione CreateNamedPipe. Il descrittore di sicurezza controlla l'accesso alle estremità client e server del named pipe.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Sicurezza e diritti di accesso delle named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556987cf35845de249bf0e19f3a0b481aab18e891c3b6211f26eb51571704d7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451211"
---
# <a name="named-pipe-security-and-access-rights"></a>Sicurezza e diritti di accesso delle named pipe

Windows sicurezza consente di controllare l'accesso alle named pipe. Per altre informazioni sulla sicurezza, vedere [Modello di controllo di accesso.](/windows/desktop/SecAuthZ/access-control-model)

È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per named pipe quando si chiama la [**funzione CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) Il descrittore di sicurezza controlla l'accesso alle estremità client e server del named pipe. Se si specifica **NULL,** il named pipe ottiene un descrittore di sicurezza predefinito. Gli ACL nel descrittore di sicurezza predefinito per un named pipe concedono il controllo completo all'account LocalSystem, agli amministratori e al proprietario dell'autore. Concedono anche l'accesso in lettura ai membri del gruppo Everyone e all'account anonimo.

Per recuperare un named pipe di sicurezza di un utente, chiamare la [**funzione GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) Per modificare il descrittore di sicurezza di un named pipe, chiamare la [**funzione SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Quando un thread chiama [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) per aprire un handle all'estremità server di un named pipe esistente, il sistema esegue un controllo di accesso prima di restituire l'handle. Il controllo di accesso confronta il token [](/windows/desktop/SecAuthZ/access-rights-and-access-masks) di accesso del thread e i diritti di accesso richiesti con l'elenco DACL nel named pipe di sicurezza del thread. Oltre ai diritti di accesso richiesti, l'elenco DACL deve consentire al thread chiamante FILE \_ CREATE PIPE INSTANCE l'accesso al \_ \_ named pipe.

Analogamente, quando un client chiama la [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) per connettersi all'estremità client di un named pipe, il sistema esegue un controllo di accesso prima di concedere l'accesso al client.

L'handle restituito dalla [**funzione CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) ha sempre l'accesso SYNCHRONIZE. Include anche GENERIC \_ READ, GENERIC WRITE o entrambi, a \_ seconda della modalità di apertura della pipe. Di seguito sono riportati i diritti di accesso per ogni modalità aperta.



| Modalità di apertura                           | Diritti di accesso                                              |
|-------------------------------------|------------------------------------------------------------|
| PIPE \_ ACCESS \_ DUPLEX (0x00000003)   | FILE \_ GENERIC \_ READ, FILE GENERIC WRITE e \_ \_ SYNCHRONIZE |
| PIPE \_ ACCESS \_ INBOUND (0x00000001)  | FILE \_ GENERIC READ e \_ SYNCHRONIZE                        |
| PIPE \_ ACCESS \_ OUTBOUND (0x00000002) | FILE \_ GENERIC WRITE e \_ SYNCHRONIZE                       |



 

L'accesso IN LETTURA GENERICO FILE per un named pipe combina i diritti per leggere i dati dalla pipe, leggere gli attributi della pipe, leggere gli attributi estesi e leggere \_ \_ l'elenco DACL della pipe.

L'accesso WRITE GENERICO FILE per un named pipe combina i diritti di scrittura dei dati nella pipe, l'aggiunta di dati, la scrittura di attributi della pipe, la scrittura di attributi estesi e la lettura \_ \_ dell'elenco DACL della pipe. Poiché FILE APPEND DATA e FILE CREATE PIPE INSTANCE hanno la stessa definizione, FILE GENERIC WRITE abilita \_ \_ \_ \_ \_ \_ \_ l'autorizzazione per creare la pipe. Per evitare questo problema, usare i singoli diritti anziché FILE \_ GENERIC \_ WRITE.

È possibile richiedere il diritto di accesso ACCESS SYSTEM SECURITY a un oggetto named pipe se si vuole leggere o \_ \_ scrivere l'elenco SACL dell'oggetto. Per altre informazioni, vedere [Elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e Diritto di accesso [SACL.](/windows/desktop/SecAuthZ/sacl-access-right)

Per impedire agli utenti remoti o agli utenti di una sessione di Servizi terminal diversa di accedere a un named pipe, usare il SID di accesso nell'elenco DACL per la pipe. Il SID di accesso viene usato anche negli accessi RunAs. è il SID usato per proteggere lo spazio dei nomi dell'oggetto per sessione. Per altre informazioni, vedere [Recupero del SID di accesso in C++.](/previous-versions//aa446670(v=vs.85))

 

 
