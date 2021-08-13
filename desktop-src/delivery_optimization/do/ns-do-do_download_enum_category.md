---
title: DO_DOWNLOAD_ENUM_CATEGORY struttura
description: Usato da **IDOManager::EnumDownloads** per filtrare l'enumerazione dei download in base al valore della proprietà specifica.
keywords:
- DO_DOWNLOAD_ENUM_CATEGORY struttura
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
ms.openlocfilehash: 32bdc7ca9a84bfe87ff453d34c4ecff57a8dabf5f67b21cc0d54ba079efd1578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543760"
---
# <a name="do_download_enum_category-structure"></a>DO_DOWNLOAD_ENUM_CATEGORY struttura

La **DO_DOWNLOAD_ENUM_CATEGORY** viene usata da **IDOManager::EnumDownloads** per filtrare l'enumerazione dei download in base al valore della proprietà specifica.

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
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | Do.h |
