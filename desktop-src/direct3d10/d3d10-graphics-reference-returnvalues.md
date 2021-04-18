---
description: La tabella seguente contiene i codici restituiti dalle funzioni API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Codici restituiti Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304714"
---
# <a name="direct3d-10-return-codes"></a><span data-ttu-id="83e3e-103">Codici restituiti Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="83e3e-103">Direct3D 10 Return Codes</span></span>

<span data-ttu-id="83e3e-104">La tabella seguente contiene i codici restituiti dalle funzioni API.</span><span class="sxs-lookup"><span data-stu-id="83e3e-104">The following table contains return codes from API functions.</span></span>



| <span data-ttu-id="83e3e-105">HRESULT</span><span class="sxs-lookup"><span data-stu-id="83e3e-105">HRESULT</span></span>                                         | <span data-ttu-id="83e3e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83e3e-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e3e-107">\_File di errore D3D10 \_ \_ non \_ trovato</span><span class="sxs-lookup"><span data-stu-id="83e3e-107">D3D10\_ERROR\_FILE\_NOT\_FOUND</span></span>                  | <span data-ttu-id="83e3e-108">Impossibile trovare il file.</span><span class="sxs-lookup"><span data-stu-id="83e3e-108">The file was not found.</span></span>                                                                                                                               |
| <span data-ttu-id="83e3e-109">\_Errore D3D10 \_ troppi \_ \_ \_ oggetti stato \_ univoco</span><span class="sxs-lookup"><span data-stu-id="83e3e-109">D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS</span></span> | <span data-ttu-id="83e3e-110">Troppe istanze univoche di un determinato tipo di [oggetto di stato](d3d10-graphics-programming-guide-api-features-state-objects.md).</span><span class="sxs-lookup"><span data-stu-id="83e3e-110">There are too many unique instances of a particular type of [state object](d3d10-graphics-programming-guide-api-features-state-objects.md).</span></span>          |
| <span data-ttu-id="83e3e-111">\_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="83e3e-111">D3DERR\_INVALIDCALL</span></span>                             | <span data-ttu-id="83e3e-112">La chiamata al metodo non è valida.</span><span class="sxs-lookup"><span data-stu-id="83e3e-112">The method call is invalid.</span></span> <span data-ttu-id="83e3e-113">Il parametro di un metodo, ad esempio, non può essere un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="83e3e-113">For example, a method's parameter may not be a valid pointer.</span></span>                                                             |
| <span data-ttu-id="83e3e-114">\_WASSTILLDRAWING D3DERR</span><span class="sxs-lookup"><span data-stu-id="83e3e-114">D3DERR\_WASSTILLDRAWING</span></span>                         | <span data-ttu-id="83e3e-115">L'operazione blit precedente che sta trasferendo informazioni da o verso questa superficie non è completa.</span><span class="sxs-lookup"><span data-stu-id="83e3e-115">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                                                   |
| <span data-ttu-id="83e3e-116">E \_ non riescono</span><span class="sxs-lookup"><span data-stu-id="83e3e-116">E\_FAIL</span></span>                                         | <span data-ttu-id="83e3e-117">Si è tentato di creare un dispositivo con il [livello di debug](d3d10-graphics-programming-guide-api-features-layers.md) abilitato e il livello non è installato.</span><span class="sxs-lookup"><span data-stu-id="83e3e-117">Attempted to create a device with the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) enabled and the layer is not installed.</span></span> |
| <span data-ttu-id="83e3e-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="83e3e-118">E\_INVALIDARG</span></span>                                   | <span data-ttu-id="83e3e-119">Un parametro non valido è stato passato alla funzione di restituzione.</span><span class="sxs-lookup"><span data-stu-id="83e3e-119">An invalid parameter was passed to the returning function.</span></span>                                                                                            |
| <span data-ttu-id="83e3e-120">E \_ OutOfMemory</span><span class="sxs-lookup"><span data-stu-id="83e3e-120">E\_OUTOFMEMORY</span></span>                                  | <span data-ttu-id="83e3e-121">Direct3D non è riuscito ad allocare memoria sufficiente per completare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="83e3e-121">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                                                   |
| <span data-ttu-id="83e3e-122">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="83e3e-122">E\_NOTIMPL</span></span>                                      | <span data-ttu-id="83e3e-123">La chiamata al metodo non viene implementata con la combinazione di parametri passata.</span><span class="sxs-lookup"><span data-stu-id="83e3e-123">The method call isn't implemented with the passed parameter combination.</span></span>                                                                              |
| <span data-ttu-id="83e3e-124">S \_ false</span><span class="sxs-lookup"><span data-stu-id="83e3e-124">S\_FALSE</span></span>                                        | <span data-ttu-id="83e3e-125">Valore di operazione riuscita alternativo, che indica un completamento positivo ma non standard (il significato esatto dipende dal contesto).</span><span class="sxs-lookup"><span data-stu-id="83e3e-125">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span>                                 |
| <span data-ttu-id="83e3e-126">\_OK</span><span class="sxs-lookup"><span data-stu-id="83e3e-126">S\_OK</span></span>                                           | <span data-ttu-id="83e3e-127">Non si sono verificati errori.</span><span class="sxs-lookup"><span data-stu-id="83e3e-127">No error occurred.</span></span>                                                                                                                                    |



 

<span data-ttu-id="83e3e-128">Per scrivere codice che gestisce [i valori HRESULT](../winprog/windows-data-types.md) in modo affidabile, usare le macro SUCCEEDED (HR) e failed (HR).</span><span class="sxs-lookup"><span data-stu-id="83e3e-128">To write code that handles [HRESULT values](../winprog/windows-data-types.md) robustly, use the SUCCEEDED(hr) and FAILED(hr) macros.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83e3e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83e3e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83e3e-130">Riferimento a Direct3D</span><span class="sxs-lookup"><span data-stu-id="83e3e-130">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[<span data-ttu-id="83e3e-131">Informazioni di riferimento su Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="83e3e-131">Reference for Direct3D 10</span></span>](d3d10-graphics-reference.md)
</dt> </dl>

 

 
