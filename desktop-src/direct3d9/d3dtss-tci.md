---
description: Flag di funzionalità delle coordinate della trama del driver.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58746f17eb18b679a4dfe4957ac46236baeec35d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342976"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="65f13-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="65f13-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="65f13-104">Flag di funzionalità delle coordinate della trama del driver.</span><span class="sxs-lookup"><span data-stu-id="65f13-104">Driver texture coordinate capability flags.</span></span>



| <span data-ttu-id="65f13-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="65f13-105">\#define</span></span>                                 | <span data-ttu-id="65f13-106">Valore</span><span class="sxs-lookup"><span data-stu-id="65f13-106">Value</span></span>       | <span data-ttu-id="65f13-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65f13-107">Description</span></span>                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f13-108">D3DTSS \_ TCI \_ PASSTHRU</span><span class="sxs-lookup"><span data-stu-id="65f13-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="65f13-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="65f13-109">0x00000000L</span></span> | <span data-ttu-id="65f13-110">Usare le coordinate di trama specificate contenute nel formato vertice.</span><span class="sxs-lookup"><span data-stu-id="65f13-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="65f13-111">Questo valore viene risolto in zero.</span><span class="sxs-lookup"><span data-stu-id="65f13-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="65f13-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="65f13-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="65f13-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="65f13-113">0x00010000L</span></span> | <span data-ttu-id="65f13-114">Usare la normale vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input per la trasformazione della trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="65f13-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="65f13-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="65f13-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="65f13-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="65f13-116">0x00020000L</span></span> | <span data-ttu-id="65f13-117">Usare la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input per la trasformazione della trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="65f13-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="65f13-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="65f13-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="65f13-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="65f13-119">0x00030000L</span></span> | <span data-ttu-id="65f13-120">Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinata della trama di input per la trasformazione della trama di questa fase.</span><span class="sxs-lookup"><span data-stu-id="65f13-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="65f13-121">Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale.</span><span class="sxs-lookup"><span data-stu-id="65f13-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="65f13-122">D3DTSS \_ TCI \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="65f13-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="65f13-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="65f13-123">0x00040000L</span></span> | <span data-ttu-id="65f13-124">Usare le coordinate di trama specificate per il mapping della sfera.</span><span class="sxs-lookup"><span data-stu-id="65f13-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="65f13-125">Queste costanti vengono usate da D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="65f13-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="65f13-126">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="65f13-126">Constant Information</span></span>



|  <span data-ttu-id="65f13-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f13-127">Requirement</span></span>                        | <span data-ttu-id="65f13-128">Valore</span><span class="sxs-lookup"><span data-stu-id="65f13-128">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="65f13-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65f13-129">Header</span></span>                   | <span data-ttu-id="65f13-130">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="65f13-130">d3d9caps.h</span></span> |
| <span data-ttu-id="65f13-131">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="65f13-131">Minimum operating system</span></span> | <span data-ttu-id="65f13-132">Windows 98</span><span class="sxs-lookup"><span data-stu-id="65f13-132">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="65f13-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65f13-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65f13-134">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="65f13-134">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



