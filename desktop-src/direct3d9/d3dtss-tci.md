---
description: Flag di funzionalità delle coordinate della trama del driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da9ca23ebc4dd121527721a9d10a2db55a4d555
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995258"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="c60ab-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="c60ab-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="c60ab-104">Flag di funzionalità delle coordinate della trama del driver.</span><span class="sxs-lookup"><span data-stu-id="c60ab-104">Driver texture coordinate capability flags.</span></span>



| <span data-ttu-id="c60ab-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="c60ab-105">\#define</span></span>                                 | <span data-ttu-id="c60ab-106">Valore</span><span class="sxs-lookup"><span data-stu-id="c60ab-106">Value</span></span>       | <span data-ttu-id="c60ab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c60ab-107">Description</span></span>                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c60ab-108">D3DTSS \_ TCI \_ PASSTHRU</span><span class="sxs-lookup"><span data-stu-id="c60ab-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="c60ab-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="c60ab-109">0x00000000L</span></span> | <span data-ttu-id="c60ab-110">Usare le coordinate di trama specificate contenute nel formato vertice.</span><span class="sxs-lookup"><span data-stu-id="c60ab-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="c60ab-111">Questo valore viene risolto in zero.</span><span class="sxs-lookup"><span data-stu-id="c60ab-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="c60ab-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="c60ab-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="c60ab-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="c60ab-113">0x00010000L</span></span> | <span data-ttu-id="c60ab-114">Usa la normale del vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input per la trasformazione della trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="c60ab-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="c60ab-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="c60ab-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="c60ab-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="c60ab-116">0x00020000L</span></span> | <span data-ttu-id="c60ab-117">Usa la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input per la trasformazione della trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="c60ab-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="c60ab-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="c60ab-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="c60ab-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="c60ab-119">0x00030000L</span></span> | <span data-ttu-id="c60ab-120">Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinata della trama di input per la trasformazione della trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="c60ab-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="c60ab-121">Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale.</span><span class="sxs-lookup"><span data-stu-id="c60ab-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="c60ab-122">MAPPA \_ SPHEREMAP TCI D3DTSS \_</span><span class="sxs-lookup"><span data-stu-id="c60ab-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="c60ab-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="c60ab-123">0x00040000L</span></span> | <span data-ttu-id="c60ab-124">Usare le coordinate di trama specificate per il mapping della sfera.</span><span class="sxs-lookup"><span data-stu-id="c60ab-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="c60ab-125">Queste costanti vengono usate da D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="c60ab-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="c60ab-126">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="c60ab-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="c60ab-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c60ab-127">Header</span></span>                   | <span data-ttu-id="c60ab-128">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="c60ab-128">d3d9caps.h</span></span> |
| <span data-ttu-id="c60ab-129">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="c60ab-129">Minimum operating system</span></span> | <span data-ttu-id="c60ab-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c60ab-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c60ab-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c60ab-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c60ab-132">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="c60ab-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



