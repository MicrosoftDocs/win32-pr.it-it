---
title: 'Metodo IDODownload:: Start'
description: Avvia o riprende un download.
keywords:
- 'Metodo IDODownload:: Start'
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
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321124"
---
# <a name="idodownloadstart-method"></a>Metodo IDODownload:: Start

Avvia o riprende un download, passando intervalli facoltativi come puntatore alla struttura [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) .

## <a name="syntax"></a>Sintassi

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Parametri

`ranges`

Facoltativo. Puntatore a una struttura di [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (per scaricare solo intervalli specifici del file). Passare `nullptr` per scaricare l'intero file.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |
