---
title: Registrazione degli endpoint
description: La registrazione del programma server nella mappa degli endpoint del computer host del server consente ai programmi client di determinare quale endpoint (in genere una porta TCP/IP o un named pipe) a cui il programma server è in ascolto.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- RPC (Remote Procedure Call), attività, registrazione degli endpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707327"
---
# <a name="registering-endpoints"></a><span data-ttu-id="2a944-104">Registrazione degli endpoint</span><span class="sxs-lookup"><span data-stu-id="2a944-104">Registering Endpoints</span></span>

<span data-ttu-id="2a944-105">La registrazione del programma server nella mappa degli endpoint del computer host del server consente ai programmi client di determinare quale endpoint (in genere una porta TCP/IP o un named pipe) a cui il programma server è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="2a944-105">Registering the server program in the endpoint map of the server host computer enables client programs to determine which endpoint (usually a TCP/IP port or a named pipe) the server program is listening to.</span></span> <span data-ttu-id="2a944-106">Per registrarsi nella mappa degli endpoint del sistema host del server, un programma server chiama la funzione [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) , come illustrato nel frammento di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="2a944-106">To register itself in the server host system's endpoint map, a server program calls the [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) function as shown in the following code fragment:</span></span>


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



<span data-ttu-id="2a944-107">Il primo parametro di [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) è la struttura che rappresenta l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2a944-107">The first parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is the structure that represents the interface.</span></span> <span data-ttu-id="2a944-108">È possibile trovarlo nel file di intestazione generato dal compilatore MIDL dal file MIDL per questa applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="2a944-108">You can find it in the header file that the MIDL compiler generated from your MIDL file for this distributed application.</span></span> <span data-ttu-id="2a944-109">Vedere [sviluppo dell'interfaccia](developing-the-interface.md).</span><span class="sxs-lookup"><span data-stu-id="2a944-109">See [Developing the Interface](developing-the-interface.md).</span></span> <span data-ttu-id="2a944-110">Successivamente, **RpcEpRegister** richiede che l'applicazione passi un set di handle di associazione archiviati in un vettore di associazione.</span><span class="sxs-lookup"><span data-stu-id="2a944-110">Next, **RpcEpRegister** needs your application to pass a set of binding handles that are stored in a binding vector.</span></span>

<span data-ttu-id="2a944-111">Oltre a registrare i nomi di interfaccia, l'applicazione server può registrare anche UUID di oggetti nella mappa dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="2a944-111">In addition to registering interface names, your server application can also register object UUIDs in the endpoint map.</span></span> <span data-ttu-id="2a944-112">In questo esempio non sono presenti UUID di oggetto da registrare, quindi il terzo parametro di [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="2a944-112">In this example, there are no object UUIDs to register, so the third parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is set to **NULL**.</span></span>

<span data-ttu-id="2a944-113">L'ultimo parametro è una stringa di commento.</span><span class="sxs-lookup"><span data-stu-id="2a944-113">The last parameter is a comment string.</span></span> <span data-ttu-id="2a944-114">Sebbene la libreria di runtime RPC non utilizzi questa stringa, l'impostazione della stringa è consigliata, in quanto migliora la gestibilità del sistema.</span><span class="sxs-lookup"><span data-stu-id="2a944-114">Although the RPC run-time library does not use this string, setting the string is recommended, as it improves manageability of the system.</span></span> <span data-ttu-id="2a944-115">Un amministratore di sistema può utilizzare la stringa per individuare le porte utilizzate dalle applicazioni, che possono essere utilizzate per determinare le porte da gestire con i firewall.</span><span class="sxs-lookup"><span data-stu-id="2a944-115">A system administrator can use the string to detect which ports are used by which applications, which can then be used to determine which ports to be managed by firewalls.</span></span>

 

 




