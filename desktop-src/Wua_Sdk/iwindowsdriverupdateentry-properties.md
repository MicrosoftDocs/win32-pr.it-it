---
description: L'interfaccia IWindowsDriverUpdateEntry definisce le proprietà seguenti.
ms.assetid: a0ff6ec2-13fe-4c0c-b375-9df55e1c1bb4
title: Proprietà di IWindowsDriverUpdateEntry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae63775bd7b13c67b4ec96c70107069730f828d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129607"
---
# <a name="iwindowsdriverupdateentry-properties"></a><span data-ttu-id="4b744-103">Proprietà di IWindowsDriverUpdateEntry</span><span class="sxs-lookup"><span data-stu-id="4b744-103">IWindowsDriverUpdateEntry Properties</span></span>

<span data-ttu-id="4b744-104">L'interfaccia [**IWindowsDriverUpdateEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdateentry) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="4b744-104">The [**IWindowsDriverUpdateEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdateentry) interface defines the following properties.</span></span>



| <span data-ttu-id="4b744-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b744-105">Property</span></span>                                                                     | <span data-ttu-id="4b744-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b744-106">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b744-107">**DeviceProblemNumber**</span><span class="sxs-lookup"><span data-stu-id="4b744-107">**DeviceProblemNumber**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_deviceproblemnumber) | <span data-ttu-id="4b744-108">Ottiene il numero di problema del dispositivo che corrisponde per l'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="4b744-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                                    |
| [<span data-ttu-id="4b744-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="4b744-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_devicestatus)               | <span data-ttu-id="4b744-110">Ottiene lo stato del dispositivo che corrisponde a per l'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="4b744-110">Gets the status of the device that matches for the Windows driver update.</span></span>                                            |
| [<span data-ttu-id="4b744-111">**DriverClass**</span><span class="sxs-lookup"><span data-stu-id="4b744-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverclass)                 | <span data-ttu-id="4b744-112">Ottiene la classe dell'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="4b744-112">Gets the class of the Windows driver update.</span></span>                                                                         |
| [<span data-ttu-id="4b744-113">**DriverHardwareID**</span><span class="sxs-lookup"><span data-stu-id="4b744-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverhardwareid)       | <span data-ttu-id="4b744-114">Ottiene l'hardware o l'identificatore compatibile che l'aggiornamento del driver di Windows deve corrispondere per poter essere installato.</span><span class="sxs-lookup"><span data-stu-id="4b744-114">Gets the hardware or the compatible identifier that the Windows driver update must match in order to be installable.</span></span> |
| [<span data-ttu-id="4b744-115">**DriverManufacturer**</span><span class="sxs-lookup"><span data-stu-id="4b744-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_drivermanufacturer)   | <span data-ttu-id="4b744-116">Ottiene il nome invariante della lingua del produttore dell'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="4b744-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                                   |
| [<span data-ttu-id="4b744-117">**DriverModel**</span><span class="sxs-lookup"><span data-stu-id="4b744-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_drivermodel)                 | <span data-ttu-id="4b744-118">Ottiene il nome del modello invariante della lingua del dispositivo a cui è destinato l'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="4b744-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span>                |
| [<span data-ttu-id="4b744-119">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="4b744-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverprovider)           | <span data-ttu-id="4b744-120">Ottiene il nome invariante della lingua del provider dell'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="4b744-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                                       |
| [<span data-ttu-id="4b744-121">**DriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="4b744-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driververdate)             | <span data-ttu-id="4b744-122">Ottiene la data della versione del driver dell'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="4b744-122">Gets the driver version date of the Windows driver update.</span></span>                                                           |



 

 

 



