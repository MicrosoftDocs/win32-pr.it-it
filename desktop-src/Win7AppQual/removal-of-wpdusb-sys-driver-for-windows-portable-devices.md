---
description: .
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Rimozione del driver WPDUSB.SYS per dispositivi portatili Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d602c8277a5c256332b3eaec6a383997d5c63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317611"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="91746-103">Rimozione del driver WPDUSB.SYS per dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="91746-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="91746-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="91746-104">Affected Platforms</span></span>

<span data-ttu-id="91746-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="91746-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="91746-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="91746-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="91746-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="91746-107">Feature Impact</span></span>

 <span data-ttu-id="91746-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="91746-108">**Severity** - Low</span></span>  
<span data-ttu-id="91746-109">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="91746-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="91746-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91746-110">Description</span></span>

<span data-ttu-id="91746-111">Microsoft ha sostituito il componente modalità kernel dello stack di driver USB di Windows Vista (WPDUSB.SYS) per i dispositivi portatili Windows (WPD) con il driver di WINUSB.SYS generico.</span><span class="sxs-lookup"><span data-stu-id="91746-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="91746-112">La comunicazione con il driver di WPDUSB.SYS originale è stata tramite codici IOCTL (private I/O Control); anche il supporto di questi elementi è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="91746-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="91746-113">Tutti i consumer di questi codici IOCTL sarebbero stati responsabili dell'interpretazione e dell'implementazione corrette del protocollo MTP (Media Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="91746-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="91746-114">Windows Vista non supportava l'utilizzo di questi codici IOCTL da parte di applicazioni di terze parti.</span><span class="sxs-lookup"><span data-stu-id="91746-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="91746-115">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="91746-115">Manifestation of Impact</span></span>

<span data-ttu-id="91746-116">Qualsiasi applicazione che dipende dalla disponibilità di questi codici IOCTL privati non avrà più accesso ai dispositivi MTP connessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="91746-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="91746-117">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="91746-117">Mitigation</span></span>

<span data-ttu-id="91746-118">Gli utenti di un'applicazione che dipende dai codici IOCTL privati devono usare un'applicazione diversa o una versione aggiornata dell'applicazione per accedere al dispositivo MTP connesso tramite USB.</span><span class="sxs-lookup"><span data-stu-id="91746-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="91746-119">Soluzione</span><span class="sxs-lookup"><span data-stu-id="91746-119">Solution</span></span>

<span data-ttu-id="91746-120">Per individuare e interagire con qualsiasi dispositivo WPD, le applicazioni devono usare l'API dispositivi portatili Windows (WPD).</span><span class="sxs-lookup"><span data-stu-id="91746-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="91746-121">Sebbene una percentuale significativa di dispositivi WPD implementi MTP per la comunicazione con il PC, WPD non è limitato solo ai dispositivi MTP.</span><span class="sxs-lookup"><span data-stu-id="91746-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="91746-122">Inoltre, quando l'accesso diretto al dispositivo tramite le IOCTL private avrebbe limitato l'applicazione alla comunicazione con solo i dispositivi connessi tramite USB, l'uso dell'API WPD espande l'elenco di opzioni di connettività ad altri protocolli di comunicazione, ad esempio Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="91746-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="91746-123">Nei rari casi in cui l'applicazione deve essere compatibile con MTP, l'API WPD fornisce un meccanismo pass-through per i comandi MTP non elaborati.</span><span class="sxs-lookup"><span data-stu-id="91746-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="91746-124">Sfruttando le funzionalità</span><span class="sxs-lookup"><span data-stu-id="91746-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="91746-125">L'API WPD è supportata in Windows XP (tramite Windows Format SDK), Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="91746-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="91746-126">L'implementazione di Windows 7 di WPD aggiunge il supporto per MTP su Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="91746-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="91746-127">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="91746-127">Links to Other Resources</span></span>

[<span data-ttu-id="91746-128">Dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="91746-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
