---
title: 'Metodo IDODownload:: GetStatus'
description: Recupera un puntatore a una struttura **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download.
keywords:
- 'Metodo IDODownload:: GetStatus'
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
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398356"
---
# <a name="idodownloadgetstatus-method"></a>Metodo IDODownload:: GetStatus

Recupera un puntatore a una struttura **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parametri

`status`

Puntatore a una struttura **DO_DOWNLOAD_STATUS** .

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |
