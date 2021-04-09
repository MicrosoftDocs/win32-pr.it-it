---
description: La funzione DecryptMessage (generale) intercetta le richieste di rinegoziazione provenienti dal mittente del messaggio. Invia una notifica all'applicazione decrittografando i dati del messaggio e restituendo il valore SEC i \_ \_ rinegoziare.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Riconoscimento di una richiesta di rinegoziazione di una connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049978"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a>Riconoscimento di una richiesta di rinegoziazione di una connessione

La funzione [**DecryptMessage (generale)**](decryptmessage--general.md) intercetta le richieste di rinegoziazione provenienti dal mittente del messaggio. Invia una notifica all'applicazione decrittografando i dati del messaggio e restituendo il valore SEC i \_ \_ rinegoziare.

L'applicazione deve gestire tali richieste chiamando [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (Server) o [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md) (client) e passando il contenuto di SECBUFFER_EXTRA restituito da DecryptMessage nel SECBUFFER_TOKEN. Dopo che la chiamata iniziale restituisce un valore, procedere come se l'applicazione creasse una nuova connessione.

 

 



