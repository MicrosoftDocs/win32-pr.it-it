---
title: D3DPERF_SetRegion funzione
description: Contrassegnare una serie di fotogrammi con il colore e il nome specificati nel file PIXRun. Questa funzione non è attualmente supportata da PIX.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 05884fe8a3b104588a941dcaf3089a1c0f6f8eab4f4a01e143470f73454ad4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989261"
---
# <a name="d3dperf_setregion-function"></a>D3DPERF_SetRegion funzione

Contrassegnare una serie di fotogrammi con il colore e il nome specificati nel file PIXRun. Questa funzione non è attualmente supportata da PIX.

## <a name="syntax"></a>Sintassi

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Parametri

`col`

Colore dell'evento. Si tratta del colore per visualizzare l'evento nella visualizzazione eventi.

`wszName`

Nome evento.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Per semplificare l'analisi, il programma di destinazione può usare il colore per contrassegnare ogni livello di un programma di destinazione.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9.h |
| **Libreria** | d3d9.lib |
| **DLL** | d3d9.dll |