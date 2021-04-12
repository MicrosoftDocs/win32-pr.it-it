---
title: Funzione D3DPERF_SetOptions
description: Imposta le opzioni del profiler specificate dal programma di destinazione.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104472334"
---
# <a name="d3dperf_setoptions-function"></a>Funzione D3DPERF_SetOptions

Imposta le opzioni del profiler specificate dal programma di destinazione.

## <a name="syntax"></a>Sintassi

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Parametri

`dwOptions`

Opzioni utente riconoscibili da PIX. Impostare questa impostazione su 1 per notificare a PIX che il programma di destinazione non concede l'autorizzazione per la profilatura.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9. h |
| **Libreria** | d3d9. lib |
| **DLL** | d3d9.dll |