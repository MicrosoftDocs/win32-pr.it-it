---
description: Interfacce utilizzate con le quote disco.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Interfacce di quota disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485621"
---
# <a name="disk-quota-interfaces"></a><span data-ttu-id="f5d6e-103">Interfacce di quota disco</span><span class="sxs-lookup"><span data-stu-id="f5d6e-103">Disk Quota Interfaces</span></span>

<span data-ttu-id="f5d6e-104">Con le quote disco vengono utilizzate le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-104">The following interfaces are used with disk quotas.</span></span>



| <span data-ttu-id="f5d6e-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f5d6e-105">Interface</span></span>                                          | <span data-ttu-id="f5d6e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5d6e-106">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5d6e-107">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="f5d6e-107">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | <span data-ttu-id="f5d6e-108">Controlla le funzionalità di quota del disco di un singolo volume di file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-108">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="f5d6e-109">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="f5d6e-109">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | <span data-ttu-id="f5d6e-110">Riceve le notifiche degli eventi relative alla quota.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-110">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="f5d6e-111">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="f5d6e-111">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | <span data-ttu-id="f5d6e-112">Rappresenta una singola voce della quota utente nel file di informazioni sulla quota del volume.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-112">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="f5d6e-113">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="f5d6e-113">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | <span data-ttu-id="f5d6e-114">Aggiunge più oggetti utente della quota a un contenitore che viene quindi inviato per l'aggiornamento in una singola chiamata.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-114">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="f5d6e-115">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="f5d6e-115">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | <span data-ttu-id="f5d6e-116">Enumera le voci della quota utente nel volume.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-116">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

