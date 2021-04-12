---
title: Autenticazione reciproca nelle applicazioni Windows Sockets
description: I servizi Microsoft Windows Sockets possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi oppure possono usare i punti di connessione del servizio.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Autenticazione reciproca nelle applicazioni Windows Sockets
- Active Directory, uso dell'autenticazione reciproca nelle applicazioni Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220928"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a><span data-ttu-id="39a94-105">Autenticazione reciproca nelle applicazioni Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="39a94-105">Mutual Authentication in Windows Sockets Applications</span></span>

<span data-ttu-id="39a94-106">I servizi Microsoft Windows Sockets possono usare le API di registrazione e risoluzione (RnR) per pubblicare i servizi oppure possono usare i punti di connessione del servizio.</span><span class="sxs-lookup"><span data-stu-id="39a94-106">Microsoft Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services, or they can use service connection points.</span></span>

<span data-ttu-id="39a94-107">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire l'autenticazione reciproca per un servizio Windows Sockets che pubblica utilizzando un punto di connessione del servizio, vedere [autenticazione reciproca in un servizio Windows Sockets con SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="39a94-107">For more information and a code example that shows how to perform mutual authentication for a Windows Sockets service that publishes using a service connection point, see [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span></span> <span data-ttu-id="39a94-108">In questo esempio di codice viene utilizzato un pacchetto di sicurezza SSPI per gestire le negoziazioni di autenticazione tra un client e il servizio WinSock.</span><span class="sxs-lookup"><span data-stu-id="39a94-108">This code example uses an SSPI security package to manage the authentication negotiations between a client and the WinSock service.</span></span>

<span data-ttu-id="39a94-109">Un servizio WinSock RnR può utilizzare codice simile per eseguire l'autenticazione reciproca utilizzando un pacchetto SSPI.</span><span class="sxs-lookup"><span data-stu-id="39a94-109">A WinSock RnR service can use similar code to perform mutual authentication using an SSPI package.</span></span> <span data-ttu-id="39a94-110">In questo caso, il servizio comporrà i nomi SPN usando il nome distinto della voce del servizio nel contenitore WinsockServices nella directory.</span><span class="sxs-lookup"><span data-stu-id="39a94-110">In this case, the service would compose its SPNs using the distinguished name of the service's entry in the WinsockServices container in the directory.</span></span>

<span data-ttu-id="39a94-111">Se, ad esempio, il servizio si registra con il nome "WinSockRnRSampleService", è necessario comporre il nome SPN del servizio dal nome distinto seguente:</span><span class="sxs-lookup"><span data-stu-id="39a94-111">For example, if the service registers itself with the name "WinSockRnRSampleService", you would compose the service's SPN from the following distinguished name:</span></span>


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




