---
description: Flag della funzionalità di coordinate della trama del driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966315"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="d3230-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="d3230-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="d3230-104">Flag della funzionalità di coordinate della trama del driver.</span><span class="sxs-lookup"><span data-stu-id="d3230-104">Driver texture coordinate capability flags.</span></span>



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3230-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="d3230-105">\#define</span></span>                                 | <span data-ttu-id="d3230-106">Valore</span><span class="sxs-lookup"><span data-stu-id="d3230-106">Value</span></span>       | <span data-ttu-id="d3230-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3230-107">Description</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="d3230-108">D3DTSS \_ TCI \_ PassThru</span><span class="sxs-lookup"><span data-stu-id="d3230-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="d3230-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="d3230-109">0x00000000L</span></span> | <span data-ttu-id="d3230-110">Usare le coordinate di trama specificate contenute all'interno del formato del vertice.</span><span class="sxs-lookup"><span data-stu-id="d3230-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="d3230-111">Questo valore viene risolto in zero.</span><span class="sxs-lookup"><span data-stu-id="d3230-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="d3230-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="d3230-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="d3230-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="d3230-113">0x00010000L</span></span> | <span data-ttu-id="d3230-114">Usare il vertice normale, trasformato nello spazio della fotocamera, come coordinate di trama di input per la trasformazione di trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="d3230-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="d3230-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="d3230-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="d3230-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="d3230-116">0x00020000L</span></span> | <span data-ttu-id="d3230-117">Usare la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate di trama di input per la trasformazione di trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="d3230-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="d3230-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="d3230-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="d3230-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="d3230-119">0x00030000L</span></span> | <span data-ttu-id="d3230-120">Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinata di trama di input per la trasformazione di trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="d3230-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="d3230-121">Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale.</span><span class="sxs-lookup"><span data-stu-id="d3230-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="d3230-122">D3DTSS \_ TCI \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="d3230-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="d3230-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="d3230-123">0x00040000L</span></span> | <span data-ttu-id="d3230-124">Usare le coordinate di trama specificate per il mapping della sfera.</span><span class="sxs-lookup"><span data-stu-id="d3230-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="d3230-125">Queste costanti vengono usate da D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="d3230-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="d3230-126">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="d3230-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="d3230-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3230-127">Header</span></span>                   | <span data-ttu-id="d3230-128">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="d3230-128">d3d9caps.h</span></span> |
| <span data-ttu-id="d3230-129">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="d3230-129">Minimum operating system</span></span> | <span data-ttu-id="d3230-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d3230-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d3230-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3230-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3230-132">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="d3230-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



