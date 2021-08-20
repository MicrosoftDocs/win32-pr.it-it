---
title: Metodo IDODownloadInternal::GetPropertyEx
description: Recupera un puntatore a un **variant che** contiene un valore della proprietà di download esteso specifico.
keywords:
- Metodo IDODownloadInternal::GetPropertyEx
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e812c82d1159651f7ad8567f0039555835f32911c9f5a8a92b6cedd3fb84dcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101673"
---
# <a name="idodownloadinternalgetpropertyex-method"></a>Metodo IDODownloadInternal::GetPropertyEx

> [!IMPORTANT]
> **L'interfaccia IDODownloadInternal** è deprecata. Usare invece [l'interfaccia IDODownload.](../do/nn-do-idodownload.md)

Recupera un puntatore a un **variant che** contiene un valore della proprietà di download esteso specifico.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parametri

`propId`

ID di proprietà obbligatorio da ottenere (di **tipo DODownloadPropertyEx).**

`propVal`

Valore della proprietà risultante, archiviato in un **variant.**

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10).

|Valore restituito|Descrizione|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* è sconosciuto.|
|DO_E_WRITE_ONLY_PROPERTY|La proprietà è di sola scrittura e non può essere letta.|
|E_NOT_SET|Tale proprietà non è stata impostata **tramite SetPropertyEx.**|

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | DODownloadInternal.h |