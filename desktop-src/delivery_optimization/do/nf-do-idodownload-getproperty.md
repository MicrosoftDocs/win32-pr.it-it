---
title: 'Metodo IDODownload:: GetProperty'
description: Recupera un puntatore a un **Variant** che contiene una specifica proprietà di download.
keywords:
- 'Metodo IDODownload:: GetProperty'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857846"
---
# <a name="idodownloadgetproperty-method"></a>Metodo IDODownload:: GetProperty

Recupera un puntatore a un **Variant** che contiene una specifica proprietà di download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parametri

`propId`

ID di proprietà obbligatorio da ottenere (di tipo **DODownloadProperty**).

`propVal`

Il valore della proprietà risultante, archiviato in una **variante**.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valore restituito|Descrizione|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propid* è sconosciuto.|
|DO_E_WRITE_ONLY_PROPERTY|La proprietà è di sola scrittura e non può essere letta.|
|E_NOT_SET|Questa proprietà non è stata impostata tramite **SetProperty**.|

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |
