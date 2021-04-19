---
description: L'interfaccia IWindowsDriverUpdate definisce le proprietà seguenti.
ms.assetid: 2177c5e0-47db-44ae-a0ce-2544ff2d0855
title: Proprietà di IWindowsDriverUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291d7933cf3e73dee6f47edab3240c4ebd14f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307591"
---
# <a name="iwindowsdriverupdate-properties"></a><span data-ttu-id="ce5b0-103">Proprietà di IWindowsDriverUpdate</span><span class="sxs-lookup"><span data-stu-id="ce5b0-103">IWindowsDriverUpdate Properties</span></span>

<span data-ttu-id="ce5b0-104">L'interfaccia [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-104">The [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="ce5b0-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce5b0-105">Property</span></span>                                                                                                    | <span data-ttu-id="ce5b0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce5b0-106">Description</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5b0-107">[](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Indirizzo** DeviceProblemNumber](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span><span class="sxs-lookup"><span data-stu-id="ce5b0-107">[**DeviceProblemNumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Address**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span></span> | <span data-ttu-id="ce5b0-108">Ottiene il numero di problema del dispositivo che corrisponde per l'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                     |
| [<span data-ttu-id="ce5b0-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="ce5b0-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_devicestatus)                                                   | <span data-ttu-id="ce5b0-110">Ottiene lo stato del dispositivo che corrisponde a per l'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-110">Gets the status of the device that matches for the Windows driver update.</span></span>                             |
| [<span data-ttu-id="ce5b0-111">**DriverClass**</span><span class="sxs-lookup"><span data-stu-id="ce5b0-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverclass)                                                     | <span data-ttu-id="ce5b0-112">Ottiene la classe dell'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-112">Gets the class of the Windows driver update.</span></span>                                                          |
| [<span data-ttu-id="ce5b0-113">**DriverHardwareID**</span><span class="sxs-lookup"><span data-stu-id="ce5b0-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverhardwareid)                                           | <span data-ttu-id="ce5b0-114">Ottiene l'ID hardware o l'ID compatibile che l'aggiornamento del driver di Windows deve corrispondere per essere installabile.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-114">Gets the hardware ID or compatible ID that the Windows driver update must match to be installable.</span></span>    |
| [<span data-ttu-id="ce5b0-115">**DriverManufacturer**</span><span class="sxs-lookup"><span data-stu-id="ce5b0-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermanufacturer)                                       | <span data-ttu-id="ce5b0-116">Ottiene il nome invariante della lingua del produttore dell'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                    |
| [<span data-ttu-id="ce5b0-117">**DriverModel**</span><span class="sxs-lookup"><span data-stu-id="ce5b0-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermodel)                                                     | <span data-ttu-id="ce5b0-118">Ottiene il nome del modello invariante della lingua del dispositivo a cui è destinato l'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span> |
| [<span data-ttu-id="ce5b0-119">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="ce5b0-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverprovider)                                               | <span data-ttu-id="ce5b0-120">Ottiene il nome invariante della lingua del provider dell'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                        |
| [<span data-ttu-id="ce5b0-121">**DriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="ce5b0-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driververdate)                                                 | <span data-ttu-id="ce5b0-122">Ottiene la data della versione del driver dell'aggiornamento del driver di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce5b0-122">Gets the driver version date of the Windows driver update.</span></span>                                            |



 

 

 



