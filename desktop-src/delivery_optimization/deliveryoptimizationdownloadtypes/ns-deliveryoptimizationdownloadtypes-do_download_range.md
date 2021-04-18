---
title: Struttura DO_DOWNLOAD_RANGE
description: Identifica un singolo intervallo di byte da scaricare da un file.
keywords:
- Struttura DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299309"
---
# <a name="do_download_range-structure"></a>Struttura DO_DOWNLOAD_RANGE

La struttura **DO_DOWNLOAD_RANGE** identifica un singolo intervallo di byte da scaricare da un file. La struttura **DO_DOWNLOAD_RANGE** è inclusa nella struttura **DO_DOWNLOAD_RANGES_INFO** per fornire una matrice di intervalli da scaricare.

## <a name="syntax"></a>Sintassi
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a>Members

`Offset`

Offset in base zero all'inizio dell'intervallo di byte da scaricare da un file.

`Length`

Lunghezza dell'intervallo, in byte. Non specificare una lunghezza pari a zero byte. Per indicare che l'intervallo si estende fino alla fine del file, specificare **DO_LENGTH_TO_EOF**.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | DeliveryOptimizationDownloadTypes. h |
