---
description: Le dll TAPI, insieme al server TAPI (Tapisvr.exe), sono astrazioni cruciali che separano le applicazioni dell'utente finale o del server dai provider di servizi. Una DLL TAPI insieme al server TAPI fornisce un'interfaccia coerente tra i due livelli.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: DLL TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560450"
---
# <a name="tapi-dll"></a><span data-ttu-id="a96ee-104">DLL TAPI</span><span class="sxs-lookup"><span data-stu-id="a96ee-104">TAPI DLL</span></span>

<span data-ttu-id="a96ee-105">Le dll TAPI, insieme al server TAPI (Tapisvr.exe), sono astrazioni cruciali che separano le applicazioni dell'utente finale o del server dai provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="a96ee-105">The TAPI DLLs, along with the TAPI Server (Tapisvr.exe), are crucial abstractions separating end-user or server applications from service providers.</span></span> <span data-ttu-id="a96ee-106">Una DLL TAPI insieme al server TAPI fornisce un'interfaccia coerente tra i due livelli.</span><span class="sxs-lookup"><span data-stu-id="a96ee-106">A TAPI DLL in conjunction with the TAPI Server provides a consistent interface between these two layers.</span></span>

<span data-ttu-id="a96ee-107">Un'applicazione TAPI carica la DLL appropriata nello spazio di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a96ee-107">A TAPI application loads the appropriate DLL into its process space.</span></span> <span data-ttu-id="a96ee-108">Durante l'inizializzazione, TAPI stabilisce un collegamento RPC con Tapisvr.exe.</span><span class="sxs-lookup"><span data-stu-id="a96ee-108">During initialization, TAPI establishes an RPC link with Tapisvr.exe.</span></span> <span data-ttu-id="a96ee-109">Il server TAPI viene eseguito nel contesto di SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="a96ee-109">The TAPI Server runs in the context of SVCHOST.</span></span>

<span data-ttu-id="a96ee-110">Sono disponibili tre DLL associate a TAPI: Tapi.dll, Tapi32.dll e Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="a96ee-110">There are three DLLs associated with TAPI: Tapi.dll, Tapi32.dll, and Tapi3.dll.</span></span> <span data-ttu-id="a96ee-111">Queste dll si trovano in% SystemRoot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="a96ee-111">These DLLs are located in %SystemRoot%\\system32.</span></span> <span data-ttu-id="a96ee-112">Nella figura seguente vengono illustrati i ruoli dei rispettivi ruoli in telefonia Microsoft:</span><span class="sxs-lookup"><span data-stu-id="a96ee-112">The following figure illustrates the roles of their respective roles in Microsoft Telephony:</span></span>

![ruoli delle tre dll TAPI](images/dllserv.png)

<span data-ttu-id="a96ee-114">Le applicazioni a 16 bit esistenti si collegano a Tapi.dll.</span><span class="sxs-lookup"><span data-stu-id="a96ee-114">Existing 16-bit applications link to Tapi.dll.</span></span> <span data-ttu-id="a96ee-115">Tapi.dll è semplicemente un livello thunk che esegue il mapping degli indirizzi a 16 bit a indirizzi a 32 bit e passa le richieste al Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a96ee-115">Tapi.dll is simply a thunk layer that maps 16-bit addresses to 32-bit addresses and pass requests to Tapi32.dll.</span></span>

<span data-ttu-id="a96ee-116">Le applicazioni TAPI 2. x a 32 bit esistenti si collegano a Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a96ee-116">Existing 32-bit TAPI 2.x applications link to Tapi32.dll.</span></span> <span data-ttu-id="a96ee-117">Tapi32.dll è un livello di marshalling sottile che trasferisce le richieste di funzione al server TAPI (TAPISRV) e, quando necessario, carica e richiama le dll del provider di servizi multimediali nel processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a96ee-117">Tapi32.dll is a thin marshalling layer that transfers function requests to the TAPI Server (TAPISRV) and, when needed, loads and invokes media service provider DLLs in the application's process.</span></span>

<span data-ttu-id="a96ee-118">Le applicazioni TAPI 3. x si collegano a Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="a96ee-118">TAPI 3.x applications link to Tapi3.dll.</span></span>

 

 



