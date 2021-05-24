---
description: Le funzioni set Direct3D 10 non contengono un riferimento a un oggetto dispositivo-figlio.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Conteggio dei riferimenti (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335455"
---
# <a name="reference-counting-direct3d-10"></a><span data-ttu-id="94c8d-103">Conteggio dei riferimenti (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="94c8d-103">Reference Counting (Direct3D 10)</span></span>

<span data-ttu-id="94c8d-104">Le funzioni set Direct3D 10 non contengono un riferimento a un oggetto dispositivo-figlio.</span><span class="sxs-lookup"><span data-stu-id="94c8d-104">Direct3D 10 set functions do not hold a reference to a device-child object.</span></span> <span data-ttu-id="94c8d-105">Ciò significa che ogni applicazione deve contenere un riferimento a un oggetto dispositivo-figlio per tutto il tempo in cui l'oggetto deve essere associato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="94c8d-105">This means that each application must hold a reference to a device-child object for as long as the object needs to be bound to the pipeline.</span></span> <span data-ttu-id="94c8d-106">Quando il conteggio dei riferimenti di un oggetto scende a zero, l'oggetto verrà scollegato dalla pipeline ed eliminato.</span><span class="sxs-lookup"><span data-stu-id="94c8d-106">When the reference count of an object drops to zero, the object will be unbound from the pipeline and destroyed.</span></span> <span data-ttu-id="94c8d-107">Questo stile di riferimento che contiene è noto anche come delimitazione dei riferimenti deboli perché ogni percorso di associazione della pipeline contiene un riferimento debole all'interfaccia o all'oggetto associato.</span><span class="sxs-lookup"><span data-stu-id="94c8d-107">This style of reference holding is also known as weak-reference holding because each pipeline binding location holds a weak reference to the interface/object that is bound to it.</span></span>

<span data-ttu-id="94c8d-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="94c8d-108">For example:</span></span>


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





<span data-ttu-id="94c8d-109">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="94c8d-109">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="94c8d-110">In Direct3D 9 le funzioni set contengono un riferimento agli oggetti dispositivo; nelle funzioni set Direct3D 10 non contengono un riferimento agli oggetti dispositivo-figlio.</span><span class="sxs-lookup"><span data-stu-id="94c8d-110">In Direct3D 9, set functions hold a reference to the device objects; in Direct3D 10 set functions do not hold a reference to the device-child objects.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="94c8d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94c8d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94c8d-112">Funzionalità API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="94c8d-112">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




