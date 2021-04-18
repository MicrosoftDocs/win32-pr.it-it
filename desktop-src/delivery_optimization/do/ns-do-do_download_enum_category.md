---
title: Struttura DO_DOWNLOAD_ENUM_CATEGORY
description: "Usato da **IDOManager:: EnumDownloads** per filtrare l'enumerazione downloads in base al valore della proprietà specifica."
keywords:
- Struttura DO_DOWNLOAD_ENUM_CATEGORY
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299301"
---
# <a name="do_download_enum_category-structure"></a><span data-ttu-id="0c519-104">Struttura DO_DOWNLOAD_ENUM_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="0c519-104">DO_DOWNLOAD_ENUM_CATEGORY structure</span></span>

<span data-ttu-id="0c519-105">La struttura **DO_DOWNLOAD_ENUM_CATEGORY** viene utilizzata da **IDOManager:: EnumDownloads** per filtrare l'enumerazione downloads in base al valore della proprietà specifica.</span><span class="sxs-lookup"><span data-stu-id="0c519-105">The **DO_DOWNLOAD_ENUM_CATEGORY** structure is used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c519-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c519-106">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a><span data-ttu-id="0c519-107">Members</span><span class="sxs-lookup"><span data-stu-id="0c519-107">Members</span></span>

`Property`

<span data-ttu-id="0c519-108">Nome della proprietà da utilizzare per l'enumerazione di download.</span><span class="sxs-lookup"><span data-stu-id="0c519-108">The property name to be used for the download enumeration.</span></span> <span data-ttu-id="0c519-109">Queste proprietà sono supportate a scopo di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0c519-109">These properties are supported for enumeration purposes.</span></span>
- <span data-ttu-id="0c519-110">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="0c519-110">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="0c519-111">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="0c519-111">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="0c519-112">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="0c519-112">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="0c519-113">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0c519-113">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="0c519-114">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="0c519-114">**DODownloadProperty_LocalPath**</span></span>

`Value`

<span data-ttu-id="0c519-115">Valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c519-115">The property's value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c519-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c519-116">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0c519-117">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="0c519-117">**Minimum supported client**</span></span> | <span data-ttu-id="0c519-118">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c519-118">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="0c519-119">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="0c519-119">**Minimum supported server**</span></span> | <span data-ttu-id="0c519-120">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="0c519-120">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="0c519-121">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="0c519-121">**Header**</span></span> | <span data-ttu-id="0c519-122">Do. h</span><span class="sxs-lookup"><span data-stu-id="0c519-122">Do.h</span></span> |
