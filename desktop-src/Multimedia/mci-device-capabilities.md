---
title: Funzionalità del dispositivo MCI
description: Funzionalità del dispositivo MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig (macro)
- MCIWndCanEject (macro)
- MCIWndCanPlay (macro)
- MCIWndCanRecord (macro)
- MCIWndCanSave (macro)
- MCIWndCanWindow (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045265"
---
# <a name="mci-device-capabilities"></a><span data-ttu-id="1a9af-109">Funzionalità del dispositivo MCI</span><span class="sxs-lookup"><span data-stu-id="1a9af-109">MCI Device Capabilities</span></span>

<span data-ttu-id="1a9af-110">MCIWnd include le macro seguenti per consentire l'esecuzione di query sui dispositivi MCI per le rispettive funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1a9af-110">MCIWnd includes the following macros to let you query MCI devices for their capabilities.</span></span>



| <span data-ttu-id="1a9af-111">Macro</span><span class="sxs-lookup"><span data-stu-id="1a9af-111">Macro</span></span>                                      | <span data-ttu-id="1a9af-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a9af-112">Description</span></span>                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a9af-113">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="1a9af-113">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | <span data-ttu-id="1a9af-114">Determina se un dispositivo ha una finestra di dialogo di configurazione per supportare più configurazioni, ad esempio il dispositivo MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="1a9af-114">Determines whether a device has a configuration dialog box to support multiple configurations, such as the MCIAVI device.</span></span>                   |
| [<span data-ttu-id="1a9af-115">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="1a9af-115">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | <span data-ttu-id="1a9af-116">Determina se un dispositivo dispone di una funzione di espulsione controllata dal software.</span><span class="sxs-lookup"><span data-stu-id="1a9af-116">Determines whether a device has a software-controlled eject function.</span></span>                                                                       |
| [<span data-ttu-id="1a9af-117">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="1a9af-117">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | <span data-ttu-id="1a9af-118">Determina se un dispositivo è in grado di riprodurre il contenuto esistente.</span><span class="sxs-lookup"><span data-stu-id="1a9af-118">Determines whether a device can play the existing content.</span></span>                                                                                  |
| [<span data-ttu-id="1a9af-119">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="1a9af-119">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | <span data-ttu-id="1a9af-120">Determina se un dispositivo è in grado di registrare.</span><span class="sxs-lookup"><span data-stu-id="1a9af-120">Determines whether a device can record.</span></span>                                                                                                     |
| [<span data-ttu-id="1a9af-121">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="1a9af-121">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | <span data-ttu-id="1a9af-122">Determina se un dispositivo può archiviare i dati.</span><span class="sxs-lookup"><span data-stu-id="1a9af-122">Determines whether a device can store data.</span></span>                                                                                                 |
| [<span data-ttu-id="1a9af-123">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="1a9af-123">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | <span data-ttu-id="1a9af-124">Determina se un dispositivo supporta i comandi della finestra MCI, ad esempio [**finestra**](window.md), [**put**](put.md) e [**where**](where.md).</span><span class="sxs-lookup"><span data-stu-id="1a9af-124">Determines whether a device supports MCI window commands (such as [**window**](window.md), [**put**](put.md) and [**where**](where.md)).</span></span> |



 

<span data-ttu-id="1a9af-125">Queste macro restituiscono **true** se il dispositivo supporta la funzionalità specifica o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1a9af-125">These macros return **TRUE** if the device supports the specific capability, or **FALSE** otherwise.</span></span>

 

 




