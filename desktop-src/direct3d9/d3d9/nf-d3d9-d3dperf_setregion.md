---
title: Funzione D3DPERF_SetRegion
description: Contrassegna una serie di frame con il colore e il nome specificati nel file PIXRun. Questa funzione non è attualmente supportata da PIX.
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
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "106299487"
---
# <a name="d3dperf_setregion-function"></a>Funzione D3DPERF_SetRegion

Contrassegna una serie di frame con il colore e il nome specificati nel file PIXRun. Questa funzione non è attualmente supportata da PIX.

## <a name="syntax"></a>Sintassi

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Parametri

`col`

Colore dell'evento. Si tratta del colore per visualizzare l'evento nella visualizzazione evento.

`wszName`

Nome evento.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Per semplificare l'analisi, il programma di destinazione può utilizzare il colore per contrassegnare ogni livello di un programma di destinazione.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9. h |
| **Libreria** | d3d9. lib |
| **DLL** | d3d9.dll |