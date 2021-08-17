---
title: Metodo IDODownload::GetProperty
description: Recupera un puntatore a un **variant** che contiene una proprietà di download specifica.
keywords:
- Metodo IDODownload::GetProperty
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
ms.openlocfilehash: f498900e8dd2e87460a5fe4e75ea1269272788488159379d64f5332f2006f97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736248"
---
# <a name="idodownloadgetproperty-method"></a>Metodo IDODownload::GetProperty

Recupera un puntatore a un **variant** che contiene una proprietà di download specifica.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parametri

`propId`

ID di proprietà obbligatorio da ottenere (di **tipo DODownloadProperty).**

`propVal`

Valore della proprietà risultante, archiviato in un **variant.**

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10).

|Valore restituito|Descrizione|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* è sconosciuto.|
|DO_E_WRITE_ONLY_PROPERTY|La proprietà è di sola scrittura e non può essere letta.|
|E_NOT_SET|Tale proprietà non è stata impostata **tramite SetProperty.**|

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | Do.h |
