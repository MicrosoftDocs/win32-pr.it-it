---
title: Informazioni su Bluetooth
description: Bluetooth è un protocollo standard del settore che consente la connettività wireless per molti dispositivi, tra cui computer, stampanti, telefoni cellulari e dispositivi palmari.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, descritto
- Bluetooth Bluetooth, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046355"
---
# <a name="about-bluetooth"></a><span data-ttu-id="1c61f-105">Informazioni su Bluetooth</span><span class="sxs-lookup"><span data-stu-id="1c61f-105">About Bluetooth</span></span>

<span data-ttu-id="1c61f-106">Bluetooth è un protocollo standard del settore che consente la connettività wireless per molti dispositivi, tra cui computer, stampanti, telefoni cellulari e dispositivi palmari.</span><span class="sxs-lookup"><span data-stu-id="1c61f-106">Bluetooth is an industry-standard protocol that enables wireless connectivity for a multitude of devices, including computers, printers, mobile phones, and handheld devices.</span></span>

<span data-ttu-id="1c61f-107">Le principali funzionalità Bluetooth includono:</span><span class="sxs-lookup"><span data-stu-id="1c61f-107">Key Bluetooth features include:</span></span>

-   <span data-ttu-id="1c61f-108">Un protocollo wireless a basso costo e a basso consumo di energia con supporto standard del settore e accettazione in tutto il mondo.</span><span class="sxs-lookup"><span data-stu-id="1c61f-108">A low-cost, low-power consumption wireless protocol with industry-standard support and worldwide acceptance.</span></span>
-   <span data-ttu-id="1c61f-109">Interfaccia di programmazione definita e familiare che gli sviluppatori possono utilizzare per sviluppare o trasferire rapidamente le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1c61f-109">A defined and familiar programming interface that developers can use to quickly develop or port applications.</span></span>
-   <span data-ttu-id="1c61f-110">Un sito web ufficiale e un'organizzazione cooperativa a livello di settore che spiega, promuove e standardizza la tecnologia Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="1c61f-110">An official Web site and an industry-wide cooperative organization that explains, promotes, and standardizes Bluetooth technology.</span></span> <span data-ttu-id="1c61f-111">Per ulteriori informazioni, vedere [www.Bluetooth.com](https://www.bluetooth.com/).</span><span class="sxs-lookup"><span data-stu-id="1c61f-111">For more information, see [www.bluetooth.com](https://www.bluetooth.com/).</span></span>

