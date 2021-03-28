---
title: Registro booleano costante (HLSL VS Reference)
description: Questo registro è una raccolta di bit utilizzati nelle istruzioni di controllo di flusso statiche, ad esempio, se bool-vs-else-vs-endif-vs.
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976751"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a><span data-ttu-id="0943a-103">Registro booleano costante (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="0943a-103">Constant Boolean register (HLSL VS reference)</span></span>

<span data-ttu-id="0943a-104">Questo registro è una raccolta di bit usati nelle istruzioni per il controllo di flusso statico (ad esempio, [se bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [endif-vs](endif---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="0943a-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - vs](if-bool---vs.md) - [else - vs](else---vs.md) - [endif - vs](endif---vs.md)).</span></span> <span data-ttu-id="0943a-105">Ne sono disponibili 16, pertanto uno shader può avere 16 condizioni di ramo indipendenti.</span><span class="sxs-lookup"><span data-stu-id="0943a-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="0943a-106">Possono essere impostate usando [defb-vs](defb---vs.md) o [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="0943a-106">They can be set using [defb - vs](defb---vs.md) or [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span></span>

<span data-ttu-id="0943a-107">Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0943a-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="0943a-108">Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="0943a-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="0943a-109">Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader.</span><span class="sxs-lookup"><span data-stu-id="0943a-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="0943a-110">Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="0943a-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="0943a-111">Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="0943a-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="0943a-112">Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="0943a-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="0943a-113">Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.</span><span class="sxs-lookup"><span data-stu-id="0943a-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0943a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0943a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0943a-115">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="0943a-115">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 