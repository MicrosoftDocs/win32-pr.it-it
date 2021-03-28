---
title: Registro float costante (HLSL VS Reference)
description: Registro di input vertex shader per una costante a virgola mobile a quattro componenti. Impostare un registro costante con def-vs o SetVertexShaderConstantF.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 856c9567070a071a123b28279342fd9cbbb0f6af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399174"
---
# <a name="constant-float-register-hlsl-vs-reference"></a><span data-ttu-id="59c49-104">Registro float costante (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="59c49-104">Constant float register (HLSL VS reference)</span></span>

<span data-ttu-id="59c49-105">Registro di input vertex shader per una costante a virgola mobile a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="59c49-105">Vertex shader input register for a four component floating-point constant.</span></span> <span data-ttu-id="59c49-106">Impostare un registro costante con [def-vs](def---vs.md) o [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="59c49-106">Set a constant register with either [def - vs](def---vs.md) or [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span></span>

<span data-ttu-id="59c49-107">Il file di registro delle costanti è di sola lettura dal punto di vista del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="59c49-107">The constant register file is read-only from the perspective of the vertex shader.</span></span> <span data-ttu-id="59c49-108">Ogni singola istruzione può accedere a un solo registro costante.</span><span class="sxs-lookup"><span data-stu-id="59c49-108">Any single instruction may access only one constant register.</span></span> <span data-ttu-id="59c49-109">Tuttavia, ogni origine in tale istruzione può swizzle in modo indipendente e negare il vettore mentre viene letto.</span><span class="sxs-lookup"><span data-stu-id="59c49-109">However, each source in that instruction may independently swizzle and negate that vector as it is read.</span></span>

<span data-ttu-id="59c49-110">Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="59c49-110">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="59c49-111">Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="59c49-111">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="59c49-112">Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader.</span><span class="sxs-lookup"><span data-stu-id="59c49-112">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="59c49-113">Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="59c49-113">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="59c49-114">Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.</span><span class="sxs-lookup"><span data-stu-id="59c49-114">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="59c49-115">Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader.</span><span class="sxs-lookup"><span data-stu-id="59c49-115">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="59c49-116">Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.</span><span class="sxs-lookup"><span data-stu-id="59c49-116">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

<span data-ttu-id="59c49-117">Un registro costante viene designato come assoluto o relativo:</span><span class="sxs-lookup"><span data-stu-id="59c49-117">A constant register is designated as either absolute or relative:</span></span>


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



<span data-ttu-id="59c49-118">Il registro costante può essere letto, quindi, usando un indice assoluto o un indice relativo da un registro indirizzi.</span><span class="sxs-lookup"><span data-stu-id="59c49-118">The constant register can be read, therefore, either by using an absolute index or with a relative index from an address register.</span></span> <span data-ttu-id="59c49-119">Le letture dei registri fuori intervallo restituiscono (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="59c49-119">Reads from out-of-range registers return (0.0, 0.0, 0.0, 0.0).</span></span>

## <a name="examples"></a><span data-ttu-id="59c49-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="59c49-120">Examples</span></span>

<span data-ttu-id="59c49-121">Di seguito è riportato un esempio che dichiara due costanti a virgola mobile all'interno di uno shader.</span><span class="sxs-lookup"><span data-stu-id="59c49-121">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="59c49-122">Queste costanti vengono caricate ogni volta che viene chiamato [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .</span><span class="sxs-lookup"><span data-stu-id="59c49-122">These constants are loaded every time [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) is called.</span></span>

<span data-ttu-id="59c49-123">Di seguito è riportato un esempio di utilizzo dell'API.</span><span class="sxs-lookup"><span data-stu-id="59c49-123">Here is an example using the API.</span></span>


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



<span data-ttu-id="59c49-124">Se si impostano valori costanti con l'API, non è necessaria alcuna dichiarazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="59c49-124">If you are setting constant values with the API, there is no shader declaration required.</span></span>



| <span data-ttu-id="59c49-125">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="59c49-125">Vertex shader versions</span></span> | <span data-ttu-id="59c49-126">1\_1</span><span class="sxs-lookup"><span data-stu-id="59c49-126">1\_1</span></span> | <span data-ttu-id="59c49-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59c49-127">2\_0</span></span> | <span data-ttu-id="59c49-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="59c49-128">2\_sw</span></span> | <span data-ttu-id="59c49-129">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="59c49-129">2\_x</span></span> | <span data-ttu-id="59c49-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59c49-130">3\_0</span></span> | <span data-ttu-id="59c49-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="59c49-131">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="59c49-132">Registro costanti</span><span class="sxs-lookup"><span data-stu-id="59c49-132">Constant Register</span></span>      | <span data-ttu-id="59c49-133">x</span><span class="sxs-lookup"><span data-stu-id="59c49-133">x</span></span>    | <span data-ttu-id="59c49-134">x</span><span class="sxs-lookup"><span data-stu-id="59c49-134">x</span></span>    | <span data-ttu-id="59c49-135">x</span><span class="sxs-lookup"><span data-stu-id="59c49-135">x</span></span>     | <span data-ttu-id="59c49-136">x</span><span class="sxs-lookup"><span data-stu-id="59c49-136">x</span></span>    | <span data-ttu-id="59c49-137">x</span><span class="sxs-lookup"><span data-stu-id="59c49-137">x</span></span>    | <span data-ttu-id="59c49-138">x</span><span class="sxs-lookup"><span data-stu-id="59c49-138">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="59c49-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59c49-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59c49-140">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="59c49-140">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 