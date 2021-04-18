---
description: Interfaccia di programmazione dell'applicazione WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Interfaccia di programmazione dell'applicazione WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316368"
---
# <a name="wpd-application-programming-interface"></a><span data-ttu-id="32d89-103">Interfaccia di programmazione dell'applicazione WPD</span><span class="sxs-lookup"><span data-stu-id="32d89-103">WPD Application Programming Interface</span></span>

<span data-ttu-id="32d89-104">Le applicazioni basate sui dispositivi portatili Windows possono esplorare un dispositivo, inviare e ricevere contenuto e persino controllare il dispositivo, ad esempio, scattare un'immagine o inviare un SMS.</span><span class="sxs-lookup"><span data-stu-id="32d89-104">Applications built on Windows Portable Devices can explore a device, send and receive content, and even control the device, for example, take a picture or send a text message.</span></span> <span data-ttu-id="32d89-105">Il sistema è progettato per essere flessibile, in modo che molti tipi di dispositivi possano essere esplorati ed estendibile in modo che gli sviluppatori di driver possano definire proprietà e comandi personalizzati per i dispositivi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="32d89-105">The system is designed to be flexible so that many types of devices can be explored, and extensible so that driver developers can define custom properties and commands for custom devices.</span></span>

<span data-ttu-id="32d89-106">La tabella seguente descrive gli argomenti principali di questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="32d89-106">The following table describes the main topics of this documentation.</span></span>



| <span data-ttu-id="32d89-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="32d89-107">Topic</span></span>                                                                                                                  | <span data-ttu-id="32d89-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32d89-108">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32d89-109">Requisiti generali per lo sviluppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="32d89-109">General Requirements for Application Development</span></span>](general-requirements-for-application-development.md)               | <span data-ttu-id="32d89-110">Requisiti hardware e software per sviluppare driver e applicazioni mediante dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="32d89-110">Hardware and software requirements to develop drivers and applications using Windows Portable Devices.</span></span>     |
| [<span data-ttu-id="32d89-111">Requisiti per le applicazioni Windows Media DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="32d89-111">Requirements for Windows Media DRM-Enabled Applications</span></span>](requirements-for-windows-media-drm-enabled-applications.md) | <span data-ttu-id="32d89-112">Proprietà necessarie per abilitare i trasferimenti di contenuto protetti da DRM di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="32d89-112">Properties that are required to enable Windows Media DRM-protected content transfers.</span></span>                      |
| [<span data-ttu-id="32d89-113">Esempi</span><span class="sxs-lookup"><span data-stu-id="32d89-113">Samples</span></span>](sample.md)                                                                                                  | <span data-ttu-id="32d89-114">Descrizione di due applicazioni desktop da riga di comando fornite con questo Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="32d89-114">Description of two command-line desktop applications that are supplied with this software development kit.</span></span> |
| [<span data-ttu-id="32d89-115">Panoramica dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="32d89-115">Application Overview</span></span>](application-overview.md)                                                                       | <span data-ttu-id="32d89-116">Concetti chiave usati nei dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="32d89-116">Key concepts used in Windows Portable Devices.</span></span>                                                             |
| [<span data-ttu-id="32d89-117">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="32d89-117">Programming Guide</span></span>](programming-guide.md)                                                                             | <span data-ttu-id="32d89-118">Attività principali che un'applicazione eseguirà con istruzioni dettagliate e frammenti di codice.</span><span class="sxs-lookup"><span data-stu-id="32d89-118">Key tasks that an application will perform, with step-by-step instructions and code snippets.</span></span>              |
| [<span data-ttu-id="32d89-119">Guida di riferimento alla programmazione</span><span class="sxs-lookup"><span data-stu-id="32d89-119">Programming Reference</span></span>](programming-reference.md)                                                                     | <span data-ttu-id="32d89-120">Guida di riferimento per le interfacce e i tipi di dati definiti dai dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="32d89-120">Reference guide to the interfaces and data types defined by Windows Portable Devices.</span></span>                      |



 

<span data-ttu-id="32d89-121">Le applicazioni basate su Windows Media Gestione dispositivi o l'acquisizione di immagini Windows possono accedere ai dispositivi portatili Windows tramite un livello di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="32d89-121">Applications built on Windows Media Device Manager or Windows Image Acquisition can access Windows Portable Devices through a compatibility layer.</span></span>

<span data-ttu-id="32d89-122">Microsoft fornisce diversi driver per i protocolli e i dispositivi standard, inclusi i dispositivi MTP (Media Transport Protocol) e i dispositivi di classe di archiviazione di massa (MSC).</span><span class="sxs-lookup"><span data-stu-id="32d89-122">Microsoft provides several drivers for standard protocols and devices, including Media Transport Protocol (MTP) devices and Mass Storage Class (MSC) devices.</span></span> <span data-ttu-id="32d89-123">Se si ha familiarità con il Framework di driver User-Mode, è possibile sviluppare i propri driver per i dispositivi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="32d89-123">If you are familiar with the User-Mode Driver Framework, you can develop your own drivers for custom devices.</span></span>

 

 



