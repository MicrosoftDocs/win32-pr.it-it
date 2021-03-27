---
description: Un'applicazione può recuperare le metriche dei tipi di carattere per un tipo di carattere fisico solo dopo che il tipo di carattere è stato selezionato in un contesto di dispositivo.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Dispositivo e unità di progettazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880305"
---
# <a name="device-vs-design-units"></a><span data-ttu-id="19fac-103">Dispositivo e unità di progettazione</span><span class="sxs-lookup"><span data-stu-id="19fac-103">Device vs. Design Units</span></span>

<span data-ttu-id="19fac-104">Un'applicazione può recuperare le metriche dei tipi di carattere per un tipo di carattere fisico solo dopo che il tipo di carattere è stato selezionato in un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19fac-104">An application can retrieve font metrics for a physical font only after the font has been selected into a device context.</span></span> <span data-ttu-id="19fac-105">Quando si seleziona un tipo di carattere in un contesto di dispositivo, questo viene ridimensionato per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19fac-105">When a font is selected into a device context, it is scaled for the device.</span></span> <span data-ttu-id="19fac-106">Le metriche dei tipi di carattere specifiche del dispositivo sono note come unità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19fac-106">The font metrics specific to the device are known as device units.</span></span>

<span data-ttu-id="19fac-107">Le metriche portabili nei tipi di carattere sono note come unità di progettazione.</span><span class="sxs-lookup"><span data-stu-id="19fac-107">Portable metrics in fonts are known as design units.</span></span> <span data-ttu-id="19fac-108">Per applicare a un dispositivo specifico, le unità di progettazione devono essere convertite in unità di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19fac-108">To apply to a specified device, design units must be converted to device units.</span></span> <span data-ttu-id="19fac-109">Usare la formula seguente per convertire le unità di progettazione in unità di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19fac-109">Use the following formula to convert design units to device units.</span></span>

<span data-ttu-id="19fac-110">*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*pointsize*/72) \* *DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="19fac-110">*DeviceUnits* = (*DesignUnits*/*unitsPerEm*) \* (*PointSize*/72) \* *DeviceResolution*</span></span>

<span data-ttu-id="19fac-111">Le variabili in questa formula hanno i significati seguenti.</span><span class="sxs-lookup"><span data-stu-id="19fac-111">The variables in this formula have the following meanings.</span></span>



| <span data-ttu-id="19fac-112">Variabile</span><span class="sxs-lookup"><span data-stu-id="19fac-112">Variable</span></span>           | <span data-ttu-id="19fac-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19fac-113">Description</span></span>                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19fac-114">*DeviceUnits*</span><span class="sxs-lookup"><span data-stu-id="19fac-114">*DeviceUnits*</span></span>      | <span data-ttu-id="19fac-115">Specifica la metrica del tipo di carattere *DesignUnits* convertita in unità dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19fac-115">Specifies the *DesignUnits* font metric converted to device units.</span></span> <span data-ttu-id="19fac-116">Questo valore si trova nelle stesse unità del valore specificato per *DeviceResolution*.</span><span class="sxs-lookup"><span data-stu-id="19fac-116">This value is in the same units as the value specified for *DeviceResolution*.</span></span>                          |
| <span data-ttu-id="19fac-117">*DesignUnits*</span><span class="sxs-lookup"><span data-stu-id="19fac-117">*DesignUnits*</span></span>      | <span data-ttu-id="19fac-118">Specifica la metrica del tipo di carattere da convertire in unità di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19fac-118">Specifies the font metric to be converted to device units.</span></span> <span data-ttu-id="19fac-119">Questo valore può essere qualsiasi metrica del tipo di carattere, inclusa la larghezza di un carattere o il valore crescente per un intero tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="19fac-119">This value can be any font metric, including the width of a character or the ascender value for an entire font.</span></span> |
| <span data-ttu-id="19fac-120">*unitsPerEm*</span><span class="sxs-lookup"><span data-stu-id="19fac-120">*unitsPerEm*</span></span>       | <span data-ttu-id="19fac-121">Specifica la dimensione del quadrato em per il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="19fac-121">Specifies the em square size for the font.</span></span>                                                                                                                                 |
| <span data-ttu-id="19fac-122">*PointSize*</span><span class="sxs-lookup"><span data-stu-id="19fac-122">*PointSize*</span></span>        | <span data-ttu-id="19fac-123">Specifica la dimensione del tipo di carattere, in punti.</span><span class="sxs-lookup"><span data-stu-id="19fac-123">Specifies size of the font, in points.</span></span> <span data-ttu-id="19fac-124">(Un punto è uguale a 1/72 di pollice).</span><span class="sxs-lookup"><span data-stu-id="19fac-124">(One point equals 1/72 of an inch.)</span></span>                                                                                                 |
| <span data-ttu-id="19fac-125">*DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="19fac-125">*DeviceResolution*</span></span> | <span data-ttu-id="19fac-126">Specifica il numero di unità di dispositivo (pixel) per pollice.</span><span class="sxs-lookup"><span data-stu-id="19fac-126">Specifies number of device units (pixels) per inch.</span></span> <span data-ttu-id="19fac-127">I valori tipici possono essere 300 per una stampante laser o 96 per una schermata VGA.</span><span class="sxs-lookup"><span data-stu-id="19fac-127">Typical values might be 300 for a laser printer or 96 for a VGA screen.</span></span>                                                |



 

<span data-ttu-id="19fac-128">Questa formula non può essere usata per convertire le unità del dispositivo in unità di progettazione.</span><span class="sxs-lookup"><span data-stu-id="19fac-128">This formula should not be used to convert device units back to design units.</span></span> <span data-ttu-id="19fac-129">Le unità del dispositivo sono sempre arrotondate al pixel più vicino.</span><span class="sxs-lookup"><span data-stu-id="19fac-129">Device units are always rounded to the nearest pixel.</span></span> <span data-ttu-id="19fac-130">L'errore di arrotondamento propagato può diventare molto elevato, soprattutto quando un'applicazione utilizza dimensioni dello schermo.</span><span class="sxs-lookup"><span data-stu-id="19fac-130">The propagated round-off error can become very large, especially when an application is working with screen sizes.</span></span>

<span data-ttu-id="19fac-131">Per richiedere unità di progettazione, creare un tipo di carattere logico la cui altezza è specificata come *unitsPerEm*.</span><span class="sxs-lookup"><span data-stu-id="19fac-131">To request design units, create a logical font whose height is specified as *unitsPerEm*.</span></span> <span data-ttu-id="19fac-132">Le applicazioni possono recuperare il valore per *unitsPerEm* chiamando la funzione [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) e controllando il membro **ntmSizeEM** della struttura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="19fac-132">Applications can retrieve the value for *unitsPerEm* by calling the [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function and checking the **ntmSizeEM** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span>

 

 



