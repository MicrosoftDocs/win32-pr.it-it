---
description: Il dispositivo scanner Windows Image Acquisition (WIA) viene implementato come albero gerarchico di oggetti IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivi scanner WIA in WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751759"
---
# <a name="wia-scanner-devices-in-wia-10"></a><span data-ttu-id="ca827-103">Dispositivi scanner WIA in WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="ca827-103">WIA Scanner Devices in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="ca827-104">Questo argomento illustra l'albero del dispositivo dello scanner per le applicazioni che usano il servizio Windows Image Acquisition (WIA) 1,0, supportato in Windows XP o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="ca827-104">This topic discusses the scanner device tree for applications that use the Windows Image Acquisition (WIA) 1.0 service (which is supported on Windows XP or earlier).</span></span> <span data-ttu-id="ca827-105">Per informazioni sull'albero dei dispositivi degli elementi di acquisizione immagini Windows (WIA) 2,0, supportati in Windows Vista o versioni successive, vedere [informazioni sull'albero degli elementi di IWiaItem2](-wia-about-item-tree.md).</span><span class="sxs-lookup"><span data-stu-id="ca827-105">For information on the device tree of Windows Image Acquisition (WIA) 2.0 items (which are supported on Windows Vista or later), see [About the IWiaItem2 Item Tree](-wia-about-item-tree.md).</span></span>

 

<span data-ttu-id="ca827-106">Il dispositivo scanner Windows Image Acquisition (WIA) viene implementato come albero gerarchico di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="ca827-106">The Windows Image Acquisition (WIA) scanner device is implemented as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="ca827-107">Dall'elemento radice è possibile che un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="ca827-107">From the root item an application may:</span></span>

-   <span data-ttu-id="ca827-108">Funzionalità di query scanner</span><span class="sxs-lookup"><span data-stu-id="ca827-108">Query scanner capabilities</span></span>
-   <span data-ttu-id="ca827-109">Impostare le proprietà del dispositivo scanner</span><span class="sxs-lookup"><span data-stu-id="ca827-109">Set scanner device properties</span></span>
-   <span data-ttu-id="ca827-110">Controllare il feeder di documenti</span><span class="sxs-lookup"><span data-stu-id="ca827-110">Control the document feeder</span></span>

<span data-ttu-id="ca827-111">Un dispositivo scanner WIA è diverso da un dispositivo della fotocamera WIA perché, in generale, non archivia più immagini in memoria.</span><span class="sxs-lookup"><span data-stu-id="ca827-111">A WIA scanner device is different from a WIA camera device because, in general, it does not store multiple images in memory.</span></span>

<span data-ttu-id="ca827-112">Sotto l'elemento radice, un oggetto scanner tipico ha un singolo oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) che rappresenta la funzionalità di raccolta dati del dispositivo, l'elemento di analisi.</span><span class="sxs-lookup"><span data-stu-id="ca827-112">Underneath the root item, a typical scanner object has a single [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object that represents the data collecting functionality of the device, the Scan Item.</span></span> <span data-ttu-id="ca827-113">Questo elemento ha il flag [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) impostato per indicare che i trasferimenti di dati in questo elemento sono possibili.</span><span class="sxs-lookup"><span data-stu-id="ca827-113">This item has the [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) flag set to indicate that data transfers on this item are possible.</span></span> <span data-ttu-id="ca827-114">Un'applicazione imposta un'analisi impostando le proprietà dell'elemento Scan, quindi esegue l'analisi e trasferisce i dati utilizzando un'interfaccia di trasferimento dati.</span><span class="sxs-lookup"><span data-stu-id="ca827-114">An application sets up a scan by setting the properties of the scan item, then performs the scan and transfers the data using a data transfer interface.</span></span>

<span data-ttu-id="ca827-115">Il diagramma seguente illustra l'implementazione di WIA per uno scanner tipico:</span><span class="sxs-lookup"><span data-stu-id="ca827-115">The following diagram illustrates the WIA implementation for a typical scanner:</span></span>

![implementazione WIA di uno scanner tipico](images/wiscantr.gif)

<span data-ttu-id="ca827-117">Un tipico scanner duplex viene rappresentato in WIA con un oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="ca827-117">A typical duplex scanner is represented in WIA by having one [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span> <span data-ttu-id="ca827-118">Viene eseguito l'accesso ai dati della pagina iniziale e in sequenza a un trasferimento dati per pagina.</span><span class="sxs-lookup"><span data-stu-id="ca827-118">Front- and back-page data is accessed sequentially one data transfer per page.</span></span> <span data-ttu-id="ca827-119">La rappresentazione di uno scanner duplex è pertanto identica alla rappresentazione di uno scanner tipico.</span><span class="sxs-lookup"><span data-stu-id="ca827-119">Therefore, the representation of a duplex scanner is identical to the representation of a typical scanner.</span></span>

<span data-ttu-id="ca827-120">Uno scanner scorrevole in grado di analizzare più diapositive in un'unica operazione di analisi rappresenta ciascuna immagine separata come oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) separato.</span><span class="sxs-lookup"><span data-stu-id="ca827-120">A slide scanner capable of scanning multiple slides in a single scan operation represents each separate image as a separate [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span>

<span data-ttu-id="ca827-121">Il diagramma seguente illustra la rappresentazione WIA di uno scanner diapositiva:</span><span class="sxs-lookup"><span data-stu-id="ca827-121">The following diagram illustrates the WIA representation of a slide scanner:</span></span>

![scanner diapositiva](images/wislscan.gif)

 

 



