---
title: Metodo IDODownloadStatusCallback::OnStatusChange
description: DO chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato di download.
keywords:
- Metodo IDODownloadStatusCallback::OnStatusChange
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0395b6bc64ad3abe102a0a4f0dc7afd8e8d59f336949a3b97eaf683a4f4900cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736218"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>Metodo IDODownloadStatusCallback::OnStatusChange

DO chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato di download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parametri

`download`

Puntatore **all'interfaccia IDODownload** il cui stato è cambiato.

`status`

Puntatore a una **DO_DOWNLOAD_STATUS** contenente lo stato del download.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | Do.h |
