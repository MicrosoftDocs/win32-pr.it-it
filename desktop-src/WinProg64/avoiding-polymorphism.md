---
title: Evitare il polimorfismo
description: I nuovi tipi di dati includono due tipi polimorfici, INT \_ ptr e Long \_ ptr.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- polimorfismo-programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332100"
---
# <a name="avoiding-polymorphism"></a><span data-ttu-id="80e3e-104">Evitare il polimorfismo</span><span class="sxs-lookup"><span data-stu-id="80e3e-104">Avoiding Polymorphism</span></span>

<span data-ttu-id="80e3e-105">I nuovi tipi di dati includono due tipi polimorfici, **int \_ ptr** e **Long \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="80e3e-105">The new data types include two polymorphic types, **INT\_PTR** and **LONG\_PTR**.</span></span> <span data-ttu-id="80e3e-106">Nelle finestre a 32 bit, il **\_ ptr int** esegue il mapping a **int** e il **Long \_ ptr** viene mappato a **Long**.</span><span class="sxs-lookup"><span data-stu-id="80e3e-106">On 32-bit Windows, the **INT\_PTR** maps to **int** and the **LONG\_PTR** maps to **long**.</span></span> <span data-ttu-id="80e3e-107">Nelle finestre a 64 bit entrambi i tipi sono mappati al tipo intrinseco **\_ \_ Int64** .</span><span class="sxs-lookup"><span data-stu-id="80e3e-107">On 64-bit Windows, both types map to the **\_\_int64** intrinsic type.</span></span> <span data-ttu-id="80e3e-108">Il compilatore MIDL supporta questi tipi per le chiamate di procedure remote, ma esiste una limitazione intrinseca che è necessario tenere presente quando si usano in un ambiente distribuito.</span><span class="sxs-lookup"><span data-stu-id="80e3e-108">The MIDL compiler supports these types for remote procedure calls, but there is an inherent limitation that you must keep in mind when using them in a distributed environment.</span></span> <span data-ttu-id="80e3e-109">Assicurarsi di commentare il codice di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="80e3e-109">Be sure to comment your code accordingly.</span></span>

<span data-ttu-id="80e3e-110">Indipendentemente dalle dimensioni della piattaforma, le dimensioni del Wire di questi tipi polimorfici sono sempre di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="80e3e-110">Regardless of the platform size, the wire size of these polymorphic types is always 32 bits.</span></span> <span data-ttu-id="80e3e-111">Quando si esegue l'unmarshalling in Windows a 64 bit, il segno della libreria di Runtime estende i valori firmati e assegna zero ai byte più significativi per un valore senza segno.</span><span class="sxs-lookup"><span data-stu-id="80e3e-111">When unmarshaling on 64-bit Windows, the run-time library sign extends signed values and assigns zero to the high-order bytes for an unsigned value.</span></span> <span data-ttu-id="80e3e-112">Quando si inserisce un valore a 64 bit in rete, il runtime tronca i byte più ordinati.</span><span class="sxs-lookup"><span data-stu-id="80e3e-112">When putting a 64-bit value on the wire, the run time truncates the high-order bytes.</span></span> <span data-ttu-id="80e3e-113">Sono pertanto utilizzabili solo i valori a 32 bit di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="80e3e-113">Thus, only the low-order 32-bit values are usable.</span></span>

<span data-ttu-id="80e3e-114">Usare i tipi polimorfici solo quando necessario per il porting.</span><span class="sxs-lookup"><span data-stu-id="80e3e-114">Use the polymorphic types only when necessary for porting.</span></span> <span data-ttu-id="80e3e-115">Per le nuove interfacce, usare i tipi Integer intrinseci **\_ \_ MIDL e** **\_ \_ Int64** oppure usare un tipo di puntatore o un handle di contesto, a seconda del tipo di dati che si desidera trasferire.</span><span class="sxs-lookup"><span data-stu-id="80e3e-115">For new interfaces, use the MIDL intrinsic integer types **\_\_int32** and **\_\_int64**, or use a pointer type or context handle, whichever is most appropriate for the kind of data being transferred.</span></span>

<span data-ttu-id="80e3e-116">Il compilatore a 64 bit supporta un nuovo **\_ \_ int3264** intrinseco polimorfico.</span><span class="sxs-lookup"><span data-stu-id="80e3e-116">The 64-bit compiler supports a new polymorphic intrinsic **\_\_int3264**.</span></span> <span data-ttu-id="80e3e-117">Anche in questo caso, questo tipo è stato sviluppato per supportare le attività di porting, in questo caso per supportare in modo trasparente i tipi **uint \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="80e3e-117">Again, this type was developed to support porting efforts, in this case to support the **UINT\_PTR** types transparently.</span></span> <span data-ttu-id="80e3e-118">(Un'altra funzione intrinseca, **\_ \_ long3264**, supporterà il tipo **ULONG \_ ptr** ). Non utilizzare direttamente **\_ \_ int3264** . utilizzare il tipo **\_ ptr int** quando è necessario un tipo polimorfico per i motivi di portabilità.</span><span class="sxs-lookup"><span data-stu-id="80e3e-118">(Another intrinsic, **\_\_long3264**, will support the **ULONG\_PTR** type.) Do not use **\_\_int3264** directly; use the **INT\_PTR** type when you need a polymorphic type for porting reasons.</span></span>

 

 




