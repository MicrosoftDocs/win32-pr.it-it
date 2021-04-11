---
description: Interfacce utilizzate in Gestione disco.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfacce di gestione disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233160"
---
# <a name="disk-management-interfaces"></a><span data-ttu-id="388fb-103">Interfacce di gestione disco</span><span class="sxs-lookup"><span data-stu-id="388fb-103">Disk Management Interfaces</span></span>

<span data-ttu-id="388fb-104">Le interfacce seguenti vengono utilizzate in Gestione disco.</span><span class="sxs-lookup"><span data-stu-id="388fb-104">The following interfaces are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="388fb-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="388fb-105">In this section</span></span>



| <span data-ttu-id="388fb-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="388fb-106">Interface</span></span>                                                     | <span data-ttu-id="388fb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="388fb-107">Description</span></span>                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="388fb-108">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="388fb-108">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | <span data-ttu-id="388fb-109">Controlla le funzionalità di quota del disco di un singolo volume di file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="388fb-109">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="388fb-110">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="388fb-110">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | <span data-ttu-id="388fb-111">Riceve le notifiche degli eventi relative alla quota.</span><span class="sxs-lookup"><span data-stu-id="388fb-111">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="388fb-112">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="388fb-112">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | <span data-ttu-id="388fb-113">Rappresenta una singola voce della quota utente nel file di informazioni sulla quota del volume.</span><span class="sxs-lookup"><span data-stu-id="388fb-113">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="388fb-114">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="388fb-114">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | <span data-ttu-id="388fb-115">Aggiunge più oggetti utente della quota a un contenitore che viene quindi inviato per l'aggiornamento in una singola chiamata.</span><span class="sxs-lookup"><span data-stu-id="388fb-115">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="388fb-116">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="388fb-116">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | <span data-ttu-id="388fb-117">Enumera le voci della quota utente nel volume.</span><span class="sxs-lookup"><span data-stu-id="388fb-117">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

