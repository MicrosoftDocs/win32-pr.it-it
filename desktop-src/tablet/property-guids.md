---
description: I riconoscitori Microsoft usano i seguenti GUID.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUID proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132027"
---
# <a name="property-guids"></a><span data-ttu-id="da7c1-103">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="da7c1-103">Property GUIDs</span></span>

<span data-ttu-id="da7c1-104">I riconoscitori Microsoft usano i seguenti GUID.</span><span class="sxs-lookup"><span data-stu-id="da7c1-104">The Microsoft recognizers use the following GUIDs.</span></span> <span data-ttu-id="da7c1-105">Laddove possibile, le applicazioni devono usare questi GUID.</span><span class="sxs-lookup"><span data-stu-id="da7c1-105">Whenever possible, applications should use these GUIDs.</span></span> <span data-ttu-id="da7c1-106">Tuttavia, è previsto che gli altri riconoscitori usino GUID aggiuntivi per le proprietà non supportate dai sistemi di riconoscimento Microsoft.</span><span class="sxs-lookup"><span data-stu-id="da7c1-106">However, it is expected and encouraged that other recognizers will use additional GUIDs for properties that are not supported by the Microsoft recognizers.</span></span>

<span data-ttu-id="da7c1-107">Tutte le funzioni di proprietà sono state sviluppate con la consapevolezza che l'elenco dei GUID può essere esteso da altri riconoscitori.</span><span class="sxs-lookup"><span data-stu-id="da7c1-107">All property functions have been developed with the understanding that the list of GUIDs may be extended by other recognizers.</span></span> <span data-ttu-id="da7c1-108">Queste funzioni di proprietà includono:</span><span class="sxs-lookup"><span data-stu-id="da7c1-108">These property functions include:</span></span>

-   [<span data-ttu-id="da7c1-109">**GetContextPropertyList (funzione)**</span><span class="sxs-lookup"><span data-stu-id="da7c1-109">**GetContextPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [<span data-ttu-id="da7c1-110">**GetContextPropertyValue (funzione)**</span><span class="sxs-lookup"><span data-stu-id="da7c1-110">**GetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [<span data-ttu-id="da7c1-111">**GetResultPropertyList (funzione)**</span><span class="sxs-lookup"><span data-stu-id="da7c1-111">**GetResultPropertyList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [<span data-ttu-id="da7c1-112">**SetContextPropertyValue (funzione)**</span><span class="sxs-lookup"><span data-stu-id="da7c1-112">**SetContextPropertyValue Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

<span data-ttu-id="da7c1-113">La tabella seguente elenca i GUID delle proprietà di Tablet PC definiti in msinkaut. h (installati in c: \\ programmi \\ Microsoft Tablet PC Platform SDK \\ includono per impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="da7c1-113">The following table lists Tablet PC property GUIDs defined in msinkaut.h (installed in c:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include by default).</span></span>



| <span data-ttu-id="da7c1-114">GUID</span><span class="sxs-lookup"><span data-stu-id="da7c1-114">GUID</span></span>                                                  | <span data-ttu-id="da7c1-115">Definizione</span><span class="sxs-lookup"><span data-stu-id="da7c1-115">Definition</span></span>                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="da7c1-116">\_BOXNUMBER INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="da7c1-116">INKRECOGNITIONPROPERTY\_BOXNUMBER</span></span><br/>          | <span data-ttu-id="da7c1-117">Indice della casella alternativa del riconoscitore in modalità Box</span><span class="sxs-lookup"><span data-stu-id="da7c1-117">The recognizer alternate box index in box mode</span></span><br/>                                    |
| <span data-ttu-id="da7c1-118">INKRECOGNITIONPROPERTY \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="da7c1-118">INKRECOGNITIONPROPERTY\_LINENUMBER</span></span><br/>         | <span data-ttu-id="da7c1-119">Numero di riga</span><span class="sxs-lookup"><span data-stu-id="da7c1-119">The line number</span></span><br/>                                                                   |
| <span data-ttu-id="da7c1-120">\_segmentazione INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="da7c1-120">INKRECOGNITIONPROPERTY\_SEGMENTATION</span></span><br/>       | <span data-ttu-id="da7c1-121">Segmenti di parole e caratteri per il riconoscimento</span><span class="sxs-lookup"><span data-stu-id="da7c1-121">How the recognizer segments words and characters</span></span><br/>                                  |
| <span data-ttu-id="da7c1-122">\_Hotpoint INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="da7c1-122">INKRECOGNITIONPROPERTY\_HOTPOINT</span></span><br/>           | <span data-ttu-id="da7c1-123">Punto critico del movimento</span><span class="sxs-lookup"><span data-stu-id="da7c1-123">The gesture hot point</span></span><br/>                                                             |
| <span data-ttu-id="da7c1-124">\_MAXIMUMSTROKECOUNT INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="da7c1-124">INKRECOGNITIONPROPERTY\_MAXIMUMSTROKECOUNT</span></span><br/> | <span data-ttu-id="da7c1-125">Numero massimo di tratti per un segmento</span><span class="sxs-lookup"><span data-stu-id="da7c1-125">Maximum number of strokes for a segment</span></span><br/>                                           |
| <span data-ttu-id="da7c1-126">\_POINTSPERINCH INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="da7c1-126">INKRECOGNITIONPROPERTY\_POINTSPERINCH</span></span><br/>      | <span data-ttu-id="da7c1-127">Metrica dei punti per pollice</span><span class="sxs-lookup"><span data-stu-id="da7c1-127">The points-per-inch metric</span></span><br/>                                                        |
| <span data-ttu-id="da7c1-128">\_CONFIDENCELEVEL INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="da7c1-128">INKRECOGNITIONPROPERTY\_CONFIDENCELEVEL</span></span><br/>    | <span data-ttu-id="da7c1-129">[**Sicurezza \_ Enumerazione LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level)</span><span class="sxs-lookup"><span data-stu-id="da7c1-129">[**CONFIDENCE\_LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) enumeration</span></span><br/>                         |
| <span data-ttu-id="da7c1-130">\_LINEMETRICS INKRECOGNITIONPROPERTY</span><span class="sxs-lookup"><span data-stu-id="da7c1-130">INKRECOGNITIONPROPERTY\_LINEMETRICS</span></span><br/>        | <span data-ttu-id="da7c1-131">Informazioni per il calcolo della baseline, della linea media o di entrambe le informazioni utilizzate nel reticolo</span><span class="sxs-lookup"><span data-stu-id="da7c1-131">Information for computing baseline, midline, or both, that is used in the lattice</span></span><br/> |



 

 

 




