---
title: 'Metodo IDODownloadStatusCallback:: OnStatusChange'
description: Chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato del download.
keywords:
- 'Metodo IDODownloadStatusCallback:: OnStatusChange'
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
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104046146"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>Metodo IDODownloadStatusCallback:: OnStatusChange

Chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato del download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parametri

`download`

Puntatore all'interfaccia **IDODownload** il cui stato è stato modificato.

`status`

Puntatore a una struttura **DO_DOWNLOAD_STATUS** contenente lo stato del download.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |
