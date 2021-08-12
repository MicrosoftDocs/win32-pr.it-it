---
title: Metodo IDODownload::SetProperty
description: Imposta una proprietà di download.
keywords:
- Metodo IDODownload::SetProperty
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7d966edb083107b80f0723bce195bfc588797efb8ad1931e0e75a468bec5a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543900"
---
# <a name="idodownloadsetproperty-method"></a>Metodo IDODownload::SetProperty

Imposta una proprietà di download. Il metodo accetta un puntatore a **UN VARIANT** che contiene una proprietà specifica da applicare al download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parametri

`propId`

ID di proprietà obbligatorio da impostare (di tipo **DODownloadProperty**).

`propVal`

Valore della proprietà da impostare, archiviato in un **elemento VARIANT.**

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [.](/windows/desktop/com/com-error-codes-10)

|Valore restituito|Descrizione|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* sconosciuto.|
|DO_E_INVALID_STATE|Il download non è attualmente in uno stato che consente l'impostazione delle proprietà.|

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | Do.h |
