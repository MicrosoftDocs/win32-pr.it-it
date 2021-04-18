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
# <a name="do_download_enum_category-structure"></a>Struttura DO_DOWNLOAD_ENUM_CATEGORY

La struttura **DO_DOWNLOAD_ENUM_CATEGORY** viene utilizzata da **IDOManager:: EnumDownloads** per filtrare l'enumerazione downloads in base al valore della proprietà specifica.

## <a name="syntax"></a>Sintassi
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a>Members

`Property`

Nome della proprietà da utilizzare per l'enumerazione di download. Queste proprietà sono supportate a scopo di enumerazione.
- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`Value`

Valore della proprietà.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |
