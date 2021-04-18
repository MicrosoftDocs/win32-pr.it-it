---
description: Le funzioni amministrative seguenti consentono a un provider di rete di eseguire un'azione specifica della rete per visualizzare e modificare le directory specifiche della rete, ovvero le directory di cui è stato eseguito il mapping a protocolli non Windows.
ms.assetid: df2f1bd6-5257-46e4-a4d4-ad2f5c0a1517
title: Funzioni amministrative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83cb5b7c515fe8e22dc5542a4d29e54e8b01329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316239"
---
# <a name="administrative-functions"></a><span data-ttu-id="796b2-103">Funzioni amministrative</span><span class="sxs-lookup"><span data-stu-id="796b2-103">Administrative Functions</span></span>

<span data-ttu-id="796b2-104">Le funzioni amministrative seguenti consentono a un provider di rete di eseguire un'azione specifica della rete per visualizzare e modificare le directory specifiche della rete, ovvero le directory di cui è stato eseguito il mapping a protocolli non Windows.</span><span class="sxs-lookup"><span data-stu-id="796b2-104">The following administrative functions enable a network provider to take network-specific action to display and manipulate network-specific directories, in other words, directories mapped to non-Windows protocols.</span></span>



| <span data-ttu-id="796b2-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="796b2-105">Function</span></span>                                         | <span data-ttu-id="796b2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="796b2-106">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="796b2-107">**NPGetDirectoryType**</span><span class="sxs-lookup"><span data-stu-id="796b2-107">**NPGetDirectoryType**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) | <span data-ttu-id="796b2-108">Chiamato da Gestione file per determinare il tipo di una directory di rete.</span><span class="sxs-lookup"><span data-stu-id="796b2-108">Called by File Manager to determine the type of a network directory.</span></span>                                                                                          |
| [<span data-ttu-id="796b2-109">**NPDirectoryNotify**</span><span class="sxs-lookup"><span data-stu-id="796b2-109">**NPDirectoryNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npdirectorynotify)   | <span data-ttu-id="796b2-110">Chiamato da Gestione file per notificare al provider di rete le operazioni di directory.</span><span class="sxs-lookup"><span data-stu-id="796b2-110">Called by File Manager to notify the network provider of directory operations.</span></span> <span data-ttu-id="796b2-111">Questa funzione può essere utilizzata per eseguire un comportamento speciale per determinate directory.</span><span class="sxs-lookup"><span data-stu-id="796b2-111">This function can be used to perform special behavior for certain directories.</span></span> |



 

 

 



