---
title: DO_DOWNLOAD_RANGE_INFO struttura
description: Identifica una matrice di intervalli di byte da scaricare da un file.
keywords:
- DO_DOWNLOAD_RANGE_INFO struttura
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 30df22c7232ad1d28315e8152396ddd92bdab9a7cbf67d748af134c0f0760c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543745"
---
# <a name="do_download_range_info-structure"></a>DO_DOWNLOAD_RANGE_INFO struttura

La **DO_DOWNLOAD_RANGE_INFO** identifica una matrice di intervalli di byte da scaricare da un file. Viene in genere passato come argomento facoltativo alla **funzione IDODownload::Start.**

## <a name="syntax"></a>Sintassi
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a>Members

`RangeCount`

Numero di elementi in Ranges.

`Ranges`

Matrice di una o più **DO_DOWNLOAD_RANGE** che specificano gli intervalli da scaricare.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | Do.h |
