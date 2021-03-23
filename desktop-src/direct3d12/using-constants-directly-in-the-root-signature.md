---
title: Uso di costanti direttamente nella firma radice
description: Le applicazioni possono definire costanti radice nella firma radice, ognuna come un set di valori a 32 bit. Vengono visualizzati in HLSL (High Level Shading Language) come buffer costante. Si noti che i buffer costanti per motivi cronologici vengono visualizzati come set di valori a 4x32 bit.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103504"
---
# <a name="using-constants-directly-in-the-root-signature"></a><span data-ttu-id="5ddea-105">Uso di costanti direttamente nella firma radice</span><span class="sxs-lookup"><span data-stu-id="5ddea-105">Using Constants Directly in the Root Signature</span></span>

<span data-ttu-id="5ddea-106">Le applicazioni possono definire costanti radice nella firma radice, ognuna come un set di valori a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5ddea-106">Applications can define root constants in the root signature, each as a set of 32-bit values.</span></span> <span data-ttu-id="5ddea-107">Vengono visualizzati in HLSL (High Level Shading Language) come buffer costante.</span><span class="sxs-lookup"><span data-stu-id="5ddea-107">They appear in High Level Shading Language (HLSL) as a constant buffer.</span></span> <span data-ttu-id="5ddea-108">Si noti che i buffer costanti per motivi cronologici vengono visualizzati come set di valori a 4x32 bit.</span><span class="sxs-lookup"><span data-stu-id="5ddea-108">Note that constant buffers for historical reasons are viewed as sets of 4x32-bit values.</span></span>

<span data-ttu-id="5ddea-109">Ogni set di costanti utente viene considerato come una matrice scalare di valori a 32 bit, indicizzabile dinamicamente e in sola lettura dallo shader.</span><span class="sxs-lookup"><span data-stu-id="5ddea-109">Each set of user constants is treated as a scalar array of 32 -bit values, dynamically indexable and read-only from the shader.</span></span> <span data-ttu-id="5ddea-110">L'indicizzazione fuori limite di un determinato set di costanti radice produce risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="5ddea-110">Out of bounds indexing a given set of root constants produces undefined results.</span></span> <span data-ttu-id="5ddea-111">In HLSL è possibile fornire le definizioni della struttura dei dati affinché le costanti utente forniscano i tipi.</span><span class="sxs-lookup"><span data-stu-id="5ddea-111">In HLSL, data structure definitions can be provided for the user constants to give them types.</span></span> <span data-ttu-id="5ddea-112">Se, ad esempio, la firma radice definisce un set di 4 costanti radice, HLSL può sovrapporsi la struttura seguente.</span><span class="sxs-lookup"><span data-stu-id="5ddea-112">For example, if the root signature defines a set of 4 root constants, HLSL can overlay the following structure on them.</span></span>

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

<span data-ttu-id="5ddea-113">Le matrici non sono consentite nei buffer costanti per i quali viene eseguito il mapping alle costanti radice perché l'indicizzazione dinamica nello spazio della firma radice non è supportata.</span><span class="sxs-lookup"><span data-stu-id="5ddea-113">Arrays are not permitted in constant buffers that get mapped onto root constants since dynamic indexing in the root signature space is not supported.</span></span> <span data-ttu-id="5ddea-114">Ad esempio, non è valido avere una voce nel buffer costante come `float myArray[2];` .</span><span class="sxs-lookup"><span data-stu-id="5ddea-114">For example, it is invalid to have an entry in the constant buffer like `float myArray[2];`.</span></span> <span data-ttu-id="5ddea-115">Un buffer costante di cui è stato eseguito il mapping alle costanti radice non può essere una matrice; non è pertanto possibile eseguire il mapping `cbuffer myCBArray[2]` in costanti radice.</span><span class="sxs-lookup"><span data-stu-id="5ddea-115">A constant buffer that is mapped to root constants cannot itself be an array; therefore, it is invalid to map `cbuffer myCBArray[2]` into root constants.</span></span>

<span data-ttu-id="5ddea-116">Le costanti possono essere impostate parzialmente.</span><span class="sxs-lookup"><span data-stu-id="5ddea-116">Constants can be partially set.</span></span> <span data-ttu-id="5ddea-117">Se, ad esempio, la firma radice definisce valori a 4 32 bit in *RootTableBindSlot* 2, è possibile impostare qualsiasi subset delle quattro costanti alla volta, mentre le altre restano invariate.</span><span class="sxs-lookup"><span data-stu-id="5ddea-117">For example, if the root signature defines four 32-bit values at *RootTableBindSlot* 2, then any subset of the four constants can be set at a time (the others remain unchanged).</span></span> <span data-ttu-id="5ddea-118">Questa operazione può essere utile nei bundle che ereditano lo stato della firma radice e possono essere modificati parzialmente.</span><span class="sxs-lookup"><span data-stu-id="5ddea-118">This can be useful in bundles that inherit root signature state and can partially change it.</span></span>

<span data-ttu-id="5ddea-119">Quando si impostano le costanti, prestare attenzione al layout del buffer costante previsto dallo shader.</span><span class="sxs-lookup"><span data-stu-id="5ddea-119">When setting constants be careful of the constant buffer layout expected by the shader.</span></span> <span data-ttu-id="5ddea-120">È possibile, ad esempio, che le costanti vengano riempite a `vec4` limiti.</span><span class="sxs-lookup"><span data-stu-id="5ddea-120">It is possible that constants are padded to `vec4` boundaries, for example.</span></span> <span data-ttu-id="5ddea-121">Per verificare il layout previsto, controllare le informazioni di Reflection dallo shader HLSL.</span><span class="sxs-lookup"><span data-stu-id="5ddea-121">To verify the layout expected, check the reflection information from the HLSL shader.</span></span>

<span data-ttu-id="5ddea-122">Le API seguenti (dall'interfaccia [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) si riportano nell'impostazione delle costanti direttamente nella firma radice:</span><span class="sxs-lookup"><span data-stu-id="5ddea-122">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting constants directly on the root signature:</span></span>

-   [<span data-ttu-id="5ddea-123">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="5ddea-123">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [<span data-ttu-id="5ddea-124">**SetGraphicsRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="5ddea-124">**SetGraphicsRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [<span data-ttu-id="5ddea-125">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="5ddea-125">**SetComputeRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="5ddea-126">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="5ddea-126">**SetComputeRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

<span data-ttu-id="5ddea-127">Vedere anche la struttura delle [**\_ \_ costanti radice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="5ddea-127">Also, refer to the [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ddea-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ddea-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ddea-129">Firme radice</span><span class="sxs-lookup"><span data-stu-id="5ddea-129">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




