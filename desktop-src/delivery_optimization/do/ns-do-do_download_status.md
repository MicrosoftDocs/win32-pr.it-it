---
title: Struttura DO_DOWNLOAD_STATUS
description: Utilizzato per ottenere lo stato di un download specifico.
keywords:
- Struttura DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299299"
---
# <a name="do_download_status-structure"></a><span data-ttu-id="ed67c-104">Struttura DO_DOWNLOAD_STATUS</span><span class="sxs-lookup"><span data-stu-id="ed67c-104">DO_DOWNLOAD_STATUS structure</span></span>

<span data-ttu-id="ed67c-105">La struttura **DO_DOWNLOAD_STATUS** viene utilizzata per ottenere lo stato di un download specifico.</span><span class="sxs-lookup"><span data-stu-id="ed67c-105">The **DO_DOWNLOAD_STATUS** structure is used to obtain the status of a specific download.</span></span> <span data-ttu-id="ed67c-106">Viene ottenuto chiamando la funzione **IDODownload:: GetStatus** .</span><span class="sxs-lookup"><span data-stu-id="ed67c-106">It is obtained by calling the **IDODownload::GetStatus** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed67c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed67c-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a><span data-ttu-id="ed67c-108">Members</span><span class="sxs-lookup"><span data-stu-id="ed67c-108">Members</span></span>

`BytesTotal`

<span data-ttu-id="ed67c-109">Numero totale di byte da scaricare.</span><span class="sxs-lookup"><span data-stu-id="ed67c-109">The total number of bytes to download.</span></span>

`BytesTransferred`

<span data-ttu-id="ed67c-110">Numero di byte già scaricati.</span><span class="sxs-lookup"><span data-stu-id="ed67c-110">The number of bytes that have already been downloaded.</span></span>

`State`

<span data-ttu-id="ed67c-111">Stato di download corrente in base a quanto definito dall'enumerazione **DODownloadState** .</span><span class="sxs-lookup"><span data-stu-id="ed67c-111">The current download state as defined by the **DODownloadState** enumeration.</span></span>

`Error`

<span data-ttu-id="ed67c-112">Informazioni sull'errore, se esistenti, associate al download corrente.</span><span class="sxs-lookup"><span data-stu-id="ed67c-112">The error information (if it exists) that is associated with the current download.</span></span>

`ExtendedError`

<span data-ttu-id="ed67c-113">Informazioni estese sull'errore, se esistenti, associate al download corrente.</span><span class="sxs-lookup"><span data-stu-id="ed67c-113">The extended error information (if it exists) that is associated with the current download.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed67c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed67c-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ed67c-115">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="ed67c-115">**Minimum supported client**</span></span> | <span data-ttu-id="ed67c-116">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed67c-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="ed67c-117">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="ed67c-117">**Minimum supported server**</span></span> | <span data-ttu-id="ed67c-118">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="ed67c-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="ed67c-119">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="ed67c-119">**Header**</span></span> | <span data-ttu-id="ed67c-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="ed67c-120">Do.h</span></span> |
