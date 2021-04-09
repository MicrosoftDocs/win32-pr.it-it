---
description: Le funzioni seguenti vengono usate per la gestione dei dispositivi.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Funzioni di gestione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966086"
---
# <a name="device-management-functions"></a><span data-ttu-id="2b775-103">Funzioni di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="2b775-103">Device Management Functions</span></span>

<span data-ttu-id="2b775-104">Le funzioni seguenti vengono usate per la gestione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="2b775-104">The following functions are used in device management.</span></span>



| <span data-ttu-id="2b775-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="2b775-105">Function</span></span>                                                             | <span data-ttu-id="2b775-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b775-106">Description</span></span>                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b775-107">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="2b775-107">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | <span data-ttu-id="2b775-108">Invia un codice di controllo direttamente a un driver di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="2b775-108">Sends a control code directly to a specified device driver.</span></span>                           |
| [<span data-ttu-id="2b775-109">**InstallNewDevice**</span><span class="sxs-lookup"><span data-stu-id="2b775-109">**InstallNewDevice**</span></span>](installnewdevice.md)                         | <span data-ttu-id="2b775-110">Installa un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b775-110">Installs a new device.</span></span> <span data-ttu-id="2b775-111">All'utente viene richiesto di selezionare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b775-111">The user is prompted to select the device.</span></span>                     |
| [<span data-ttu-id="2b775-112">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="2b775-112">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | <span data-ttu-id="2b775-113">Registra il dispositivo o il tipo di dispositivo per il quale una finestra riceverà le notifiche.</span><span class="sxs-lookup"><span data-stu-id="2b775-113">Registers the device or type of device for which a window will receive notifications.</span></span> |
| [<span data-ttu-id="2b775-114">**UnregisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="2b775-114">**UnregisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | <span data-ttu-id="2b775-115">Chiude l'handle di notifica del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="2b775-115">Closes the specified device notification handle.</span></span>                                      |



 

<span data-ttu-id="2b775-116">Le funzioni seguenti vengono utilizzate con le unità CD-ROM e DVD.</span><span class="sxs-lookup"><span data-stu-id="2b775-116">The following functions are used with CD-ROM and DVD drives.</span></span>



| <span data-ttu-id="2b775-117">Funzione</span><span class="sxs-lookup"><span data-stu-id="2b775-117">Function</span></span>                                                               | <span data-ttu-id="2b775-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b775-118">Description</span></span>                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b775-119">**CdromDisableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="2b775-119">**CdromDisableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | <span data-ttu-id="2b775-120">Disabilita la riproduzione digitale per l'unità CD-ROM o DVD specificata.</span><span class="sxs-lookup"><span data-stu-id="2b775-120">Disables digital playback for the specified CD-ROM or DVD drive.</span></span>                                    |
| [<span data-ttu-id="2b775-121">**CdromEnableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="2b775-121">**CdromEnableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | <span data-ttu-id="2b775-122">Abilita la riproduzione digitale per l'unità CD-ROM o DVD specificata.</span><span class="sxs-lookup"><span data-stu-id="2b775-122">Enables digital playback for the specified CD-ROM or DVD drive.</span></span>                                     |
| [<span data-ttu-id="2b775-123">**CdromIsDigitalPlaybackEnabled**</span><span class="sxs-lookup"><span data-stu-id="2b775-123">**CdromIsDigitalPlaybackEnabled**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | <span data-ttu-id="2b775-124">Determina se la riproduzione digitale è abilitata per l'unità CD-ROM o DVD specificata.</span><span class="sxs-lookup"><span data-stu-id="2b775-124">Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.</span></span>               |
| [<span data-ttu-id="2b775-125">**CdromKnownGoodDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="2b775-125">**CdromKnownGoodDigitalPlayback**</span></span>](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | <span data-ttu-id="2b775-126">Determina se l'unità CD-ROM o DVD specificata ha una riproduzione digitale che è nota come corretta.</span><span class="sxs-lookup"><span data-stu-id="2b775-126">Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.</span></span> |
| [<span data-ttu-id="2b775-127">**DvdLauncher**</span><span class="sxs-lookup"><span data-stu-id="2b775-127">**DvdLauncher**</span></span>](dvdlauncher.md)                                     | <span data-ttu-id="2b775-128">Verifica che l'area multimediale nell'unità DVD corrisponda all'area dell'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="2b775-128">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>                       |



 

 

 
