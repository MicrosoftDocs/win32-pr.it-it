---
title: Registro float costante (riferimenti per HLSL PS)
description: Registro di input del pixel shader per una costante a virgola mobile 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399461"
---
# <a name="constant-float-register-hlsl-ps-reference"></a><span data-ttu-id="7adc7-103">Registro float costante (riferimenti per HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="7adc7-103">Constant float register (HLSL PS reference)</span></span>

<span data-ttu-id="7adc7-104">Registro di input del pixel shader per una costante a virgola mobile 4D.</span><span class="sxs-lookup"><span data-stu-id="7adc7-104">Pixel shader input register for a 4D floating-point constant.</span></span>

<span data-ttu-id="7adc7-105">Possono essere impostate con [def-PS](def---ps.md) o [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="7adc7-105">They can be set using [def - ps](def---ps.md) or [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="7adc7-106">Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="7adc7-106">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="7adc7-107">Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="7adc7-107">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="7adc7-108">Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader.</span><span class="sxs-lookup"><span data-stu-id="7adc7-108">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="7adc7-109">Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="7adc7-109">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="7adc7-110">Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="7adc7-110">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="7adc7-111">Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="7adc7-111">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="7adc7-112">Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.</span><span class="sxs-lookup"><span data-stu-id="7adc7-112">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="examples"></a><span data-ttu-id="7adc7-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="7adc7-113">Examples</span></span>

<span data-ttu-id="7adc7-114">Di seguito è riportato un esempio che dichiara due costanti a virgola mobile all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="7adc7-114">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="7adc7-115">Queste costanti vengono caricate ogni volta che viene chiamato [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) .</span><span class="sxs-lookup"><span data-stu-id="7adc7-115">These constants are loaded every time [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) is called.</span></span>

<span data-ttu-id="7adc7-116">Se si impostano valori costanti con l'API, non è necessaria alcuna dichiarazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="7adc7-116">If you are setting constant values with the API, there is no shader declaration required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7adc7-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7adc7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7adc7-118">Registri</span><span class="sxs-lookup"><span data-stu-id="7adc7-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 