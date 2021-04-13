---
title: Funzione D3DPERF_EndEvent
description: Contrassegna la fine di un evento definito dall'utente. PIX può utilizzare questo evento per attivare un'azione.
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
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104398710"
---
# <a name="d3dperf_endevent-function"></a>Funzione D3DPERF_EndEvent

Contrassegna la fine di un evento definito dall'utente. PIX può utilizzare questo evento per attivare un'azione.

## <a name="syntax"></a>Sintassi

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Valore restituito

Livello della gerarchia in cui l'evento sta per scadere. Se si verifica un errore, questo valore è negativo.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9. h |
| **Libreria** | d3d9. lib |
| **DLL** | d3d9.dll |