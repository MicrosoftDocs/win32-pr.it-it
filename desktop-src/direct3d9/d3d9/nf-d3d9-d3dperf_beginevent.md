---
title: Funzione D3DPERF_BeginEvent
description: Contrassegna l'inizio di un evento definito dall'utente. PIX può utilizzare questo evento per attivare un'azione.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104398708"
---
# <a name="d3dperf_beginevent-function"></a>Funzione D3DPERF_BeginEvent

Contrassegna l'inizio di un evento definito dall'utente. PIX può utilizzare questo evento per attivare un'azione.

## <a name="syntax"></a>Sintassi

```cpp
int WINAPI D3DPERF_BeginEvent(
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

Il livello in base zero della gerarchia da cui viene avviato l'evento. Se si verifica un errore, il valore restituito sarà negativo.

## <a name="remarks"></a>Commenti

Gli eventi definiti dall'utente raggruppano altri eventi in modo significativo per il programma di destinazione in modo che possano essere rappresentati meglio negli strumenti di profilatura delle prestazioni. Ad esempio, un evento di *spazio di disegno* può racchiudere un numero di chiamate Direct3D che gestiscono il disegno di una spaziatura in un gioco. Gli eventi possono essere annidati.

Ogni chiamata di **D3DPERF_BeginEvent** deve avere una chiamata **D3DPERF_EndEvent** corrispondente. Gli eventi istantanei, che non sono racchiusi tra altri eventi, devono essere etichettati usando **D3DPERF_SetMarker** anziché **D3DPERF_BeginEvent** e **D3DPERF_EndEvent**.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9. h |
| **Libreria** | d3d9. lib |
| **DLL** | d3d9.dll |