---
description: Gli amministratori possono controllare la quantità di dati che ciascun utente può archiviare in un volume file system NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Gestione delle quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317771"
---
# <a name="managing-disk-quotas"></a><span data-ttu-id="86d62-103">Gestione delle quote disco</span><span class="sxs-lookup"><span data-stu-id="86d62-103">Managing Disk Quotas</span></span>

<span data-ttu-id="86d62-104">Il file system NTFS supporta le *quote disco* che consentono agli amministratori di controllare la quantità di dati che ciascun utente può archiviare in un volume file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="86d62-104">The NTFS file system supports *disk quotas*, which allow administrators to control the amount of data that each user can store on an NTFS file system volume.</span></span> <span data-ttu-id="86d62-105">Gli amministratori possono facoltativamente configurare il sistema per la registrazione di un evento quando gli utenti sono vicini alla propria quota e per negare ulteriore spazio su disco agli utenti che superano la quota.</span><span class="sxs-lookup"><span data-stu-id="86d62-105">Administrators can optionally configure the system to log an event when users are near their quota, and to deny further disk space to users who exceed their quota.</span></span> <span data-ttu-id="86d62-106">Gli amministratori possono inoltre generare report e utilizzare Monitoraggio eventi per tenere traccia dei problemi di quota.</span><span class="sxs-lookup"><span data-stu-id="86d62-106">Administrators can also generate reports, and use the event monitor to track quota issues.</span></span>

<span data-ttu-id="86d62-107">È possibile determinare se un file system supporta le quote disco chiamando la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminando il flag di bit **\_ \_ quote volume file** .</span><span class="sxs-lookup"><span data-stu-id="86d62-107">You can determine whether a file system supports disk quotas by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_VOLUME\_QUOTAS** bit flag.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="86d62-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="86d62-108">In this section</span></span>



| <span data-ttu-id="86d62-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="86d62-109">Topic</span></span>                                                                                                   | <span data-ttu-id="86d62-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86d62-110">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86d62-111">Amministrazione a livello di utente di quote disco</span><span class="sxs-lookup"><span data-stu-id="86d62-111">User-level Administration of Disk Quotas</span></span>](user-level-administration-of-disk-quotas.md)<br/>     | <span data-ttu-id="86d62-112">Come ottenere maggiore spazio libero su disco dopo il superamento della quota di quote.</span><span class="sxs-lookup"><span data-stu-id="86d62-112">How to get more free disk space after exceeding the quota allowance.</span></span><br/>                                                                  |
| [<span data-ttu-id="86d62-113">Amministrazione a livello di sistema di quote disco</span><span class="sxs-lookup"><span data-stu-id="86d62-113">System-level Administration of Disk Quotas</span></span>](system-level-administration-of-disk-quotas.md)<br/> | <span data-ttu-id="86d62-114">L'amministratore di sistema può impostare le quote per utenti specifici in un volume.</span><span class="sxs-lookup"><span data-stu-id="86d62-114">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="86d62-115">L'amministratore può inoltre impostare le quote predefinite per il volume.</span><span class="sxs-lookup"><span data-stu-id="86d62-115">The administrator can also set default quotas for the volume.</span></span><br/> |
| [<span data-ttu-id="86d62-116">Limiti della quota del disco</span><span class="sxs-lookup"><span data-stu-id="86d62-116">Disk Quota Limits</span></span>](disk-quota-limits.md)<br/>                                                   | <span data-ttu-id="86d62-117">Descrive due tipi di limiti di quota del disco e il modo in cui vengono misurati i limiti delle quote del disco</span><span class="sxs-lookup"><span data-stu-id="86d62-117">Describes two types of disk quota limits and how disk quota limits are measured.</span></span><br/>                                                      |
| [<span data-ttu-id="86d62-118">Interfacce di quota disco</span><span class="sxs-lookup"><span data-stu-id="86d62-118">Disk Quota Interfaces</span></span>](disk-quota-interfaces.md)<br/>                                           | <span data-ttu-id="86d62-119">Interfacce utilizzate con le quote disco.</span><span class="sxs-lookup"><span data-stu-id="86d62-119">Interfaces used with disk quotas.</span></span><br/>                                                                                                     |



 

 

 




