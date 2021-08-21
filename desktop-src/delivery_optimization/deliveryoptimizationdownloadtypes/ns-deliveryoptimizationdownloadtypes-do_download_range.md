---
title: DO_DOWNLOAD_RANGE struttura
description: Identifica un singolo intervallo di byte da scaricare da un file.
keywords:
- DO_DOWNLOAD_RANGE struttura
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
ms.openlocfilehash: 39672bff2e3a7194f7d674b2184d5de8c9c3c601e4a7777ef31ace80f5f9f327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047119"
---
# <a name="do_download_range-structure"></a>DO_DOWNLOAD_RANGE struttura

La **DO_DOWNLOAD_RANGE** struttura identifica un singolo intervallo di byte da scaricare da un file. La **DO_DOWNLOAD_RANGE** struttura è inclusa nella **DO_DOWNLOAD_RANGES_INFO** per fornire una matrice di intervalli da scaricare.

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

Lunghezza dell'intervallo, in byte. Non specificare una lunghezza pari a zero byte. Per indicare che l'intervallo si estende fino alla fine del file, **specificare** DO_LENGTH_TO_EOF .

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | DeliveryOptimizationDownloadTypes.h |
