---
title: Registro di tipo Integer costante (riferimento di HLSL VS)
description: I registri di tipo integer costanti vengono usati solo da loop-vs e Rep-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976775"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a><span data-ttu-id="f927a-103">Registro di tipo Integer costante (riferimento di HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="f927a-103">Constant Integer Register (HLSL VS reference)</span></span>

<span data-ttu-id="f927a-104">I registri di tipo integer costanti vengono usati solo da [loop-vs](loop---vs.md) e [Rep-vs](rep---vs.md).</span><span class="sxs-lookup"><span data-stu-id="f927a-104">Constant integer registers are used only by [loop - vs](loop---vs.md) and [rep - vs](rep---vs.md).</span></span>

<span data-ttu-id="f927a-105">Possono essere impostate tramite [defi-vs](defi---vs.md) o [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="f927a-105">They can be set using [defi - vs](defi---vs.md) or [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span></span>

<span data-ttu-id="f927a-106">Quando viene usato come argomento dell'istruzione [loop-vs](loop---vs.md) :</span><span class="sxs-lookup"><span data-stu-id="f927a-106">When used as an argument to the [loop - vs](loop---vs.md) instruction:</span></span>

-   <span data-ttu-id="f927a-107">. x è il numero di iterazioni.</span><span class="sxs-lookup"><span data-stu-id="f927a-107">.x is the iteration count.</span></span> <span data-ttu-id="f927a-108">([Rep-vs](rep---vs.md) usa solo questo componente).</span><span class="sxs-lookup"><span data-stu-id="f927a-108">([rep - vs](rep---vs.md) uses only this component).</span></span>
-   <span data-ttu-id="f927a-109">. y è il valore iniziale del contatore di cicli.</span><span class="sxs-lookup"><span data-stu-id="f927a-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="f927a-110">. z è il passaggio di incremento per il contatore del ciclo.</span><span class="sxs-lookup"><span data-stu-id="f927a-110">.z is the increment step for the loop counter.</span></span>

<span data-ttu-id="f927a-111">Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="f927a-111">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="f927a-112">Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="f927a-112">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="f927a-113">Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader.</span><span class="sxs-lookup"><span data-stu-id="f927a-113">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="f927a-114">Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="f927a-114">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="f927a-115">Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="f927a-115">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="f927a-116">Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="f927a-116">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="f927a-117">Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.</span><span class="sxs-lookup"><span data-stu-id="f927a-117">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f927a-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f927a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f927a-119">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="f927a-119">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 