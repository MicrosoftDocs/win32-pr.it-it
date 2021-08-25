---
title: Metodo IDODownloadInternal::SetPropertyEx
description: Imposta una proprietà di download estesa. Il metodo accetta un puntatore a **un variant** che contiene un valore di proprietà specifico da applicare al download.
keywords:
- Metodo IDODownloadInternal::SetPropertyEx
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: d6156f4309c0eac9d2d250c85f7e9ab365e4a3b1e4072aabec7f6aa7e17c437f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858801"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>Metodo IDODownloadInternal::SetPropertyEx

> [!IMPORTANT]
> **L'interfaccia IDODownloadInternal** è deprecata. Usare invece [l'interfaccia IDODownload.](../do/nn-do-idodownload.md)

Imposta una proprietà di download estesa. Il metodo accetta un puntatore a **un variant** che contiene un valore di proprietà specifico da applicare al download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parametri

`propId`

ID di proprietà obbligatorio da impostare (di **tipo DODownloadPropertyEx).**

`propVal`

Valore della proprietà da impostare, archiviato in un **variant.**

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10).

|Valore restituito|Descrizione|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* è sconosciuto.|
|DO_E_INVALID_STATE|Il download non è attualmente in uno stato che consente l'impostazione delle proprietà.|

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | DODownloadInternal.h |