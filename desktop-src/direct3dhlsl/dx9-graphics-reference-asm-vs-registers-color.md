---
title: Registro colori
description: Questi registri di output del vertex shader contengono un valore di colore.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104350871"
---
# <a name="color-register"></a><span data-ttu-id="fd0ad-103">Registro colori</span><span class="sxs-lookup"><span data-stu-id="fd0ad-103">Color Register</span></span>

<span data-ttu-id="fd0ad-104">Questi registri di output del vertex shader contengono un valore di colore.</span><span class="sxs-lookup"><span data-stu-id="fd0ad-104">These vertex shader output registers contain a color value.</span></span> 

| <span data-ttu-id="fd0ad-105">Registrazione</span><span class="sxs-lookup"><span data-stu-id="fd0ad-105">Register</span></span> | <span data-ttu-id="fd0ad-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd0ad-106">Description</span></span>              |
|----------|--------------------------|
| <span data-ttu-id="fd0ad-107">oD0</span><span class="sxs-lookup"><span data-stu-id="fd0ad-107">oD0</span></span>      | <span data-ttu-id="fd0ad-108">registro colori diffuso.</span><span class="sxs-lookup"><span data-stu-id="fd0ad-108">diffuse color register.</span></span>  |
| <span data-ttu-id="fd0ad-109">oD1</span><span class="sxs-lookup"><span data-stu-id="fd0ad-109">oD1</span></span>      | <span data-ttu-id="fd0ad-110">registro colori speculare.</span><span class="sxs-lookup"><span data-stu-id="fd0ad-110">specular color register.</span></span> |



 

<span data-ttu-id="fd0ad-111">Il valore oD0 viene interpolato e viene scritto nel registro colori pixel shader 0 (V0).</span><span class="sxs-lookup"><span data-stu-id="fd0ad-111">The oD0 value is interpolated and is written to the pixel shader color register 0 (v0).</span></span> <span data-ttu-id="fd0ad-112">Il valore oD1 viene interpolato e scritto nel registro colori pixel shader 1 (V1).</span><span class="sxs-lookup"><span data-stu-id="fd0ad-112">The oD1 value is interpolated and written to the pixel shader color register 1 (v1).</span></span> <span data-ttu-id="fd0ad-113">Per ulteriori informazioni sui registri dei colori pixel shader, vedere l'argomento pixel shader [Registro colori input](dx9-graphics-reference-asm-ps-registers-input-color.md) .</span><span class="sxs-lookup"><span data-stu-id="fd0ad-113">For more information about pixel shader color registers, see the pixel shader [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd0ad-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd0ad-114">Remarks</span></span>

<span data-ttu-id="fd0ad-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="fd0ad-115">Example</span></span>


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a><span data-ttu-id="fd0ad-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd0ad-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd0ad-117">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="fd0ad-117">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




