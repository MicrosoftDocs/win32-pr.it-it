---
title: Metodo IDODownload::Start
description: Avvia o riprende un download.
keywords:
- Metodo IDODownload::Start
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b2a06de8319ac07983fd13cb8523fa1dcf92365ca9275da80b699b290a4a6435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736258"
---
# <a name="idodownloadstart-method"></a>Metodo IDODownload::Start

Avvia o riprende un download, passando gli intervalli facoltativi come puntatore [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) struttura .

## <a name="syntax"></a>Sintassi

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Parametri

`ranges`

Facoltativo. Puntatore a una [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) struttura (per scaricare solo intervalli specifici del file). Passare `nullptr` per scaricare l'intero file.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | Do.h |
