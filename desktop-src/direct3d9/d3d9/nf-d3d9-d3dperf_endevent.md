---
title: D3DPERF_EndEvent funzione
description: Contrassegna la fine di un evento definito dall'utente. PIX può usare questo evento per attivare un'azione.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: bd12780dfdfcb86e83495ae877d8debf1e768517826329ccee8d40ffaa88fbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989251"
---
# <a name="d3dperf_endevent-function"></a>D3DPERF_EndEvent funzione

Contrassegna la fine di un evento definito dall'utente. PIX può usare questo evento per attivare un'azione.

## <a name="syntax"></a>Sintassi

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Valore restituito

Livello della gerarchia in cui termina l'evento. Se si verifica un errore, questo valore è negativo.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9.h |
| **Libreria** | d3d9.lib |
| **DLL** | d3d9.dll |