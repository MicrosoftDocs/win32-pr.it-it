---
description: Il colore viene definito come una combinazione di tre colori primari rossi, verdi e blu.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valori dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130810"
---
# <a name="color-values"></a><span data-ttu-id="895fe-103">Valori dei colori</span><span class="sxs-lookup"><span data-stu-id="895fe-103">Color Values</span></span>

<span data-ttu-id="895fe-104">Il colore viene definito come una combinazione di tre colori primari rossi, verdi e blu.</span><span class="sxs-lookup"><span data-stu-id="895fe-104">Color is defined as a combination of three primary colors red, green, and blue.</span></span> <span data-ttu-id="895fe-105">il sistema identifica un colore assegnando un valore di colore (talvolta denominato tripletta RGB), che è costituito da valori a 3 8 bit che specificano le intensità dei relativi componenti colore.</span><span class="sxs-lookup"><span data-stu-id="895fe-105">the system identifies a color by giving it a color value (sometimes called an RGB triplet), which consists of three 8-bit values specifying the intensities of its color components.</span></span> <span data-ttu-id="895fe-106">Il nero ha l'intensità minima per rosso, verde e blu, quindi il valore del colore per il nero è (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="895fe-106">Black has the minimum intensity for red, green, and blue, so the color value for black is (0, 0, 0).</span></span> <span data-ttu-id="895fe-107">Il bianco ha l'intensità massima per rosso, verde e blu, quindi il valore del colore è (255, 255, 255).</span><span class="sxs-lookup"><span data-stu-id="895fe-107">White has the maximum intensity for red, green, and blue, so its color value is (255, 255, 255).</span></span>

> [!Note]  
> <span data-ttu-id="895fe-108">Se è abilitata la corrispondenza dei colori dell'immagine, la definizione di colore e il significato di un valore di colore dipendono dal tipo di spazio dei colori attualmente impostato per il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="895fe-108">If image color matching is enabled, the definition of color and the meaning of a color value depends on the type of color space that is currently set for the device context.</span></span>

 

<span data-ttu-id="895fe-109">Il sistema e le applicazioni usano parametri e variabili con il tipo [COLORREF](colorref.md) per passare e archiviare i valori dei colori.</span><span class="sxs-lookup"><span data-stu-id="895fe-109">The system and applications use parameters and variables having the [COLORREF](colorref.md) type to pass and store color values.</span></span> <span data-ttu-id="895fe-110">Ad esempio, la funzione [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifica il colore di ogni penna impostando il membro **lopnColor** in una struttura [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) su un valore di colore.</span><span class="sxs-lookup"><span data-stu-id="895fe-110">For example, the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function identifies the color of each pen by setting the **lopnColor** member in a [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) structure to a color value.</span></span> <span data-ttu-id="895fe-111">Le applicazioni possono estrarre i singoli valori dei componenti rosso, verde e blu da un valore di colore utilizzando rispettivamente le macro [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) .</span><span class="sxs-lookup"><span data-stu-id="895fe-111">Applications can extract the individual values of the red, green, and blue components from a color value by using the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span> <span data-ttu-id="895fe-112">Le applicazioni possono creare un valore di colore dai singoli valori dei componenti usando la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="895fe-112">Applications can create a color value from individual component values by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="895fe-113">Quando si crea o si esamina una tavolozza logica, un'applicazione usa la struttura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) per definire i valori dei colori ed esaminare i valori dei singoli componenti.</span><span class="sxs-lookup"><span data-stu-id="895fe-113">When creating or examining a logical palette, an application uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure to define color values and to examine individual component values.</span></span>

 

 



