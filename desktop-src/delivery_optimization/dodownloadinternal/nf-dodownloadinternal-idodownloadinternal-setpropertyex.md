---
title: 'Metodo IDODownloadInternal:: SetPropertyEx'
description: Imposta una proprietà di download estesa. Il metodo accetta un puntatore a una **variante** che contiene un valore della proprietà specifico da applicare al download.
keywords:
- 'Metodo IDODownloadInternal:: SetPropertyEx'
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
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963132"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>Metodo IDODownloadInternal:: SetPropertyEx

> [!IMPORTANT]
> L'interfaccia **IDODownloadInternal** è deprecata. Usare invece l'interfaccia [IDODownload](../do/nn-do-idodownload.md) .

Imposta una proprietà di download estesa. Il metodo accetta un puntatore a una **variante** che contiene un valore della proprietà specifico da applicare al download.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parametri

`propId`

ID di proprietà obbligatorio da impostare (di tipo **DODownloadPropertyEx**).

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
| **Intestazione** | DODownloadInternal. h |