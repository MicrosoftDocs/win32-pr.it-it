---
title: Coppie di identificatori di proprietà/offset
description: In seguito al conteggio delle proprietà, il valore del set di proprietà è una matrice di coppie di identificatori di proprietà/coppie di offset.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298973"
---
# <a name="property-identifiersoffset-pairs"></a><span data-ttu-id="57cb9-103">Coppie di identificatori di proprietà/offset</span><span class="sxs-lookup"><span data-stu-id="57cb9-103">Property Identifiers/Offset Pairs</span></span>

<span data-ttu-id="57cb9-104">In seguito al conteggio delle proprietà, il valore del set di proprietà è una matrice di coppie di identificatori di proprietà/coppie di offset.</span><span class="sxs-lookup"><span data-stu-id="57cb9-104">Following the Count of Properties property set value is an array of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="57cb9-105">Gli identificatori di proprietà sono valori a 32 bit che identificano in modo univoco una proprietà all'interno di una sezione.</span><span class="sxs-lookup"><span data-stu-id="57cb9-105">Property Identifiers are 32-bit values that uniquely identify a property within a section.</span></span> <span data-ttu-id="57cb9-106">Le coppie di offset indicano la distanza tra l'inizio della sezione e l'inizio della coppia tipo/valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="57cb9-106">The Offset Pairs indicate the distance from the start of the section to the start of the property Type/Value Pair.</span></span> <span data-ttu-id="57cb9-107">Poiché gli offset sono relativi alla sezione, le sezioni possono essere copiate come una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="57cb9-107">Because the offsets are relative to the section, sections can be copied as an array of bytes.</span></span>

<span data-ttu-id="57cb9-108">Gli identificatori di proprietà non sono ordinati in base a un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="57cb9-108">Property identifiers are not sorted in any particular order.</span></span> <span data-ttu-id="57cb9-109">Le proprietà possono essere omesse dal set di proprietà archiviato; i lettori non devono basarsi su un ordine o un intervallo specifico di identificatori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="57cb9-109">Properties can be omitted from the stored property set; readers must not rely on a specific order or range of property identifiers.</span></span>

 

 




