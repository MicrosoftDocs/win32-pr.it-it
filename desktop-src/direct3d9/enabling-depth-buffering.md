---
description: 'Dopo aver creato un buffer di profondità, come descritto in creazione di un buffer di profondità (Direct3D 9), è possibile abilitare la memorizzazione nel buffer di profondità chiamando il metodo IDirect3DDevice9:: SetRenderState.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Abilitazione del buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341426"
---
# <a name="enabling-depth-buffering-direct3d-9"></a><span data-ttu-id="07797-103">Abilitazione del buffer di profondità (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="07797-103">Enabling Depth Buffering (Direct3D 9)</span></span>

<span data-ttu-id="07797-104">Dopo aver creato un buffer di profondità, come descritto in [creazione di un buffer di profondità (Direct3D 9)](creating-a-depth-buffer.md), è possibile abilitare la memorizzazione nel buffer di profondità chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="07797-104">After you create a depth buffer, as described in [Creating a Depth Buffer (Direct3D 9)](creating-a-depth-buffer.md), you enable depth buffering by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="07797-105">Impostare lo \_ stato di rendering ZENABLE di D3DRS per abilitare il buffering di profondità.</span><span class="sxs-lookup"><span data-stu-id="07797-105">Set the D3DRS\_ZENABLE render state to enable depth-buffering.</span></span> <span data-ttu-id="07797-106">Usare il \_ membro D3DZB true del tipo enumerato [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (o **true**) per abilitare il buffering z, D3DZB \_ USEW per abilitare w-buffering oppure D3DZB \_ false (o **false**) per disabilitare il buffering di profondità.</span><span class="sxs-lookup"><span data-stu-id="07797-106">Use the D3DZB\_TRUE member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type (or **TRUE**) to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE (or **FALSE**) to disable depth buffering.</span></span>

> [!Note]  
> <span data-ttu-id="07797-107">Per usare il buffering w, l'applicazione deve impostare una matrice di proiezione conforme anche se non usa la pipeline di trasformazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="07797-107">To use w-buffering, your application must set a compliant projection matrix even if it doesn't use the Direct3D transformation pipeline.</span></span> <span data-ttu-id="07797-108">Per informazioni su come fornire una matrice di proiezione appropriata, vedere [una matrice di proiezione W-friendly](projection-transform.md)</span><span class="sxs-lookup"><span data-stu-id="07797-108">For information about providing an appropriate projection matrix, see [A W-Friendly Projection Matrix](projection-transform.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="07797-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07797-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07797-110">Buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="07797-110">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
