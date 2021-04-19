---
description: Per modificare gli attributi di una connessione, ad esempio il pacchetto di crittografia o l'autenticazione client, è possibile richiedere un &\# 0034; rollforward&\# 0034; o rinegoziazione della connessione.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Rinegoziazione di una connessione Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311612"
---
# <a name="renegotiating-an-schannel-connection"></a>Rinegoziazione di una connessione Schannel

Per modificare gli attributi di una connessione, ad esempio il pacchetto di crittografia o l'autenticazione client, è possibile richiedere una "ripetizione" o una rinegoziazione della connessione.

Se gli attributi che si desidera modificare sono controllati da credenziali, è necessario ottenere nuove credenziali prima di rinegoziare la connessione. Per ulteriori informazioni, vedere [ottenere le credenziali Schannel](obtaining-schannel-credentials.md).

Per richiedere un rollforward da un'applicazione client, chiamare la funzione [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Le applicazioni server chiamano la funzione [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) . Impostare i parametri come segue:

-   Specificare il [*contesto di sicurezza*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) esistente nel parametro *phContext* .
-   (Solo client) Specificare lo stesso nome server (nel parametro *pszTargetName* ) come specificato durante la definizione del contesto.
-   Specificare le nuove credenziali, se applicabile, usando il parametro *phCredential* .
-   Se si desidera modificare gli attributi del contesto non correlati alle credenziali, specificare questi attributi utilizzando il parametro *fContextReq* .

Dopo aver chiamato la funzione appropriata, l'applicazione deve inviare i risultati al client e continuare a elaborare i messaggi in arrivo usando la funzione [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) .

La funzione [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) restituirà il \_ secondo \_ rinegoziato quando Schannel è pronto per continuare l'applicazione. Quando si riceve la prima volta \_ che si \_ rinegozia il codice restituito, l'applicazione deve chiamare [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (Server) o [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (client) e passare il contenuto di SECBUFFER_EXTRA restituito da DecryptMessage nel SECBUFFER_TOKEN. Quando questa chiamata restituisce un valore, procedere come se l'applicazione creasse una nuova connessione.

 

 
