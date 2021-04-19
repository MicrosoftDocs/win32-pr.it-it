---
description: Le funzioni seguenti vengono utilizzate con la registrazione degli eventi.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funzioni di registrazione eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310820"
---
# <a name="event-logging-functions"></a><span data-ttu-id="cfc2a-103">Funzioni di registrazione eventi</span><span class="sxs-lookup"><span data-stu-id="cfc2a-103">Event Logging Functions</span></span>

<span data-ttu-id="cfc2a-104">Le funzioni seguenti vengono utilizzate con la registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-104">The following functions are used with event logging.</span></span>



| <span data-ttu-id="cfc2a-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="cfc2a-105">Function</span></span>                                                         | <span data-ttu-id="cfc2a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfc2a-106">Description</span></span>                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfc2a-107">**BackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-107">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | <span data-ttu-id="cfc2a-108">Salva il registro eventi specificato in un file di backup.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-108">Saves the specified event log to a backup file.</span></span>                                                     |
| [<span data-ttu-id="cfc2a-109">**ClearEventLog**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-109">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | <span data-ttu-id="cfc2a-110">Cancella il registro eventi specificato e, facoltativamente, salva la copia corrente del log in un file di backup.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-110">Clears the specified event log, and optionally saves the current copy of the log to a backup file.</span></span>  |
| [<span data-ttu-id="cfc2a-111">**CloseEventLog**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-111">**CloseEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | <span data-ttu-id="cfc2a-112">Chiude un handle di lettura al log eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-112">Closes a read handle to the specified event log.</span></span>                                                    |
| [<span data-ttu-id="cfc2a-113">**DeregisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-113">**DeregisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | <span data-ttu-id="cfc2a-114">Chiude un handle di scrittura nel log eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-114">Closes a write handle to the specified event log.</span></span>                                                   |
| [<span data-ttu-id="cfc2a-115">**GetEventLogInformation**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-115">**GetEventLogInformation**</span></span>](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | <span data-ttu-id="cfc2a-116">Recupera le informazioni sul log eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-116">Retrieves information about the specified event log.</span></span>                                                |
| [<span data-ttu-id="cfc2a-117">**GetNumberOfEventLogRecords**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-117">**GetNumberOfEventLogRecords**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | <span data-ttu-id="cfc2a-118">Recupera il numero di record nel registro eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-118">Retrieves the number of records in the specified event log.</span></span>                                         |
| [<span data-ttu-id="cfc2a-119">**GetOldestEventLogRecord**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-119">**GetOldestEventLogRecord**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | <span data-ttu-id="cfc2a-120">Recupera il numero di record assoluto del record meno recente nel registro eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-120">Retrieves the absolute record number of the oldest record in the specified event log.</span></span>               |
| [<span data-ttu-id="cfc2a-121">**NotifyChangeEventLog**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-121">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | <span data-ttu-id="cfc2a-122">Consente a un'applicazione di ricevere una notifica quando un evento viene scritto nel registro eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-122">Enables an application to receive notification when an event is written to the specified event log.</span></span> |
| [<span data-ttu-id="cfc2a-123">**OpenBackupEventLog**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-123">**OpenBackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | <span data-ttu-id="cfc2a-124">Apre un handle per un log eventi di backup.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-124">Opens a handle to a backup event log.</span></span>                                                               |
| [<span data-ttu-id="cfc2a-125">**OpenEventLog**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-125">**OpenEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | <span data-ttu-id="cfc2a-126">Apre un handle per il registro eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-126">Opens a handle to the specified event log.</span></span>                                                          |
| [<span data-ttu-id="cfc2a-127">**ReadEventLog**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-127">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | <span data-ttu-id="cfc2a-128">Legge un numero intero di voci dal log eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-128">Reads a whole number of entries from the specified event log.</span></span>                                       |
| [<span data-ttu-id="cfc2a-129">**RegisterEventSource**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-129">**RegisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | <span data-ttu-id="cfc2a-130">Recupera un handle registrato nel registro eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-130">Retrieves a registered handle to the specified event log.</span></span>                                           |
| [<span data-ttu-id="cfc2a-131">**ReportEvent**</span><span class="sxs-lookup"><span data-stu-id="cfc2a-131">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | <span data-ttu-id="cfc2a-132">Scrive una voce alla fine del log eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc2a-132">Writes an entry at the end of the specified event log.</span></span>                                              |



 

 

 