<span data-ttu-id="1c61f-112">Bluetooth in Windows fornisce servizi di base simili a quelli esposti da Transmission Control Protocol (la parte TCP di TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="1c61f-112">Bluetooth on Windows provides core services that are similar to those exposed by Transmission Control Protocol (the TCP part of TCP/IP).</span></span> <span data-ttu-id="1c61f-113">Analogamente a molti protocolli e servizi di rete, la connettività Bluetooth e il trasferimento dei dati vengono programmati tramite le chiamate di funzione Windows Sockets, utilizzando le tecniche comuni di programmazione di Windows Socket e specifiche estensioni Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="1c61f-113">Like many networking protocols and services, Bluetooth connectivity and data transfer are programmed through Windows Sockets function calls, using common Windows Sockets programming techniques and specific Bluetooth extensions.</span></span> <span data-ttu-id="1c61f-114">Tuttavia, poiché esistono differenze significative tra una rete cablata e fissa e una rete ad hoc senza fili, Bluetooth fornisce estensioni quali l'individuazione di servizi/dispositivi e la notifica che consentono alle applicazioni di funzionare correttamente nell'ambiente wireless.</span><span class="sxs-lookup"><span data-stu-id="1c61f-114">However, because significant differences exist between a wired, fixed network and a wireless ad-hoc network, Bluetooth provides extensions such as service/device discovery and notification that enable applications to operate properly in the wireless environment.</span></span> <span data-ttu-id="1c61f-115">Queste estensioni aprono anche la modalità di trasferimento semplice a tecnologie simili, ad esempio IrDA, o trasporti wireless futuri.</span><span class="sxs-lookup"><span data-stu-id="1c61f-115">These extensions also pave the way for simple porting to similar technologies, such as IrDA, or future wireless transports.</span></span>

<span data-ttu-id="1c61f-116">Microsoft fornisce supporto per Bluetooth in Windows XP con Service Pack 1 (SP1) e versioni successive, in Windows XP Embedded con Service Pack 2 e in Windows CE.</span><span class="sxs-lookup"><span data-stu-id="1c61f-116">Microsoft provides support for Bluetooth on Windows XP with Service Pack 1 (SP1) and later, on Windows XP Embedded with Service Pack 2, and on Windows CE.</span></span> <span data-ttu-id="1c61f-117">Le applicazioni Bluetooth eseguite in Windows XP devono essere in grado di essere eseguite in un'immagine di run-time basata su Windows XP Embedded che include le dipendenze richieste.</span><span class="sxs-lookup"><span data-stu-id="1c61f-117">Bluetooth applications that run on Windows XP should be able to run on a Windows XP Embedded-based run-time image that includes the required dependencies.</span></span> <span data-ttu-id="1c61f-118">Per ulteriori informazioni su Windows XP Embedded, vedere la documentazione della Guida di Windows XP Embedded su MSDN.</span><span class="sxs-lookup"><span data-stu-id="1c61f-118">For more information about Windows XP Embedded, see the Windows XP Embedded Help documentation on MSDN.</span></span> <span data-ttu-id="1c61f-119">Per ulteriori informazioni sulla programmazione Windows CE, consultare l'SDK di Windows CE.</span><span class="sxs-lookup"><span data-stu-id="1c61f-119">For more information about Windows CE programming, consult the Windows CE SDK.</span></span>

<span data-ttu-id="1c61f-120">Microsoft offre due approcci per la programmazione di Bluetooth in Windows:</span><span class="sxs-lookup"><span data-stu-id="1c61f-120">Microsoft provides two approaches for programming Bluetooth on Windows:</span></span>

-   <span data-ttu-id="1c61f-121">Utilizzo dell'interfaccia Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="1c61f-121">Using the Windows Sockets interface</span></span>
-   <span data-ttu-id="1c61f-122">Gestione diretta dei dispositivi mediante interfacce Bluetooth non socket</span><span class="sxs-lookup"><span data-stu-id="1c61f-122">Managing devices directly by using nonsocket Bluetooth interfaces</span></span>

<span data-ttu-id="1c61f-123">In questa sezione vengono fornite informazioni generali su entrambi questi approcci negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="1c61f-123">This section provides overview information about both of these approaches in the following topics.</span></span> <span data-ttu-id="1c61f-124">Per ulteriori informazioni sull'utilizzo di elementi API Windows Sockets per programmare il Bluetooth, vedere la pagina relativa alla [programmazione Bluetooth con Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="1c61f-124">For more information about using Windows Sockets API elements to program Bluetooth, see [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span></span>



| <span data-ttu-id="1c61f-125">Sezione</span><span class="sxs-lookup"><span data-stu-id="1c61f-125">Section</span></span>                                                                                | <span data-ttu-id="1c61f-126">Content</span><span class="sxs-lookup"><span data-stu-id="1c61f-126">Content</span></span>                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="1c61f-127">Supporto di Windows Sockets per Bluetooth</span><span class="sxs-lookup"><span data-stu-id="1c61f-127">Windows Sockets Support for Bluetooth</span></span>](windows-sockets-support-for-bluetooth.md)     | <span data-ttu-id="1c61f-128">Descrive la relazione tra Bluetooth e Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="1c61f-128">Describes the relationship between Bluetooth and Windows Sockets.</span></span> |
| [<span data-ttu-id="1c61f-129">Gestione dei dispositivi e dei servizi Bluetooth</span><span class="sxs-lookup"><span data-stu-id="1c61f-129">Managing Bluetooth Devices and Services</span></span>](managing-bluetooth-devices-and-services.md) | <span data-ttu-id="1c61f-130">Viene descritto come gestire i dispositivi e i servizi Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="1c61f-130">Describes how to manage Bluetooth devices and services.</span></span>           |



 

 

 




