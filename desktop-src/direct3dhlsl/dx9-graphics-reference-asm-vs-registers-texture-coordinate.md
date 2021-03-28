---
title: Registro delle coordinate di trama (riferimento di HLSL VS)
description: Questo registro di output del vertex shader contiene coordinate di trama per vertice.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118355"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a><span data-ttu-id="50ddf-103">Registro delle coordinate di trama (riferimento di HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="50ddf-103">Texture Coordinate Register (HLSL VS reference)</span></span>

<span data-ttu-id="50ddf-104">Questo registro di output del vertex shader contiene coordinate di trama per vertice.</span><span class="sxs-lookup"><span data-stu-id="50ddf-104">This vertex shader output register contains per-vertex texture coordinates.</span></span>

<span data-ttu-id="50ddf-105">Un registro è costituito da proprietà che determinano il comportamento di ogni registro.</span><span class="sxs-lookup"><span data-stu-id="50ddf-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="50ddf-106">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50ddf-106">Property</span></span>        | <span data-ttu-id="50ddf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50ddf-107">Description</span></span>   |
|-----------------|---------------|
| <span data-ttu-id="50ddf-108">Nome</span><span class="sxs-lookup"><span data-stu-id="50ddf-108">Name</span></span>            | <span data-ttu-id="50ddf-109">oT0 - oT7</span><span class="sxs-lookup"><span data-stu-id="50ddf-109">oT0 - oT7</span></span>     |
| <span data-ttu-id="50ddf-110">Conteggio</span><span class="sxs-lookup"><span data-stu-id="50ddf-110">Count</span></span>           | <span data-ttu-id="50ddf-111">Otto vettori</span><span class="sxs-lookup"><span data-stu-id="50ddf-111">Eight vectors</span></span> |
| <span data-ttu-id="50ddf-112">Autorizzazioni di I/O</span><span class="sxs-lookup"><span data-stu-id="50ddf-112">I/O permissions</span></span> | <span data-ttu-id="50ddf-113">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="50ddf-113">Write-only</span></span>    |



 

<span data-ttu-id="50ddf-114">I registri delle coordinate di trama di output sono una matrice di registri di dati di output.</span><span class="sxs-lookup"><span data-stu-id="50ddf-114">The output texture coordinates registers are an array of output data registers.</span></span> <span data-ttu-id="50ddf-115">I dati del registro vengono iterati e usati come coordinate di trama dalle fasi di campionamento della trama per fornire i dati al pixel shader.</span><span class="sxs-lookup"><span data-stu-id="50ddf-115">The register data is iterated and used as texture coordinates by the texture sampling stages to supply data to the pixel shader.</span></span>

<span data-ttu-id="50ddf-116">Quando si scrive in un registro delle coordinate di trama, si consiglia di passare solo il numero di valori a virgola mobile della dimensione della mappa di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="50ddf-116">When writing to a texture coordinate register, it is recommended that you pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="50ddf-117">Controllare i valori passati con un modificatore.</span><span class="sxs-lookup"><span data-stu-id="50ddf-117">Control the values that are passed with a modifier.</span></span> <span data-ttu-id="50ddf-118">Ad esempio, usare. XY per una mappa di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="50ddf-118">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="50ddf-119">I flag della pipeline dei vertici della funzione fissa, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF COUNT2, D3DTTFF COUNT3 \_ \_ , D3DTTFF \_ COUNT4), devono essere impostati su zero se si utilizza un vertex shader programmabile.</span><span class="sxs-lookup"><span data-stu-id="50ddf-119">The fixed function vertex pipeline flags, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF\_COUNT1, D3DTTFF\_COUNT2, D3DTTFF\_COUNT3, D3DTTFF\_COUNT4), should be set to zero if you are using a programmable vertex shader.</span></span>

<span data-ttu-id="50ddf-120">I dati dei vertici degli oggetti forniscono coordinate di trama di input.</span><span class="sxs-lookup"><span data-stu-id="50ddf-120">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="50ddf-121">Per gli oggetti che non utilizzano trame affiancate sono in genere presenti coordinate di trama nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="50ddf-121">Objects that do not use tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="50ddf-122">Gli oggetti che utilizzano trame affiancate, ad esempio il terreno, in genere presentano coordinate di trama che variano da \[ -n, + n \] dove n può essere qualsiasi numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="50ddf-122">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-n,+n\] where n can be any floating point number.</span></span>

<span data-ttu-id="50ddf-123">L'interpolazione delle coordinate di trama viene eseguita sui dati dei vertici per la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="50ddf-123">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="50ddf-124">Durante la rasterizzazione, le coordinate di trama vengono interpolate tra i vertici degli oggetti, modificati dal wrapping della trama e ridimensionate in base alle dimensioni della trama (tenendo conto delle modalità di indirizzamento della trama) per produrre un indice Integer.</span><span class="sxs-lookup"><span data-stu-id="50ddf-124">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping, and scaled by the texture size (also taking into account texture addressing modes) to produce an integer index.</span></span> <span data-ttu-id="50ddf-125">L'indice viene quindi utilizzato per eseguire una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="50ddf-125">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="50ddf-126">Usare il valore MaxTextureRepeat in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) per determinare il numero di volte in cui una trama può essere affiancata.</span><span class="sxs-lookup"><span data-stu-id="50ddf-126">Use the MaxTextureRepeat value in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) to determine how many times a texture can be tiled.</span></span>

## <a name="example"></a><span data-ttu-id="50ddf-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="50ddf-127">Example</span></span>

<span data-ttu-id="50ddf-128">Dichiarare il registro delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="50ddf-128">Declare the texture coordinate register.</span></span>


```
dcl_texcoord v7
```



<span data-ttu-id="50ddf-129">Copiare le coordinate di trama per vertice nel registro di output.</span><span class="sxs-lookup"><span data-stu-id="50ddf-129">Copy the per-vertex texture coordinates to the output register.</span></span>


```
mov oT0, v7
```





| <span data-ttu-id="50ddf-130">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="50ddf-130">Vertex shader versions</span></span>      | <span data-ttu-id="50ddf-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="50ddf-131">1\_1</span></span> | <span data-ttu-id="50ddf-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="50ddf-132">2\_0</span></span> | <span data-ttu-id="50ddf-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="50ddf-133">2\_sw</span></span> | <span data-ttu-id="50ddf-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="50ddf-134">2\_x</span></span> | <span data-ttu-id="50ddf-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="50ddf-135">3\_0</span></span> | <span data-ttu-id="50ddf-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="50ddf-136">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="50ddf-137">Registro coordinate trama</span><span class="sxs-lookup"><span data-stu-id="50ddf-137">Texture Coordinate Register</span></span> | <span data-ttu-id="50ddf-138">x</span><span class="sxs-lookup"><span data-stu-id="50ddf-138">x</span></span>    | <span data-ttu-id="50ddf-139">x</span><span class="sxs-lookup"><span data-stu-id="50ddf-139">x</span></span>    | <span data-ttu-id="50ddf-140">x</span><span class="sxs-lookup"><span data-stu-id="50ddf-140">x</span></span>     | <span data-ttu-id="50ddf-141">x</span><span class="sxs-lookup"><span data-stu-id="50ddf-141">x</span></span>    | <span data-ttu-id="50ddf-142">x</span><span class="sxs-lookup"><span data-stu-id="50ddf-142">x</span></span>    | <span data-ttu-id="50ddf-143">x</span><span class="sxs-lookup"><span data-stu-id="50ddf-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="50ddf-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50ddf-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50ddf-145">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="50ddf-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 