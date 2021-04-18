---
description: Le applicazioni associano una fase di fusione a ogni trama nel set di trame correnti. Direct3D valuta ogni fase di fusione in ordine, iniziando dalla prima trama del set e terminando con l'ottavo.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Operazioni di combinazione di trame e argomenti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304192"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a><span data-ttu-id="d1f36-104">Operazioni di combinazione di trame e argomenti (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d1f36-104">Texture Blending Operations and Arguments (Direct3D 9)</span></span>

<span data-ttu-id="d1f36-105">Le applicazioni associano una fase di fusione a ogni trama nel set di trame correnti.</span><span class="sxs-lookup"><span data-stu-id="d1f36-105">Applications associate a blending stage with each texture in the set of current textures.</span></span> <span data-ttu-id="d1f36-106">Direct3D valuta ogni fase di fusione in ordine, iniziando dalla prima trama del set e terminando con l'ottavo.</span><span class="sxs-lookup"><span data-stu-id="d1f36-106">Direct3D evaluates each blending stage in order, beginning with the first texture in the set and ending with the eighth.</span></span>

<span data-ttu-id="d1f36-107">Direct3D applica le informazioni di ogni trama nel set di trame correnti alla fase di fusione a essa associata.</span><span class="sxs-lookup"><span data-stu-id="d1f36-107">Direct3D applies the information from each texture in the set of current textures to the blending stage that is associated with it.</span></span> <span data-ttu-id="d1f36-108">Le applicazioni controllano quali informazioni di una fase della trama vengono utilizzate chiamando [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="d1f36-108">Applications control what information from a texture stage is used by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api).</span></span> <span data-ttu-id="d1f36-109">È possibile impostare operazioni separate per i canali colore e alfa e ogni operazione utilizza due argomenti.</span><span class="sxs-lookup"><span data-stu-id="d1f36-109">You can set separate operations for the color and alpha channels, and each operation uses two arguments.</span></span> <span data-ttu-id="d1f36-110">Specificare le operazioni del canale colori utilizzando lo \_ stato della fase COLOROP di D3DTSS. specificare le operazioni alfa utilizzando D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="d1f36-110">Specify color channel operations by using the D3DTSS\_COLOROP stage state; specify alpha operations by using D3DTSS\_ALPHAOP.</span></span> <span data-ttu-id="d1f36-111">Entrambi gli Stati della fase utilizzano valori del tipo enumerato [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="d1f36-111">Both stage states use values from the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span>

<span data-ttu-id="d1f36-112">Gli argomenti di combinazione di trame utilizzano i \_ membri D3DTSS COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 e D3DTSS \_ ALPHARG2 del tipo enumerato [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="d1f36-112">Texture blending arguments use the D3DTSS\_COLORARG1, D3DTSS\_COLORARG2, D3DTSS\_ALPHARG1, and D3DTSS\_ALPHARG2 members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="d1f36-113">I valori degli argomenti corrispondenti vengono identificati utilizzando [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="d1f36-113">The corresponding argument values are identified using [D3DTA](d3dta.md).</span></span>

> [!Note]  
> <span data-ttu-id="d1f36-114">È possibile disabilitare una fase di trama e tutte le fasi successive di combinazione di trame in Cascade, impostando l'operazione relativa al colore per la fase su D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="d1f36-114">You can disable a texture stage - and any subsequent texture blending stages in the cascade - by setting the color operation for that stage to D3DTOP\_DISABLE.</span></span> <span data-ttu-id="d1f36-115">La disabilitazione dell'operazione di colore disattiva efficacemente anche l'operazione Alpha.</span><span class="sxs-lookup"><span data-stu-id="d1f36-115">Disabling the color operation effectively disables the alpha operation as well.</span></span> <span data-ttu-id="d1f36-116">Non è possibile disabilitare le operazioni Alpha quando sono abilitate le operazioni sui colori.</span><span class="sxs-lookup"><span data-stu-id="d1f36-116">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="d1f36-117">L'impostazione dell'operazione Alpha su D3DTOP \_ Disabilita quando è abilitata la fusione dei colori causa un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="d1f36-117">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

 

<span data-ttu-id="d1f36-118">Per determinare le operazioni di blending di trama supportate di un dispositivo, eseguire una query sul membro TextureCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="d1f36-118">To determine the supported texture blending operations of a device, query the TextureCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1f36-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1f36-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1f36-120">Combinazione di trame</span><span class="sxs-lookup"><span data-stu-id="d1f36-120">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
