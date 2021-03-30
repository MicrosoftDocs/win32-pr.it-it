---
description: Un'applicazione inverte i colori visualizzati all'interno di un'area chiamando la funzione InvertRgn.
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: Invertire le aree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e3c4b4d01f9ed8f09e819d59bf3268a1ccae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993952"
---
# <a name="inverting-regions"></a><span data-ttu-id="f4122-103">Invertire le aree</span><span class="sxs-lookup"><span data-stu-id="f4122-103">Inverting Regions</span></span>

<span data-ttu-id="f4122-104">Un'applicazione inverte i colori visualizzati all'interno di un'area chiamando la funzione [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) .</span><span class="sxs-lookup"><span data-stu-id="f4122-104">An application inverts the colors that appear within a region by calling the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function.</span></span> <span data-ttu-id="f4122-105">Nelle visualizzazioni monocromatiche **InvertRgn** rende bianchi i pixel neri e neri.</span><span class="sxs-lookup"><span data-stu-id="f4122-105">On monochrome displays, **InvertRgn** makes white pixels black and black pixels white.</span></span> <span data-ttu-id="f4122-106">Nelle schermate dei colori questa inversione dipende dal tipo di tecnologia utilizzato per generare i colori per la schermata.</span><span class="sxs-lookup"><span data-stu-id="f4122-106">On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.</span></span>

 

 



