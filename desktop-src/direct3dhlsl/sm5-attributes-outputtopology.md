---
title: outputtopology
description: Definisce il tipo primitivo di output per mosaico.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956075"
---
# <a name="outputtopology"></a><span data-ttu-id="188e7-103">outputtopology</span><span class="sxs-lookup"><span data-stu-id="188e7-103">outputtopology</span></span>

<span data-ttu-id="188e7-104">Definisce il tipo primitivo di output per mosaico.</span><span class="sxs-lookup"><span data-stu-id="188e7-104">Defines the output primitive type for the tessellator.</span></span>


```
outputtopology(X)      
```



## <a name="remarks"></a><span data-ttu-id="188e7-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="188e7-105">Remarks</span></span>

<span data-ttu-id="188e7-106">X deve essere un [**punto**](dx-graphics-hlsl-geometry-shader.md), **una linea**, un **triangolo in \_ senso orario** o un **triangolo \_ CCW** e deve essere racchiuso tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="188e7-106">X must be either [**point**](dx-graphics-hlsl-geometry-shader.md), **line**, **triangle\_cw**, or **triangle\_ccw** and must be inside quotes.</span></span> <span data-ttu-id="188e7-107">Di seguito sono riportate le opzioni valide per l'attributo:</span><span class="sxs-lookup"><span data-stu-id="188e7-107">Here are the valid options for this attribute:</span></span>


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



<span data-ttu-id="188e7-108">Questo attributo è supportato nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="188e7-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="188e7-109">Vertice</span><span class="sxs-lookup"><span data-stu-id="188e7-109">Vertex</span></span> | <span data-ttu-id="188e7-110">Hull</span><span class="sxs-lookup"><span data-stu-id="188e7-110">Hull</span></span> | <span data-ttu-id="188e7-111">Dominio</span><span class="sxs-lookup"><span data-stu-id="188e7-111">Domain</span></span> | <span data-ttu-id="188e7-112">Geometria</span><span class="sxs-lookup"><span data-stu-id="188e7-112">Geometry</span></span> | <span data-ttu-id="188e7-113">Pixel</span><span class="sxs-lookup"><span data-stu-id="188e7-113">Pixel</span></span> | <span data-ttu-id="188e7-114">Calcolo</span><span class="sxs-lookup"><span data-stu-id="188e7-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="188e7-115">x</span><span class="sxs-lookup"><span data-stu-id="188e7-115">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="188e7-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="188e7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="188e7-117">Attributi del modello di shader 5</span><span class="sxs-lookup"><span data-stu-id="188e7-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="188e7-118">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="188e7-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




