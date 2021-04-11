---
description: Requisiti generali per lo sviluppo di applicazioni
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisiti generali per lo sviluppo di applicazioni (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232308"
---
# <a name="general-requirements-for-application-development-wpd-api"></a><span data-ttu-id="a5489-103">Requisiti generali per lo sviluppo di applicazioni (API WPD)</span><span class="sxs-lookup"><span data-stu-id="a5489-103">General Requirements for Application Development (WPD API)</span></span>

<span data-ttu-id="a5489-104">Per creare un'applicazione per dispositivi portatili Windows, è necessario che nel computer sia installato [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) .</span><span class="sxs-lookup"><span data-stu-id="a5489-104">To create a Windows Portable Devices application, you must have the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) installed on your computer.</span></span> <span data-ttu-id="a5489-105">Le intestazioni e le librerie richieste sono incluse nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="a5489-105">The required headers and libraries appear in the following list.</span></span>

-   <span data-ttu-id="a5489-106">PortableDeviceGuids. lib</span><span class="sxs-lookup"><span data-stu-id="a5489-106">PortableDeviceGuids.lib</span></span>
-   <span data-ttu-id="a5489-107">PortableDevice. h</span><span class="sxs-lookup"><span data-stu-id="a5489-107">PortableDevice.h</span></span>
-   <span data-ttu-id="a5489-108">PortableDeviceTypes. h</span><span class="sxs-lookup"><span data-stu-id="a5489-108">PortableDeviceTypes.h</span></span>
-   <span data-ttu-id="a5489-109">PortableDeviceApi. h</span><span class="sxs-lookup"><span data-stu-id="a5489-109">PortableDeviceApi.h</span></span>
-   <span data-ttu-id="a5489-110">Qualsiasi altra libreria e intestazione richiesta richiesta dall'applicazione per utilizzare o eseguire il rendering dei file multimediali.</span><span class="sxs-lookup"><span data-stu-id="a5489-110">Any other required libraries and headers required by your application to consume or render media files.</span></span>

<span data-ttu-id="a5489-111">Se l'applicazione supporta le nuove interfacce di servizi per dispositivi, includerà anche uno o più dei file di intestazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="a5489-111">If your application supports the new Device Services interfaces, it will also include one or more of the following header files.</span></span>

-   <span data-ttu-id="a5489-112">AnchorSyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-112">AnchorSyncDeviceService.h</span></span>
-   <span data-ttu-id="a5489-113">BridgeDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-113">BridgeDeviceService.h</span></span>
-   <span data-ttu-id="a5489-114">CalendarDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-114">CalendarDeviceService.h</span></span>
-   <span data-ttu-id="a5489-115">ContactDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-115">ContactDeviceService.h</span></span>
-   <span data-ttu-id="a5489-116">DeviceServices. h</span><span class="sxs-lookup"><span data-stu-id="a5489-116">DeviceServices.h</span></span>
-   <span data-ttu-id="a5489-117">FullEnumSyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-117">FullEnumSyncDeviceService.h</span></span>
-   <span data-ttu-id="a5489-118">HintsDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-118">HintsDeviceService.h</span></span>
-   <span data-ttu-id="a5489-119">MessageDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-119">MessageDeviceService.h</span></span>
-   <span data-ttu-id="a5489-120">MetadataDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-120">MetadataDeviceService.h</span></span>
-   <span data-ttu-id="a5489-121">NotesDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-121">NotesDeviceService.h</span></span>
-   <span data-ttu-id="a5489-122">RingtoneDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-122">RingtoneDeviceService.h</span></span>
-   <span data-ttu-id="a5489-123">StatusDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-123">StatusDeviceService.h</span></span>
-   <span data-ttu-id="a5489-124">SyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-124">SyncDeviceService.h</span></span>
-   <span data-ttu-id="a5489-125">TaskDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="a5489-125">TaskDeviceService.h</span></span>

<span data-ttu-id="a5489-126">Dei file nell'elenco precedente, BridgeDeviceService. h e DeviceService. h sono necessari per quasi tutte le applicazioni che supportano i servizi dispositivo; gli altri file definiscono tipi diversi di servizi per dispositivi e verrebbero inclusi nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a5489-126">Of the files in the previous list, BridgeDeviceService.h and DeviceService.h are required for almost any application that supports Device Services; the other files define different types of device services and would be included as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5489-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5489-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5489-128">**Dispositivi portatili Windows**</span><span class="sxs-lookup"><span data-stu-id="a5489-128">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
