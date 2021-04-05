---
description: L'interfaccia IUpdateDownloader definisce le proprietà seguenti.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Proprietà di IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752082"
---
# <a name="iupdatedownloader-properties"></a><span data-ttu-id="2d8c6-103">Proprietà di IUpdateDownloader</span><span class="sxs-lookup"><span data-stu-id="2d8c6-103">IUpdateDownloader Properties</span></span>

<span data-ttu-id="2d8c6-104">L'interfaccia [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d8c6-104">The [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) interface defines the following properties.</span></span>



| <span data-ttu-id="2d8c6-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d8c6-105">Property</span></span>                                                             | <span data-ttu-id="2d8c6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d8c6-106">Description</span></span>                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d8c6-107">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="2d8c6-107">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | <span data-ttu-id="2d8c6-108">Ottiene e imposta l'applicazione client corrente.</span><span class="sxs-lookup"><span data-stu-id="2d8c6-108">Gets and sets the current client application.</span></span>                                                                                                                              |
| [<span data-ttu-id="2d8c6-109">**IsForced**</span><span class="sxs-lookup"><span data-stu-id="2d8c6-109">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | <span data-ttu-id="2d8c6-110">Ottiene e imposta un valore booleano che indica se l'agente di Windows Update (WUA) forza il download degli aggiornamenti già installati o che non possono essere installati.</span><span class="sxs-lookup"><span data-stu-id="2d8c6-110">Gets and sets a Boolean value that indicates whether the Windows Update Agent (WUA) forces the download of updates that are already installed or that cannot be installed.</span></span> |
| [<span data-ttu-id="2d8c6-111">**Priority**</span><span class="sxs-lookup"><span data-stu-id="2d8c6-111">**Priority**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | <span data-ttu-id="2d8c6-112">Ottiene e imposta il livello di priorità del download.</span><span class="sxs-lookup"><span data-stu-id="2d8c6-112">Gets and sets the priority level of the download.</span></span>                                                                                                                          |
| [<span data-ttu-id="2d8c6-113">**Aggiornamenti**</span><span class="sxs-lookup"><span data-stu-id="2d8c6-113">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | <span data-ttu-id="2d8c6-114">Ottiene e imposta un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati per il download.</span><span class="sxs-lookup"><span data-stu-id="2d8c6-114">Gets and sets an interface that contains a read-only collection of the updates that are specified for download.</span></span>                                                            |



 

 

 



