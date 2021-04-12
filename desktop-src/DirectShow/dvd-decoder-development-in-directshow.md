---
description: Sviluppo di DVD decoder in DirectShow
ms.assetid: c00ff132-fee1-47b5-8a8a-df7cb920ad89
title: Sviluppo di DVD decoder in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3de64b3c1d91dbf5f22ba3e4b4ae8fe78edda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482429"
---
# <a name="dvd-decoder-development-in-directshow"></a><span data-ttu-id="d2f3a-103">Sviluppo di DVD decoder in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d2f3a-103">DVD Decoder Development in DirectShow</span></span>

<span data-ttu-id="d2f3a-104">Questa sezione contiene i puntatori alle pagine di riferimento per tutti i set di proprietà DirectShow e le interfacce che sono specifiche del DVD o usate in modo estensivo nella decodifica dei DVD.</span><span class="sxs-lookup"><span data-stu-id="d2f3a-104">This section contains pointers to the reference pages for all the DirectShow property sets and interfaces that are either DVD-specific or else used extensively in DVD decoding.</span></span> <span data-ttu-id="d2f3a-105">Oltre a quanto elencato, un decodificatore e i relativi pin devono supportare anche le interfacce generiche di filtro DirectShow, come descritto in [scrittura di filtri DirectShow](writing-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d2f3a-105">In addition to what is listed here, a decoder and its pins must also support the generic DirectShow filter interfaces as described in [Writing DirectShow Filters](writing-directshow-filters.md).</span></span>

<span data-ttu-id="d2f3a-106">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2f3a-106">This section contains the following topics.</span></span>

-   [<span data-ttu-id="d2f3a-107">Controllo del volume del decodificatore</span><span class="sxs-lookup"><span data-stu-id="d2f3a-107">Decoder Volume Control</span></span>](decoder-volume-control.md)
-   [<span data-ttu-id="d2f3a-108">Supporto delle modifiche all'area DVD in Windows</span><span class="sxs-lookup"><span data-stu-id="d2f3a-108">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)

<span data-ttu-id="d2f3a-109">Vedere anche la pagina relativa alla</span><span class="sxs-lookup"><span data-stu-id="d2f3a-109">See also:</span></span>

-   [<span data-ttu-id="d2f3a-110">**Set di proprietà di DVD karaoke**</span><span class="sxs-lookup"><span data-stu-id="d2f3a-110">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="d2f3a-111">**Set di proprietà di protezione copia DVD**</span><span class="sxs-lookup"><span data-stu-id="d2f3a-111">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="d2f3a-112">**Set di proprietà della sottoimmagine DVD**</span><span class="sxs-lookup"><span data-stu-id="d2f3a-112">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="d2f3a-113">Imposta la proprietà pin</span><span class="sxs-lookup"><span data-stu-id="d2f3a-113">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="d2f3a-114">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d2f3a-114">**IKsPropertySet**</span></span>](ikspropertyset.md)
-   <span data-ttu-id="d2f3a-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (solo decodificatori hardware)</span><span class="sxs-lookup"><span data-stu-id="d2f3a-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (hardware decoders only)</span></span>
-   <span data-ttu-id="d2f3a-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (solo decodificatori hardware)</span><span class="sxs-lookup"><span data-stu-id="d2f3a-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (hardware decoders only)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2f3a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2f3a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2f3a-118">Specifiche e interfacce del decodificatore</span><span class="sxs-lookup"><span data-stu-id="d2f3a-118">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



