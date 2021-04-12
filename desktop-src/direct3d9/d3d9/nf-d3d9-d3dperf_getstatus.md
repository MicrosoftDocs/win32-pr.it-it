---
title: Funzione D3DPERF_GetStatus
description: Determinare lo stato corrente del Profiler dal programma di destinazione.
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
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104336585"
---
# <a name="d3dperf_getstatus-function"></a>Funzione D3DPERF_GetStatus

Determinare lo stato corrente del Profiler dal programma di destinazione.

## <a name="syntax"></a>Sintassi

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Valore restituito

Valore diverso da zero quando PIX sta profilando il programma di destinazione; in caso contrario, zero.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9. h |
| **Libreria** | d3d9. lib |
| **DLL** | d3d9.dll |