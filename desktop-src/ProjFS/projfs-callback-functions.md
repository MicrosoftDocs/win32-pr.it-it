---
title: Funzioni di callback ProjFS
description: Le funzioni di callback seguenti sono dichiarate in projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/22/2020
ms.locfileid: "103857941"
---
# <a name="callback-functions"></a><span data-ttu-id="c6885-103">Funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="c6885-103">Callback functions</span></span>

<span data-ttu-id="c6885-104">Le funzioni di callback seguenti sono dichiarate in projectedfslib. h.</span><span class="sxs-lookup"><span data-stu-id="c6885-104">The following callback functions are declared in projectedfslib.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6885-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c6885-105">In this section</span></span>

| <span data-ttu-id="c6885-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="c6885-106">Topic</span></span> | <span data-ttu-id="c6885-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6885-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="c6885-108">**PRJ_CANCEL_COMMAND_CB**</span><span class="sxs-lookup"><span data-stu-id="c6885-108">**PRJ_CANCEL_COMMAND_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | <span data-ttu-id="c6885-109">Notifica al provider che un'operazione eseguita da una chiamata precedente di un callback deve essere annullata.</span><span class="sxs-lookup"><span data-stu-id="c6885-109">Notifies the provider that an operation by an earlier invocation of a callback should be canceled.</span></span> |
| [<span data-ttu-id="c6885-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="c6885-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | <span data-ttu-id="c6885-111">Informa il provider che un'enumerazione di directory è finita.</span><span class="sxs-lookup"><span data-stu-id="c6885-111">Informs the provider that a directory enumeration is over.</span></span> |
| [<span data-ttu-id="c6885-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="c6885-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | <span data-ttu-id="c6885-113">Richiede le informazioni di enumerazione directory dal provider.</span><span class="sxs-lookup"><span data-stu-id="c6885-113">Requests directory enumeration information from the provider.</span></span>
| [<span data-ttu-id="c6885-114">**PRJ_GET_FILE_DATA_CB**</span><span class="sxs-lookup"><span data-stu-id="c6885-114">**PRJ_GET_FILE_DATA_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | <span data-ttu-id="c6885-115">Richiede il contenuto del flusso di dati primario di un file.</span><span class="sxs-lookup"><span data-stu-id="c6885-115">Requests the contents of a file's primary data stream.</span></span>
| [<span data-ttu-id="c6885-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span><span class="sxs-lookup"><span data-stu-id="c6885-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | <span data-ttu-id="c6885-117">Richiede le informazioni per un file o una directory dal provider.</span><span class="sxs-lookup"><span data-stu-id="c6885-117">Requests information for a file or directory from the provider.</span></span>
| [<span data-ttu-id="c6885-118">**PRJ_NOTIFICATION_CB**</span><span class="sxs-lookup"><span data-stu-id="c6885-118">**PRJ_NOTIFICATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | <span data-ttu-id="c6885-119">Recapita al provider le notifiche relative alle operazioni file system.</span><span class="sxs-lookup"><span data-stu-id="c6885-119">Delivers notifications to the provider about file system operations.</span></span>
| [<span data-ttu-id="c6885-120">**PRJ_QUERY_FILE_NAME_CB**</span><span class="sxs-lookup"><span data-stu-id="c6885-120">**PRJ_QUERY_FILE_NAME_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | <span data-ttu-id="c6885-121">Determina se un percorso di file specificato esiste nell'archivio di backup del provider.</span><span class="sxs-lookup"><span data-stu-id="c6885-121">Determines whether a given file path exists in the provider's backing store.</span></span>
| [<span data-ttu-id="c6885-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="c6885-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | <span data-ttu-id="c6885-123">Informa il provider che è in corso l'avvio di un'enumerazione di directory.</span><span class="sxs-lookup"><span data-stu-id="c6885-123">Informs the provider that a directory enumeration is starting.</span></span>