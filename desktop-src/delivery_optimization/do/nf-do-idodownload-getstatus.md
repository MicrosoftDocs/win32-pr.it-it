---
title: Metodo IDODownload::GetStatus
description: Recupera un puntatore a una **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download.
keywords:
- Metodo IDODownload::GetStatus
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e3a5aec5e35187a51865e074dae26ff012b75dfa3a41ffd13a8bed7371515fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047109"
---
# <a name="idodownloadgetstatus-method"></a>Metodo IDODownload::GetStatus

Recupera un puntatore a una **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parametri

`status`

Puntatore a una **DO_DOWNLOAD_STATUS** struttura .

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | Do.h |
