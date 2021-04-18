---
description: L'interfaccia Windows Image Acquisition (WIA) è un'API e un'interfaccia DDI (Device Driver Interface).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Informazioni sull'acquisizione di immagini Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312460"
---
# <a name="about-windows-image-acquisition"></a><span data-ttu-id="e64f3-103">Informazioni sull'acquisizione di immagini Windows</span><span class="sxs-lookup"><span data-stu-id="e64f3-103">About Windows Image Acquisition</span></span>

<span data-ttu-id="e64f3-104">L'interfaccia Windows Image Acquisition (WIA) è un'API e un'interfaccia DDI (Device Driver Interface).</span><span class="sxs-lookup"><span data-stu-id="e64f3-104">The Windows Image Acquisition (WIA) interface is both an API and a device driver interface (DDI).</span></span> <span data-ttu-id="e64f3-105">L'API WIA è progettata per consentire alle applicazioni di:</span><span class="sxs-lookup"><span data-stu-id="e64f3-105">The WIA API is designed to allow applications to:</span></span>

-   <span data-ttu-id="e64f3-106">Eseguire in un ambiente solido e stabile.</span><span class="sxs-lookup"><span data-stu-id="e64f3-106">Run in a robust and stable environment.</span></span>
-   <span data-ttu-id="e64f3-107">Ridurre al minimo i problemi di interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="e64f3-107">Minimize interoperability problems.</span></span>
-   <span data-ttu-id="e64f3-108">Enumera i dispositivi di acquisizione immagini disponibili.</span><span class="sxs-lookup"><span data-stu-id="e64f3-108">Enumerate available image acquisition devices.</span></span>
-   <span data-ttu-id="e64f3-109">Consente di creare connessioni a più dispositivi contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="e64f3-109">Create connections to multiple devices simultaneously.</span></span>
-   <span data-ttu-id="e64f3-110">Eseguire query sulle proprietà dei dispositivi in modo standard ed espandibile.</span><span class="sxs-lookup"><span data-stu-id="e64f3-110">Query properties of devices in a standard and expandable manner.</span></span>
-   <span data-ttu-id="e64f3-111">Acquisisci i dati del dispositivo usando meccanismi di trasferimento standard e ad alte prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e64f3-111">Acquire device data using standard and high performance transfer mechanisms.</span></span>
-   <span data-ttu-id="e64f3-112">Gestire le proprietà delle immagini nei trasferimenti di dati.</span><span class="sxs-lookup"><span data-stu-id="e64f3-112">Maintain image properties across data transfers.</span></span>
-   <span data-ttu-id="e64f3-113">Ricevere una notifica relativa a un'ampia gamma di eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e64f3-113">Be notified of a wide variety of device events.</span></span>

<span data-ttu-id="e64f3-114">Il WIADDI è progettato per ridurre al minimo la quantità di codice che un fornitore di hardware deve scrivere, mantenendo al tempo stesso la flessibilità necessaria per creare singole soluzioni.</span><span class="sxs-lookup"><span data-stu-id="e64f3-114">The WIADDI is designed to minimize the amount of code a hardware vendor must write, while maintaining the flexibility to craft individual solutions.</span></span> <span data-ttu-id="e64f3-115">Questa operazione viene eseguita da:</span><span class="sxs-lookup"><span data-stu-id="e64f3-115">This is accomplished by:</span></span>

-   <span data-ttu-id="e64f3-116">Fornire una libreria di servizi per dispositivi standard che esegue la maggior parte delle operazioni del driver.</span><span class="sxs-lookup"><span data-stu-id="e64f3-116">Providing a standard device service library that performs most driver operations.</span></span>
-   <span data-ttu-id="e64f3-117">Promozione degli standard di comunicazione dei dispositivi del settore in modo che un driver WIA supporti la maggior parte dei dispositivi WIA.</span><span class="sxs-lookup"><span data-stu-id="e64f3-117">Promoting industry device communications standards so that one WIA driver supports most WIA devices.</span></span> <span data-ttu-id="e64f3-118">Ad esempio, il protocollo PTP (Picture Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="e64f3-118">For example, Picture Transfer Protocol (PTP).</span></span>
-   <span data-ttu-id="e64f3-119">Consentire al driver di dispositivo di supportare interfacce personalizzate, senza richiedere l'uso della libreria del servizio del dispositivo standard.</span><span class="sxs-lookup"><span data-stu-id="e64f3-119">Allowing the device driver to support custom interfaces, while not requiring that it use the standard device service library.</span></span> <span data-ttu-id="e64f3-120">Tuttavia, i driver devono comunque implementare le interfacce standard WIA.</span><span class="sxs-lookup"><span data-stu-id="e64f3-120">However, drivers still need to implement the standard WIA interfaces.</span></span>

<span data-ttu-id="e64f3-121">In questa sezione viene presentata una breve panoramica dell'interfaccia WIA nelle seguenti aree:</span><span class="sxs-lookup"><span data-stu-id="e64f3-121">This section presents a brief overview of the WIA interface in the following areas:</span></span>

-   [<span data-ttu-id="e64f3-122">Architettura WIA</span><span class="sxs-lookup"><span data-stu-id="e64f3-122">WIA Architecture</span></span>](-wia-wia-architecture.md)
-   [<span data-ttu-id="e64f3-123">Compatibilità STI</span><span class="sxs-lookup"><span data-stu-id="e64f3-123">STI Compatibility</span></span>](-wia-sti-compatibility.md)
-   [<span data-ttu-id="e64f3-124">Compatibilità con TWAIN</span><span class="sxs-lookup"><span data-stu-id="e64f3-124">TWAIN Compatibility</span></span>](-wia-twain-compatibility.md)
-   [<span data-ttu-id="e64f3-125">Gestione dispositivi WIA</span><span class="sxs-lookup"><span data-stu-id="e64f3-125">WIA Device Manager</span></span>](-wia-wia-device-manager.md)
-   [<span data-ttu-id="e64f3-126">Libreria di servizi WIA minidriver</span><span class="sxs-lookup"><span data-stu-id="e64f3-126">WIA Minidriver Service Library</span></span>](-wia-wia-minidriver-service-library.md)
-   [<span data-ttu-id="e64f3-127">Minidriver WIA</span><span class="sxs-lookup"><span data-stu-id="e64f3-127">WIA Minidriver</span></span>](-wia-wia-minidriver.md)

 

 



