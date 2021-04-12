---
title: Stub client
description: Il modulo stub client fornisce punti di ingresso surrogati sul client per ogni operazione definita nel file IDL di input.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL e RPC MIDL, interfacce, Stub client
- interfacce MIDL
- interfacce MIDL, MIDL e RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331375"
---
# <a name="the-client-stub"></a><span data-ttu-id="419dc-106">Stub client</span><span class="sxs-lookup"><span data-stu-id="419dc-106">The Client Stub</span></span>

<span data-ttu-id="419dc-107">Il modulo stub client fornisce punti di ingresso surrogati sul client per ogni operazione definita nel file IDL di input.</span><span class="sxs-lookup"><span data-stu-id="419dc-107">The client stub module provides surrogate entry points on the client for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="419dc-108">Quando l'applicazione client effettua una chiamata alla procedura remota, la relativa chiamata passa prima alla routine surrogata nel file stub del client.</span><span class="sxs-lookup"><span data-stu-id="419dc-108">When the client application makes a call to the remote procedure, its call first goes to the surrogate routine in the client stub file.</span></span> <span data-ttu-id="419dc-109">La routine stub client esegue le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="419dc-109">The client stub routine performs the following functions:</span></span>

-   <span data-ttu-id="419dc-110">Esegue il marshalling degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="419dc-110">Marshals arguments.</span></span> <span data-ttu-id="419dc-111">Il client Stub inserisce gli argomenti di input in un modulo che può essere trasmesso al server.</span><span class="sxs-lookup"><span data-stu-id="419dc-111">The client stub packages input arguments into a form that can be transmitted to the server.</span></span>
-   <span data-ttu-id="419dc-112">Chiama la libreria di runtime del client per trasmettere argomenti allo spazio di indirizzi remoto e richiama la procedura remota nello spazio degli indirizzi del server.</span><span class="sxs-lookup"><span data-stu-id="419dc-112">Calls the client run-time library to transmit arguments to the remote address space and invokes the remote procedure in the server address space.</span></span>
-   <span data-ttu-id="419dc-113">Esegue l'unmarshalling degli argomenti di output.</span><span class="sxs-lookup"><span data-stu-id="419dc-113">Unmarshals output arguments.</span></span> <span data-ttu-id="419dc-114">Lo stub client decomprime gli argomenti di output e restituisce al chiamante.</span><span class="sxs-lookup"><span data-stu-id="419dc-114">The client stub unpacks output arguments and returns to the caller.</span></span>

<span data-ttu-id="419dc-115">Il compilatore MIDL passa [**/client**](-client.md), [**/cstub**](-cstub.md)e [**/out**](-out.md) influisce sul file stub del client.</span><span class="sxs-lookup"><span data-stu-id="419dc-115">The MIDL compiler switches [**/client**](-client.md), [**/cstub**](-cstub.md), and [**/out**](-out.md) affect the client stub file.</span></span>

 

 




