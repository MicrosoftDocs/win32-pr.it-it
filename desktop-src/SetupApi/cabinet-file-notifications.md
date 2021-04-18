---
description: Le notifiche seguenti vengono inviate da SetupIterateCabinet. Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere notifiche.
ms.assetid: 5a362a93-ebe8-4995-aacc-13ee10d3407a
title: Notifiche file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3e4eb7645fc3603f026db6bde3ce92f2ed2ce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306512"
---
# <a name="cabinet-file-notifications"></a><span data-ttu-id="b9534-104">Notifiche file CAB</span><span class="sxs-lookup"><span data-stu-id="b9534-104">Cabinet File Notifications</span></span>

<span data-ttu-id="b9534-105">Le notifiche seguenti vengono inviate da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="b9534-105">The following notifications are sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="b9534-106">Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere [notifiche](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b9534-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="b9534-107">Notifica</span><span class="sxs-lookup"><span data-stu-id="b9534-107">Notification</span></span>                                                        | <span data-ttu-id="b9534-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9534-108">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="b9534-109">**SPFILENOTIFY \_ FILEextracted**</span><span class="sxs-lookup"><span data-stu-id="b9534-109">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="b9534-110">Il file è stato estratto dal file CAB.</span><span class="sxs-lookup"><span data-stu-id="b9534-110">The file has been extracted from the cabinet.</span></span>                                  |
| [<span data-ttu-id="b9534-111">**\_FILEINCABINET SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b9534-111">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="b9534-112">Un file viene rilevato nell'archivio, l'applicazione vuole estrarla?</span><span class="sxs-lookup"><span data-stu-id="b9534-112">A file is encountered in the cabinet, does the application want to extract it?</span></span> |
| [<span data-ttu-id="b9534-113">**\_NEEDNEWCABINET SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b9534-113">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="b9534-114">Il file corrente viene continuato nel file CAB successivo.</span><span class="sxs-lookup"><span data-stu-id="b9534-114">The current file is continued in the next cabinet.</span></span>                             |



 

 

 



