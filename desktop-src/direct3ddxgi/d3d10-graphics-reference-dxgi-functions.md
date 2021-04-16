---
description: Questa sezione contiene informazioni sulle funzioni fornite da DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Funzioni DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520874"
---
# <a name="dxgi-functions"></a><span data-ttu-id="a9055-103">Funzioni DXGI</span><span class="sxs-lookup"><span data-stu-id="a9055-103">DXGI Functions</span></span>

<span data-ttu-id="a9055-104">Questa sezione contiene informazioni sulle funzioni fornite da DXGI.</span><span class="sxs-lookup"><span data-stu-id="a9055-104">This section contains info about the functions provided by DXGI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a9055-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a9055-105">In this section</span></span>



| <span data-ttu-id="a9055-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="a9055-106">Topic</span></span>                                                                                   | <span data-ttu-id="a9055-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9055-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9055-108">**CreateDXGIFactory**</span><span class="sxs-lookup"><span data-stu-id="a9055-108">**CreateDXGIFactory**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | <span data-ttu-id="a9055-109">Crea una factory DXGI 1,0 che è possibile usare per generare altri oggetti DXGI.</span><span class="sxs-lookup"><span data-stu-id="a9055-109">Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="a9055-110">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="a9055-110">**CreateDXGIFactory1**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | <span data-ttu-id="a9055-111">Crea una factory DXGI 1,1 che è possibile usare per generare altri oggetti DXGI.</span><span class="sxs-lookup"><span data-stu-id="a9055-111">Creates a DXGI 1.1 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="a9055-112">**CreateDXGIFactory2**</span><span class="sxs-lookup"><span data-stu-id="a9055-112">**CreateDXGIFactory2**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | <span data-ttu-id="a9055-113">Crea una factory DXGI 1,3 che è possibile usare per generare altri oggetti DXGI.</span><span class="sxs-lookup"><span data-stu-id="a9055-113">Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.</span></span><br/> <span data-ttu-id="a9055-114">In Windows 8, qualsiasi Factory di DXGI creata durante la DXGIDebug.dll era presente nel sistema, la caricherà e la utilizzerebbe.</span><span class="sxs-lookup"><span data-stu-id="a9055-114">In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it.</span></span> <span data-ttu-id="a9055-115">A partire da Windows 8.1, le app richiedono in modo esplicito che DXGIDebug.dll venga caricato.</span><span class="sxs-lookup"><span data-stu-id="a9055-115">Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead.</span></span> <span data-ttu-id="a9055-116">Usare [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) e specificare il \_ \_ \_ flag di debug di DXGI create Factory per richiedere DXGIDebug.dll; la dll verrà caricata se presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a9055-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) and specify the DXGI\_CREATE\_FACTORY\_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.</span></span><br/> |
| [<span data-ttu-id="a9055-117">**DXGIDeclareAdapterRemovalSupport**</span><span class="sxs-lookup"><span data-stu-id="a9055-117">**DXGIDeclareAdapterRemovalSupport**</span></span>](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | <span data-ttu-id="a9055-118">Consente a un processo di indicare che è resiliente per i dispositivi grafici da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a9055-118">Allows a process to indicate that it's resilient to any of its graphics devices being removed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="a9055-119">**DXGIGetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="a9055-119">**DXGIGetDebugInterface**</span></span>](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | <span data-ttu-id="a9055-120">Recupera un'interfaccia di debug.</span><span class="sxs-lookup"><span data-stu-id="a9055-120">Retrieves a debugging interface.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="a9055-121">**DXGIGetDebugInterface1**</span><span class="sxs-lookup"><span data-stu-id="a9055-121">**DXGIGetDebugInterface1**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | <span data-ttu-id="a9055-122">Recupera un'interfaccia utilizzata dalle app di Windows Store per il debug di Microsoft DirectX Graphics Infrastructure (DXGI).</span><span class="sxs-lookup"><span data-stu-id="a9055-122">Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="a9055-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9055-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9055-124">Riferimento a DXGI</span><span class="sxs-lookup"><span data-stu-id="a9055-124">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




