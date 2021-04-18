---
description: L'illuminazione emissivo è descritta da un singolo termine.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Illuminazione emissivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303680"
---
# <a name="emissive-lighting-direct3d-9"></a><span data-ttu-id="a5c87-103">Illuminazione emissivo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a5c87-103">Emissive Lighting (Direct3D 9)</span></span>

<span data-ttu-id="a5c87-104">L'illuminazione emissivo è descritta da un singolo termine.</span><span class="sxs-lookup"><span data-stu-id="a5c87-104">Emissive lighting is described by a single term.</span></span>

<span data-ttu-id="a5c87-105">Illuminazione emissivo = C ₑ</span><span class="sxs-lookup"><span data-stu-id="a5c87-105">Emissive Lighting = Cₑ</span></span>

<span data-ttu-id="a5c87-106">Dove:</span><span class="sxs-lookup"><span data-stu-id="a5c87-106">Where:</span></span>



| <span data-ttu-id="a5c87-107">Parametro</span><span class="sxs-lookup"><span data-stu-id="a5c87-107">Parameter</span></span> | <span data-ttu-id="a5c87-108">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="a5c87-108">Default value</span></span> | <span data-ttu-id="a5c87-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5c87-109">Type</span></span>          | <span data-ttu-id="a5c87-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5c87-110">Description</span></span>     |
|-----------|---------------|---------------|-----------------|
| <span data-ttu-id="a5c87-111">C ₑ</span><span class="sxs-lookup"><span data-stu-id="a5c87-111">Cₑ</span></span>        | <span data-ttu-id="a5c87-112">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="a5c87-112">(0,0,0,0)</span></span>     | <span data-ttu-id="a5c87-113">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="a5c87-113">D3DCOLORVALUE</span></span> | <span data-ttu-id="a5c87-114">Colore emissivo.</span><span class="sxs-lookup"><span data-stu-id="a5c87-114">Emissive color.</span></span> |



 

<span data-ttu-id="a5c87-115">Il valore per C ₑ è:</span><span class="sxs-lookup"><span data-stu-id="a5c87-115">The value for Cₑ is either:</span></span>

-   <span data-ttu-id="a5c87-116">Vertex color1, se EMISSIVEMATERIALSOURCE = D3DMCS \_ color1 e il primo colore del vertice viene specificato nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="a5c87-116">vertex color1, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="a5c87-117">Vertex color2, se EMISSIVEMATERIALSOURCE = D3DMCS \_ color2, e il secondo colore del vertice viene specificato nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="a5c87-117">vertex color2, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="a5c87-118">colore emissivo materiale</span><span class="sxs-lookup"><span data-stu-id="a5c87-118">material emissive color</span></span>

> [!Note]  
> <span data-ttu-id="a5c87-119">Se viene usata l'opzione EMISSIVEMATERIALSOURCE e il colore del vertice non viene specificato, viene usato il colore emissivo del materiale.</span><span class="sxs-lookup"><span data-stu-id="a5c87-119">If either EMISSIVEMATERIALSOURCE option is used, and the vertex color is not provided, the material emissive color is used.</span></span>

 

## <a name="example"></a><span data-ttu-id="a5c87-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="a5c87-120">Example</span></span>

<span data-ttu-id="a5c87-121">In questo esempio, l'oggetto è colorato usando la luce ambientale della scena e un colore di ambiente di materiale.</span><span class="sxs-lookup"><span data-stu-id="a5c87-121">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span> <span data-ttu-id="a5c87-122">Il codice è illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="a5c87-122">The code is shown below.</span></span>


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="a5c87-123">In base all'equazione, il colore risultante per i vertici dell'oggetto è il colore del materiale.</span><span class="sxs-lookup"><span data-stu-id="a5c87-123">According to the equation, the resulting color for the object vertices is the material color.</span></span>

<span data-ttu-id="a5c87-124">Nella figura seguente viene illustrato il colore del materiale, che è verde.</span><span class="sxs-lookup"><span data-stu-id="a5c87-124">The following illustration shows the material color, which is green.</span></span> <span data-ttu-id="a5c87-125">Emissivo illumina tutti i vertici degli oggetti con lo stesso colore.</span><span class="sxs-lookup"><span data-stu-id="a5c87-125">Emissive light lights all object vertices with the same color.</span></span> <span data-ttu-id="a5c87-126">Non dipende dal vertice normale o dalla direzione della luce.</span><span class="sxs-lookup"><span data-stu-id="a5c87-126">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="a5c87-127">Di conseguenza, la sfera appare come un cerchio 2D perché non esiste alcuna differenza nell'ombreggiatura intorno alla superficie dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a5c87-127">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![illustrazione di una sfera verde](images/lighte.jpg)

<span data-ttu-id="a5c87-129">Nell'illustrazione seguente viene illustrato il modo in cui emissivo Light si integra con gli altri tre tipi di luci, dagli esempi precedenti.</span><span class="sxs-lookup"><span data-stu-id="a5c87-129">The following illustration shows how the emissive light blends with the other three types of lights, from the previous examples.</span></span> <span data-ttu-id="a5c87-130">Sul lato destro della sfera è presente una Blend della emissivo verde e della luce di ambiente rossa.</span><span class="sxs-lookup"><span data-stu-id="a5c87-130">On the right side of the sphere, there is a blend of the green emissive and the red ambient light.</span></span> <span data-ttu-id="a5c87-131">Sul lato sinistro della sfera, il verde emissivo chiaro si fonde con l'ambiente rosso e la luce diffusa che produce una sfumatura rossa.</span><span class="sxs-lookup"><span data-stu-id="a5c87-131">On the left side of the sphere, the green emissive light blends with red ambient and diffuse light producing a red gradient.</span></span> <span data-ttu-id="a5c87-132">L'evidenziazione speculare è bianca al centro e crea un anello giallo, perché il valore della luce speculare cade in modo nitido lasciando inalterati i valori dell'ambiente, della diffusione e della luce emissivo che si fondono per essere gialli.</span><span class="sxs-lookup"><span data-stu-id="a5c87-132">The specular highlight is white in the center and creates a yellow ring as the specular light value falls off sharply leaving the ambient, diffuse and emissive light values which blend together to make yellow.</span></span>

![illustrazione di una sfera verde con emissivo Light](images/lightadse.jpg)

## <a name="related-topics"></a><span data-ttu-id="a5c87-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5c87-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5c87-135">Matematica dell'illuminazione</span><span class="sxs-lookup"><span data-stu-id="a5c87-135">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



