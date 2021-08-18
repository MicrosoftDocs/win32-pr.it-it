---
title: D3DPERF_SetOptions funzione
description: Impostare le opzioni del profiler specificate dal programma di destinazione.
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
ms.openlocfilehash: 579c07d8f93696e4e3c83b1e61c1ff5fca65e12b5a7cf0a5937a254ecc6dc306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805736"
---
# <a name="d3dperf_setoptions-function"></a>D3DPERF_SetOptions funzione

Impostare le opzioni del profiler specificate dal programma di destinazione.

## <a name="syntax"></a>Sintassi

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Parametri

`dwOptions`

Opzioni utente riconoscibili da PIX. Impostare questo valore su 1 per notificare a PIX che il programma di destinazione non fornisce l'autorizzazione per la profilata.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9.h |
| **Libreria** | d3d9.lib |
| **DLL** | d3d9.dll |