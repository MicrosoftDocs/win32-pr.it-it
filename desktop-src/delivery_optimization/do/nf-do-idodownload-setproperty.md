---
title: 'Metodo IDODownload:: SetProperty'
description: Imposta una proprietà di download.
keywords:
- 'Metodo IDODownload:: SetProperty'
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
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719564"
---
# <a name="idodownloadsetproperty-method"></a>Metodo IDODownload:: SetProperty

Imposta una proprietà di download. Il metodo accetta un puntatore a una **variante** che contiene una proprietà specifica da applicare al download.

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

Valore della proprietà da impostare, archiviato in una **variante**.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valore restituito|Descrizione|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propid* è sconosciuto.|
|DO_E_INVALID_STATE|Il download non è attualmente in uno stato che consente di impostare le proprietà.|

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |
