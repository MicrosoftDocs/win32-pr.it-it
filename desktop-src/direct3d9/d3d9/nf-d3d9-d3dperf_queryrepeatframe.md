---
title: D3DPERF_QueryRepeatFrame funzione
description: Determinare se un profiler delle prestazioni richiede il nuovo invio del frame corrente a Direct3D per l'analisi delle prestazioni. Questa funzione non è attualmente supportata da PIX.
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
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: dbc46ff05b6fa1846bb0e1ffc1fca928ca1d68ee38a43708c77a109b61a405da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751241"
---
# <a name="d3dperf_queryrepeatframe-function"></a>D3DPERF_QueryRepeatFrame funzione

Determinare se un profiler delle prestazioni richiede il nuovo invio del frame corrente a Direct3D per l'analisi delle prestazioni. Questa funzione non è attualmente supportata da PIX.

## <a name="syntax"></a>Sintassi

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Valore restituito

Se il valore restituito è TRUE, il chiamante deve ripetere la stessa sequenza di chiamate. Se FALSE, il chiamante deve continuare.

## <a name="remarks"></a>Commenti

La funzione deve essere chiamata immediatamente dopo **la chiamata di IDirect3DDevice9::P resent.**

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9.h |
| **Libreria** | d3d9.lib |
| **DLL** | d3d9.dll |