---
title: D3DPERF_GetStatus funzione
description: Determinare lo stato corrente del profiler dal programma di destinazione.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 78ff9eda9ab224faf4b2a117f6230e3361664bbfea35d8b2a8484ba7f5ab764a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805746"
---
# <a name="d3dperf_getstatus-function"></a>D3DPERF_GetStatus funzione

Determinare lo stato corrente del profiler dal programma di destinazione.

## <a name="syntax"></a>Sintassi

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Valore restituito

Valore diverso da zero quando PIX esegue la profilatura del programma di destinazione. in caso contrario, zero.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9.h |
| **Libreria** | d3d9.lib |
| **DLL** | d3d9.dll |