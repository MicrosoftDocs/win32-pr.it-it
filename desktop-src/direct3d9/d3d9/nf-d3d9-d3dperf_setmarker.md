---
title: Funzione D3DPERF_SetMarker
description: Contrassegnare un evento istantaneo. PIX può utilizzare questo evento per attivare un'azione.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104398709"
---
# <a name="d3dperf_setmarker-function"></a>Funzione D3DPERF_SetMarker

Contrassegnare un evento istantaneo. PIX può utilizzare questo evento per attivare un'azione.

## <a name="syntax"></a>Sintassi

```cpp
void WINAPI D3DPERF_SetMarker(
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

Gli eventi utente istantanei non racchiudono né raggruppano altri eventi. Ad esempio, quando l'utente genera un'arma in un gioco, è possibile creare un evento *shot generato* da una chiamata **D3DPERF_SetMarker** . Per raggruppare più eventi con un unico nome definito dall'utente, usare **D3DPERF_BeginEvent** e **D3DPERF_EndEvent** invece di **D3DPERF_SetMarker**.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9. h |
| **Libreria** | d3d9. lib |
| **DLL** | d3d9.dll |