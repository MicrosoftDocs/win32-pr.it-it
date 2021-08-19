---
title: Autenticazione reciproca nelle Windows Sockets
description: I servizi Microsoft Windows Sockets possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi oppure i punti di connessione del servizio.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Autenticazione reciproca nelle Windows Sockets
- Active Directory, tramite l'autenticazione reciproca, nelle Windows socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a7267159f826d572a8efd101ab86338f5a24c6966b8d2af3a260e1f4af6244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025749"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>Autenticazione reciproca nelle Windows Sockets

I servizi Microsoft Windows Sockets possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi oppure i punti di connessione del servizio.

Per altre informazioni e un esempio di codice che illustra come eseguire l'autenticazione reciproca per un servizio socket Windows che pubblica tramite un punto di connessione del servizio, vedere Autenticazione reciproca in un servizio Windows Sockets con [SCP.](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) Questo esempio di codice usa un pacchetto di sicurezza SSPI per gestire le negoziazioni di autenticazione tra un client e il servizio WinSock.

Un servizio WinSock RnR può usare codice simile per eseguire l'autenticazione reciproca usando un pacchetto SSPI. In questo caso, il servizio componi i relativi nomi SPN usando il nome distinto della voce del servizio nel contenitore WinsockServices nella directory .

Ad esempio, se il servizio si registra con il nome "WinSockRnRSampleService", è necessario comporre il nome SPN del servizio dal nome distinto seguente:


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




