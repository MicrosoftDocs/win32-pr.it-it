---
title: Codici restituiti Direct3D 12
description: Di seguito sono riportati i codici restituiti dalle funzioni API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300260"
---
# <a name="direct3d-12-return-codes"></a><span data-ttu-id="41733-103">Codici restituiti Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="41733-103">Direct3D 12 Return Codes</span></span>

<span data-ttu-id="41733-104">Di seguito sono riportati i codici restituiti dalle funzioni API.</span><span class="sxs-lookup"><span data-stu-id="41733-104">The following are return codes from API functions.</span></span> <span data-ttu-id="41733-105">Per ulteriori codici restituiti, vedere [DXGI \_ Error](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="41733-105">For more return codes, see [DXGI\_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>



| <span data-ttu-id="41733-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="41733-106">HRESULT</span></span>                                                                  | <span data-ttu-id="41733-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41733-107">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41733-108">\_Adattatore errore \_ D3D12 \_ non \_ trovato</span><span class="sxs-lookup"><span data-stu-id="41733-108">D3D12\_ERROR\_ADAPTER\_NOT\_FOUND</span></span>                                        | <span data-ttu-id="41733-109">L'oggetto PSO memorizzato nella cache specificato è stato creato in una scheda diversa e non può essere riutilizzato nell'adapter corrente.</span><span class="sxs-lookup"><span data-stu-id="41733-109">The specified cached PSO was created on a different adapter and cannot be reused on the current adapter.</span></span>          |
| <span data-ttu-id="41733-110">Versione del driver di errore D3D12 non \_ \_ \_ \_ corrispondente</span><span class="sxs-lookup"><span data-stu-id="41733-110">D3D12\_ERROR\_DRIVER\_VERSION\_MISMATCH</span></span>                                  | <span data-ttu-id="41733-111">L'oggetto PSO memorizzato nella cache specificato è stato creato in una versione di driver diversa e non può essere riutilizzato nell'adapter corrente.</span><span class="sxs-lookup"><span data-stu-id="41733-111">The specified cached PSO was created on a different driver version and cannot be reused on the current adapter.</span></span>  |
| <span data-ttu-id="41733-112">D3DERR \_ INVALIDCALL (sostituito con DXGI \_ errore \_ chiamata non valida \_ )</span><span class="sxs-lookup"><span data-stu-id="41733-112">D3DERR\_INVALIDCALL (replaced with DXGI\_ERROR\_INVALID\_CALL)</span></span>           | <span data-ttu-id="41733-113">La chiamata al metodo non è valida.</span><span class="sxs-lookup"><span data-stu-id="41733-113">The method call is invalid.</span></span> <span data-ttu-id="41733-114">Il parametro di un metodo, ad esempio, non può essere un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="41733-114">For example, a method's parameter may not be a valid pointer.</span></span>                             |
| <span data-ttu-id="41733-115">D3DERR \_ WASSTILLDRAWING (sostituito con DXGI \_ errore durante il \_ \_ \_ disegno)</span><span class="sxs-lookup"><span data-stu-id="41733-115">D3DERR\_WASSTILLDRAWING (replaced with DXGI\_ERROR\_WAS\_STILL\_DRAWING)</span></span> | <span data-ttu-id="41733-116">L'operazione blit precedente che sta trasferendo informazioni da o verso questa superficie non è completa.</span><span class="sxs-lookup"><span data-stu-id="41733-116">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                   |
| <span data-ttu-id="41733-117">E \_ non riescono</span><span class="sxs-lookup"><span data-stu-id="41733-117">E\_FAIL</span></span>                                                                  | <span data-ttu-id="41733-118">Si è tentato di creare un dispositivo con il livello di debug abilitato e il livello non è installato.</span><span class="sxs-lookup"><span data-stu-id="41733-118">Attempted to create a device with the debug layer enabled and the layer is not installed.</span></span>                             |
| <span data-ttu-id="41733-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="41733-119">E\_INVALIDARG</span></span>                                                            | <span data-ttu-id="41733-120">Un parametro non valido è stato passato alla funzione di restituzione.</span><span class="sxs-lookup"><span data-stu-id="41733-120">An invalid parameter was passed to the returning function.</span></span>                                                             |
| <span data-ttu-id="41733-121">E \_ OutOfMemory</span><span class="sxs-lookup"><span data-stu-id="41733-121">E\_OUTOFMEMORY</span></span>                                                           | <span data-ttu-id="41733-122">Direct3D non è riuscito ad allocare memoria sufficiente per completare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="41733-122">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                   |
| <span data-ttu-id="41733-123">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="41733-123">E\_NOTIMPL</span></span>                                                               | <span data-ttu-id="41733-124">La chiamata al metodo non viene implementata con la combinazione di parametri passata.</span><span class="sxs-lookup"><span data-stu-id="41733-124">The method call isn't implemented with the passed parameter combination.</span></span>                                               |
| <span data-ttu-id="41733-125">S \_ false</span><span class="sxs-lookup"><span data-stu-id="41733-125">S\_FALSE</span></span>                                                                 | <span data-ttu-id="41733-126">Valore di operazione riuscita alternativo, che indica un completamento positivo ma non standard (il significato esatto dipende dal contesto).</span><span class="sxs-lookup"><span data-stu-id="41733-126">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span> |
| <span data-ttu-id="41733-127">\_OK</span><span class="sxs-lookup"><span data-stu-id="41733-127">S\_OK</span></span>                                                                    | <span data-ttu-id="41733-128">Non si sono verificati errori.</span><span class="sxs-lookup"><span data-stu-id="41733-128">No error occurred.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="41733-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41733-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41733-130">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="41733-130">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 