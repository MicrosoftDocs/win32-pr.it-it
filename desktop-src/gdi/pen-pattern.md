---
description: L'attributo pattern specifica il modello di una penna geometrica.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Modello di penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528297"
---
# <a name="pen-pattern"></a><span data-ttu-id="0aec0-103">Modello di penna</span><span class="sxs-lookup"><span data-stu-id="0aec0-103">Pen Pattern</span></span>

<span data-ttu-id="0aec0-104">L'attributo pattern specifica il modello di una penna geometrica.</span><span class="sxs-lookup"><span data-stu-id="0aec0-104">The pattern attribute specifies the pattern of a geometric pen.</span></span>

<span data-ttu-id="0aec0-105">Nella figura seguente sono illustrate le linee disegnate con diverse penne geometriche.</span><span class="sxs-lookup"><span data-stu-id="0aec0-105">The following illustration shows lines drawn with different geometric pens.</span></span> <span data-ttu-id="0aec0-106">Ogni penna è stata creata usando un attributo del criterio diverso.</span><span class="sxs-lookup"><span data-stu-id="0aec0-106">Each pen was created using a different pattern attribute.</span></span>

![illustrazione che mostra quattro righe, ognuna con una penna diversa](images/cspen-02.png)

<span data-ttu-id="0aec0-108">La prima riga della figura precedente viene disegnata utilizzando uno dei sei modelli di tratteggio disponibili. Per ulteriori informazioni sui modelli di tratteggio, vedere [Pen Hatch](pen-hatch.md).</span><span class="sxs-lookup"><span data-stu-id="0aec0-108">The first line in the previous illustration is drawn using one of the six available hatch patterns; for more information about hatch patterns, see [Pen Hatch](pen-hatch.md).</span></span> <span data-ttu-id="0aec0-109">La riga successiva viene disegnata usando il modello vuoto, identica al modello null.</span><span class="sxs-lookup"><span data-stu-id="0aec0-109">The next line is drawn using the hollow pattern, identical to the null pattern.</span></span> <span data-ttu-id="0aec0-110">La terza riga viene disegnata usando un modello personalizzato creato da una bitmap da 8 a 8 pixel.</span><span class="sxs-lookup"><span data-stu-id="0aec0-110">The third line is drawn using a custom pattern created from an 8-by-8-pixel bitmap.</span></span> <span data-ttu-id="0aec0-111">Per ulteriori informazioni sulle bitmap e sulla relativa creazione, vedere [bitmap](bitmaps.md). L'ultima riga viene disegnata usando un modello a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="0aec0-111">(For more information about bitmaps and their creation, see [Bitmaps](bitmaps.md).) The last line is drawn using a solid pattern.</span></span> <span data-ttu-id="0aec0-112">La creazione di un pennello e il passaggio del relativo handle alla funzione [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) creano un modello.</span><span class="sxs-lookup"><span data-stu-id="0aec0-112">Creating a brush and passing its handle to the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function creates a pattern.</span></span>

 

 



