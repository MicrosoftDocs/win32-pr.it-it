---
description: Codici e strutture di controllo da utilizzare con il Journal delle modifiche del numero di sequenza di aggiornamento (USN) file system NTFS.
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: Operazioni Journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52cda51d0efc4cbae1333fc197f42d6a5cc0f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317807"
---
# <a name="change-journal-operations"></a><span data-ttu-id="0702f-103">Operazioni Journal delle modifiche</span><span class="sxs-lookup"><span data-stu-id="0702f-103">Change Journal Operations</span></span>

<span data-ttu-id="0702f-104">L'elenco seguente identifica i codici di controllo che funzionano con il Journal delle modifiche del numero di sequenza di aggiornamento (USN) NTFS file system.</span><span class="sxs-lookup"><span data-stu-id="0702f-104">The following list identifies the control codes that work with the NTFS file system update sequence number (USN) change journal.</span></span>

-   [<span data-ttu-id="0702f-105">**FSCTL \_ creare \_ \_ journal USN**</span><span class="sxs-lookup"><span data-stu-id="0702f-105">**FSCTL\_CREATE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [<span data-ttu-id="0702f-106">**FSCTL \_ eliminare \_ \_ journal USN**</span><span class="sxs-lookup"><span data-stu-id="0702f-106">**FSCTL\_DELETE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [<span data-ttu-id="0702f-107">**\_ \_ dati USN dell'enumerazione FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="0702f-107">**FSCTL\_ENUM\_USN\_DATA**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [<span data-ttu-id="0702f-108">**\_handle del contrassegno FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="0702f-108">**FSCTL\_MARK\_HANDLE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [<span data-ttu-id="0702f-109">**\_ \_ journal USN query \_ FSCTL**</span><span class="sxs-lookup"><span data-stu-id="0702f-109">**FSCTL\_QUERY\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [<span data-ttu-id="0702f-110">**\_ \_ journal USN Read \_ FSCTL**</span><span class="sxs-lookup"><span data-stu-id="0702f-110">**FSCTL\_READ\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

<span data-ttu-id="0702f-111">Nell'elenco riportato di seguito vengono identificate le informazioni sulle strutture correlate al Journal delle modifiche del file system USN NTFS.</span><span class="sxs-lookup"><span data-stu-id="0702f-111">The following list identifies the structures information that relates to the NTFS file system USN change journal.</span></span>

-   [<span data-ttu-id="0702f-112">**CREAZIONE \_ di \_ dati del journal USN \_**</span><span class="sxs-lookup"><span data-stu-id="0702f-112">**CREATE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [<span data-ttu-id="0702f-113">**Elimina \_ \_ dati journal \_ USN**</span><span class="sxs-lookup"><span data-stu-id="0702f-113">**DELETE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [<span data-ttu-id="0702f-114">**CONTRASSEGNA \_ le \_ informazioni sull'handle**</span><span class="sxs-lookup"><span data-stu-id="0702f-114">**MARK\_HANDLE\_INFO**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [<span data-ttu-id="0702f-115">**\_dati enum \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="0702f-115">**MFT\_ENUM\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [<span data-ttu-id="0702f-116">**LEGGERE \_ \_ i dati del journal USN \_**</span><span class="sxs-lookup"><span data-stu-id="0702f-116">**READ\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [<span data-ttu-id="0702f-117">**\_dati journal \_ USN**</span><span class="sxs-lookup"><span data-stu-id="0702f-117">**USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [<span data-ttu-id="0702f-118">**\_record USN**</span><span class="sxs-lookup"><span data-stu-id="0702f-118">**USN\_RECORD**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
