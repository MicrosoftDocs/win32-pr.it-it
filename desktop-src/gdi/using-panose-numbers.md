---
description: I file dei tipi di carattere TrueType includono i numeri PANOse, che possono essere usati dalle applicazioni per scegliere un tipo di carattere che corrisponda strettamente alle specifiche.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Uso di numeri PANOse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233212"
---
# <a name="using-panose-numbers"></a><span data-ttu-id="d2d37-103">Uso di numeri PANOse</span><span class="sxs-lookup"><span data-stu-id="d2d37-103">Using PANOSE Numbers</span></span>

<span data-ttu-id="d2d37-104">I file dei tipi di carattere TrueType includono i numeri PANOse, che possono essere usati dalle applicazioni per scegliere un tipo di carattere che corrisponda strettamente alle specifiche.</span><span class="sxs-lookup"><span data-stu-id="d2d37-104">TrueType font files include PANOSE numbers, which applications can use to choose a font that closely matches their specifications.</span></span> <span data-ttu-id="d2d37-105">Il sistema PANOn classifica i visi di 10 attributi diversi.</span><span class="sxs-lookup"><span data-stu-id="d2d37-105">The PANOSE system classifies faces by 10 different attributes.</span></span> <span data-ttu-id="d2d37-106">Per ulteriori informazioni su questi attributi, vedere [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose).</span><span class="sxs-lookup"><span data-stu-id="d2d37-106">For more information about these attributes, see [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose).</span></span> <span data-ttu-id="d2d37-107">Una struttura **Panoa** fa parte della struttura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (i cui valori sono compilati chiamando la funzione [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).</span><span class="sxs-lookup"><span data-stu-id="d2d37-107">A **PANOSE** structure is part of the [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) structure (whose values are filled in by calling the [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) function).</span></span>

<span data-ttu-id="d2d37-108">Gli attributi PANOn vengono classificati singolarmente su una scala.</span><span class="sxs-lookup"><span data-stu-id="d2d37-108">The PANOSE attributes are rated individually on a scale.</span></span> <span data-ttu-id="d2d37-109">I valori risultanti vengono concatenati per produrre un numero.</span><span class="sxs-lookup"><span data-stu-id="d2d37-109">The resulting values are concatenated to produce a number.</span></span> <span data-ttu-id="d2d37-110">Dato questo numero per un tipo di carattere e una metrica matematica per misurare le distanze nello spazio PANOn, un'applicazione può determinare gli elementi adiacenti più vicini.</span><span class="sxs-lookup"><span data-stu-id="d2d37-110">Given this number for a font and a mathematical metric to measure distances in the PANOSE space, an application can determine the nearest neighbors.</span></span>

 

 



