---
title: Struttura DO_DOWNLOAD_RANGE_INFO
description: Identifica una matrice di intervalli di byte da scaricare da un file.
keywords:
- Struttura DO_DOWNLOAD_RANGE_INFO
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
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398352"
---
# <a name="do_download_range_info-structure"></a>Struttura DO_DOWNLOAD_RANGE_INFO

La struttura **DO_DOWNLOAD_RANGE_INFO** identifica una matrice di intervalli di byte da scaricare da un file. Viene in genere passato come argomento facoltativo alla funzione **IDODownload:: Start** .

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

Numero di elementi negli intervalli.

`Ranges`

Matrice di una o più strutture di **DO_DOWNLOAD_RANGE** che specificano gli intervalli da scaricare.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |
