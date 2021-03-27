---
description: Un'applicazione può convertire un percorso in un'area chiamando la funzione PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversione dei percorsi in aree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754474"
---
# <a name="conversion-of-paths-to-regions"></a><span data-ttu-id="be652-103">Conversione dei percorsi in aree</span><span class="sxs-lookup"><span data-stu-id="be652-103">Conversion of Paths to Regions</span></span>

<span data-ttu-id="be652-104">Un'applicazione può convertire un percorso in un'area chiamando la funzione [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) .</span><span class="sxs-lookup"><span data-stu-id="be652-104">An application can convert a path into a region by calling the [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) function.</span></span> <span data-ttu-id="be652-105">Analogamente a [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** è utile per la creazione di speciali effetti grafici.</span><span class="sxs-lookup"><span data-stu-id="be652-105">Like [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** is useful in the creation of special graphics effects.</span></span> <span data-ttu-id="be652-106">Non sono ad esempio disponibili funzioni che consentono a un'applicazione di eseguire l'offset di un percorso. Tuttavia, esiste una funzione che consente a un'applicazione di eseguire l'offset di un'area ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span><span class="sxs-lookup"><span data-stu-id="be652-106">For example, there are no functions that allow an application to offset a path; however, there is a function that enables an application to offset a region ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span></span> <span data-ttu-id="be652-107">Usando **PathToRegion** , un'applicazione può creare l'effetto dell'animazione di una forma complessa creando un percorso che definisce la forma, convertendo il percorso in un'area (chiamando **PathToRegion**), quindi disegnando ripetutamente, spostando e cancellando l'area (chiamando le funzioni in una sequenza, ad esempio [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** e **FillRgn**).</span><span class="sxs-lookup"><span data-stu-id="be652-107">Using **PathToRegion** , an application can create the effect of animating a complex shape by creating a path that defines the shape, converting the path into a region (by calling **PathToRegion**), and then repeatedly painting, moving, and erasing the region (by calling functions in a sequence, such as [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** , and **FillRgn**).</span></span>

 

 



