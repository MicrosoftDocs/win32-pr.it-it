---
title: Descrittori
description: I descrittori sono l'unità primaria di binding per una singola risorsa in D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104247"
---
# <a name="descriptors"></a><span data-ttu-id="1abc3-103">Descrittori</span><span class="sxs-lookup"><span data-stu-id="1abc3-103">Descriptors</span></span>

<span data-ttu-id="1abc3-104">I descrittori sono l'unità primaria di binding per una singola risorsa in D3D12.</span><span class="sxs-lookup"><span data-stu-id="1abc3-104">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1abc3-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1abc3-105">In this section</span></span>



| <span data-ttu-id="1abc3-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="1abc3-106">Topic</span></span>                                                       | <span data-ttu-id="1abc3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1abc3-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1abc3-108">Cenni preliminari sui descrittori</span><span class="sxs-lookup"><span data-stu-id="1abc3-108">Descriptors Overview</span></span>](descriptors-overview.md)<br/> | <span data-ttu-id="1abc3-109">I descrittori vengono creati dalle chiamate API e identificano le risorse.</span><span class="sxs-lookup"><span data-stu-id="1abc3-109">Descriptors are created by API calls and identify resources.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="1abc3-110">Creazione di descrittori</span><span class="sxs-lookup"><span data-stu-id="1abc3-110">Creating Descriptors</span></span>](creating-descriptors.md)<br/> | <span data-ttu-id="1abc3-111">Vengono descritti e illustrati esempi per la creazione di viste di buffer di indice, vertex e costanti; risorsa shader, destinazione di rendering, accesso non ordinato, output del flusso e visualizzazioni di stencil Depth; e Samplers.</span><span class="sxs-lookup"><span data-stu-id="1abc3-111">Describes and shows examples for creating index, vertex, and constant buffer views; shader resource, render target, unordered access, stream output and depth-stencil views; and samplers.</span></span> <span data-ttu-id="1abc3-112">Tutti i metodi per la creazione di descrittori sono a thread libero.</span><span class="sxs-lookup"><span data-stu-id="1abc3-112">All methods for creating descriptors are free threaded.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="1abc3-113">Copia di descrittori</span><span class="sxs-lookup"><span data-stu-id="1abc3-113">Copying Descriptors</span></span>](copying-descriptors.md)<br/>   | <span data-ttu-id="1abc3-114">I metodi [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) sull'interfaccia del dispositivo utilizzano la CPU per copiare immediatamente i descrittori.</span><span class="sxs-lookup"><span data-stu-id="1abc3-114">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="1abc3-115">Possono essere denominati thread gratuiti purché più thread sulla CPU o sulla GPU non eseguano Scritture potenzialmente in conflitto.</span><span class="sxs-lookup"><span data-stu-id="1abc3-115">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1abc3-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1abc3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1abc3-117">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="1abc3-117">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="1abc3-118">Tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="1abc3-118">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="1abc3-119">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="1abc3-119">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="1abc3-120">Firme radice</span><span class="sxs-lookup"><span data-stu-id="1abc3-120">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





