---
description: Rimozione di WPDUSB.SYS driver per dispositivi portatili Windows
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Rimozione di WPDUSB.SYS driver per dispositivi portatili Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116249"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="7d9eb-103">Rimozione di WPDUSB.SYS driver per dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="7d9eb-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="7d9eb-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="7d9eb-104">Affected Platforms</span></span>

<span data-ttu-id="7d9eb-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d9eb-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="7d9eb-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d9eb-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="7d9eb-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="7d9eb-107">Feature Impact</span></span>

 <span data-ttu-id="7d9eb-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="7d9eb-108">**Severity** - Low</span></span>  
<span data-ttu-id="7d9eb-109">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="7d9eb-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="7d9eb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d9eb-110">Description</span></span>

<span data-ttu-id="7d9eb-111">Microsoft ha sostituito il componente in modalità kernel dello stack di driver USB di Windows Vista (WPDUSB.SYS) per dispositivi portatili Windows (WPD) con il driver WINUSB.SYS generico.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="7d9eb-112">La comunicazione con il driver WPDUSB.SYS originale è stata tramite codici I/O control (IOCTL) privati; Anche il supporto di questi elementi è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="7d9eb-113">Tutti i consumer di questi codici IOCTL sarebbero stati responsabili dell'interpretazione e dell'implementazione appropriate del protocollo MTP (Media Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="7d9eb-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="7d9eb-114">Windows Vista non supporta l'uso di questi codici IOCTL da parte di applicazioni di terze parti.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="7d9eb-115">Impatto significativo</span><span class="sxs-lookup"><span data-stu-id="7d9eb-115">Manifestation of Impact</span></span>

<span data-ttu-id="7d9eb-116">Qualsiasi applicazione che dipendeva dalla disponibilità di questi codici IOCTL privati non avrebbe più accesso ai dispositivi MTP connessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="7d9eb-117">Mitigazione</span><span class="sxs-lookup"><span data-stu-id="7d9eb-117">Mitigation</span></span>

<span data-ttu-id="7d9eb-118">Gli utenti di un'applicazione che dipende dai codici IOCTL privati devono usare un'applicazione diversa (o una versione aggiornata dell'applicazione) per accedere al dispositivo MTP connesso tramite USB.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="7d9eb-119">Soluzione</span><span class="sxs-lookup"><span data-stu-id="7d9eb-119">Solution</span></span>

<span data-ttu-id="7d9eb-120">Le applicazioni devono usare l'API WPD (Windows Portable Devices) per trovare e interagire con qualsiasi dispositivo WPD.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="7d9eb-121">Anche se una percentuale significativa di dispositivi WPD implementa MTP per la comunicazione con il PC, la WPD non è limitata ai soli dispositivi MTP.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="7d9eb-122">Inoltre, se l'accesso diretto al dispositivo tramite gli IOCL privati avrebbe limitato l'applicazione alla comunicazione solo con dispositivi connessi tramite USB, l'uso dell'API WPD espande l'elenco delle opzioni di connettività ad altri protocolli di comunicazione (ad esempio, Wi-Fi).</span><span class="sxs-lookup"><span data-stu-id="7d9eb-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="7d9eb-123">Nei rari casi in cui l'applicazione deve essere in grado di riconoscere MTP, l'API WPD fornisce un meccanismo pass-through per i comandi MTP non elaborati.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="7d9eb-124">Uso delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="7d9eb-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="7d9eb-125">L'API WPD è supportata in Windows XP (tramite Windows Format SDK), Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="7d9eb-126">L'implementazione di Windows 7 di WPD aggiunge il supporto per MTP tramite Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="7d9eb-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7d9eb-127">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="7d9eb-127">Links to Other Resources</span></span>

[<span data-ttu-id="7d9eb-128">Dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="7d9eb-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
