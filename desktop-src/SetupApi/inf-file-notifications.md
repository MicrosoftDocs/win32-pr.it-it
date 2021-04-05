---
description: Le notifiche seguenti vengono utilizzate con le funzioni SetupInstallFile, SetupInstallFileEx e SetupInstallFromInfSection. Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere notifiche.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Notifiche file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967611"
---
# <a name="inf-file-notifications"></a><span data-ttu-id="eb18f-104">Notifiche file INF</span><span class="sxs-lookup"><span data-stu-id="eb18f-104">INF File Notifications</span></span>

<span data-ttu-id="eb18f-105">Le notifiche seguenti vengono utilizzate con le funzioni [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) .</span><span class="sxs-lookup"><span data-stu-id="eb18f-105">The following notifications are used with the [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) functions.</span></span> <span data-ttu-id="eb18f-106">Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere [notifiche](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="eb18f-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="eb18f-107">Notifica</span><span class="sxs-lookup"><span data-stu-id="eb18f-107">Notification</span></span>                                                      | <span data-ttu-id="eb18f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb18f-108">Description</span></span>                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb18f-109">**\_FILEOPDELAYED SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="eb18f-109">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md) | <span data-ttu-id="eb18f-110">Il file è in uso e l'operazione corrente viene posticipata fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="eb18f-110">The file is in use, and the current operation is delayed until the system is rebooted.</span></span> |
| [<span data-ttu-id="eb18f-111">**\_LANGMISMATCH SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="eb18f-111">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)   | <span data-ttu-id="eb18f-112">La lingua del file corrente non corrisponde alla lingua del sistema.</span><span class="sxs-lookup"><span data-stu-id="eb18f-112">The language of the current file does not match the system language.</span></span>                   |
| [<span data-ttu-id="eb18f-113">**\_TARGETEXISTS SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="eb18f-113">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)   | <span data-ttu-id="eb18f-114">Una copia del file specificato esiste già nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="eb18f-114">A copy of the specified file already exists on the target.</span></span>                             |
| [<span data-ttu-id="eb18f-115">**\_TARGETNEWER SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="eb18f-115">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)     | <span data-ttu-id="eb18f-116">Nella destinazione è presente una versione più recente del file specificato.</span><span class="sxs-lookup"><span data-stu-id="eb18f-116">A newer version of the specified file exists on the target.</span></span>                            |



 

> [!Note]  
> <span data-ttu-id="eb18f-117">Poiché [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crea ed Esegui il commit di una coda di file interna, USA anche le [notifiche della coda di file](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="eb18f-117">Because [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) creates and commits an internal file queue, it also uses the [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 

 



