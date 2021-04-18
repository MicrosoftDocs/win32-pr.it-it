---
description: Descrive due tipi di limiti di quota del disco e il modo in cui vengono misurati i limiti delle quote del disco
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limiti della quota del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313889"
---
# <a name="disk-quota-limits"></a><span data-ttu-id="94394-103">Limiti della quota del disco</span><span class="sxs-lookup"><span data-stu-id="94394-103">Disk Quota Limits</span></span>

<span data-ttu-id="94394-104">Lo spazio su disco utilizzato da ogni file viene addebitato direttamente all'utente proprietario del file.</span><span class="sxs-lookup"><span data-stu-id="94394-104">The disk space that each file uses is charged directly to the user who owns the file.</span></span> <span data-ttu-id="94394-105">Il proprietario di un file è identificato dall'ID di sicurezza (SID) nelle informazioni di sicurezza per il file.</span><span class="sxs-lookup"><span data-stu-id="94394-105">The owner of a file is identified by the security identifier (SID) in the security information for the file.</span></span> <span data-ttu-id="94394-106">Lo spazio totale su disco addebitato a un utente è la somma della lunghezza di tutti i flussi di dati.</span><span class="sxs-lookup"><span data-stu-id="94394-106">The total disk space charged to a user is the sum of the length of all data streams.</span></span> <span data-ttu-id="94394-107">In altre parole, i flussi di set di proprietà e i flussi di dati utente residenti influiscono sulla quota dell'utente.</span><span class="sxs-lookup"><span data-stu-id="94394-107">In other words, property set streams and resident user data streams affect the user's quota.</span></span>

<span data-ttu-id="94394-108">Per la quota non vengono addebitati punti di analisi, descrittori di sicurezza o altri metadati associati ai file.</span><span class="sxs-lookup"><span data-stu-id="94394-108">Quota is not charged for re-parse points, security descriptors, or other metadata that is associated with the files.</span></span> <span data-ttu-id="94394-109">La compressione o la decompressione dei file non influisce sullo spazio su disco segnalato per i file.</span><span class="sxs-lookup"><span data-stu-id="94394-109">Compressing or decompressing files does not affect the disk space reported for the files.</span></span> <span data-ttu-id="94394-110">È pertanto possibile confrontare le impostazioni delle quote in un volume con le impostazioni di un altro volume.</span><span class="sxs-lookup"><span data-stu-id="94394-110">Therefore, quota settings on one volume can be compared to settings on another volume.</span></span>

<span data-ttu-id="94394-111">Esistono due tipi di limiti di quota del disco, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="94394-111">There are two types of disk quota limits, as shown in the following table.</span></span>



| <span data-ttu-id="94394-112">Limite</span><span class="sxs-lookup"><span data-stu-id="94394-112">Limit</span></span>                        | <span data-ttu-id="94394-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94394-113">Description</span></span>                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94394-114">Valore soglia avvisi</span><span class="sxs-lookup"><span data-stu-id="94394-114">Warning threshold</span></span><br/> | <span data-ttu-id="94394-115">È possibile configurare il sistema in modo da generare una voce di registro di sistema quando lo spazio su disco addebitato all'utente supera questo valore.</span><span class="sxs-lookup"><span data-stu-id="94394-115">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="94394-116">Quota rigida</span><span class="sxs-lookup"><span data-stu-id="94394-116">Hard quota</span></span><br/>        | <span data-ttu-id="94394-117">È possibile configurare il sistema in modo da generare una voce di registro di sistema quando lo spazio su disco addebitato all'utente supera questo valore.</span><span class="sxs-lookup"><span data-stu-id="94394-117">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span> <span data-ttu-id="94394-118">È inoltre possibile configurare il sistema in modo da negare ulteriore spazio su disco all'utente quando lo spazio su disco addebitato all'utente supera questo valore.</span><span class="sxs-lookup"><span data-stu-id="94394-118">You can also configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.</span></span><br/> |



 

<span data-ttu-id="94394-119">Il file system NTFS crea automaticamente una voce di quota utente quando un utente scrive per la prima volta nel volume.</span><span class="sxs-lookup"><span data-stu-id="94394-119">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="94394-120">Alle voci create automaticamente vengono assegnati la soglia di avviso predefinita e i valori di limite della quota hardware per il volume.</span><span class="sxs-lookup"><span data-stu-id="94394-120">Entries that are created automatically are assigned the default warning threshold and hard quota limit values for the volume.</span></span>

 

 




