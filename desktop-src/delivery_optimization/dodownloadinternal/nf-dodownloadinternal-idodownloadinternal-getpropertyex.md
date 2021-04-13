---
title: 'Metodo IDODownloadInternal:: GetPropertyEx'
description: Recupera un puntatore a un **Variant** che contiene un valore di proprietà di download esteso specifico.
keywords:
- 'Metodo IDODownloadInternal:: GetPropertyEx'
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
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399285"
---
# <a name="idodownloadinternalgetpropertyex-method"></a>Metodo IDODownloadInternal:: GetPropertyEx

> [!IMPORTANT]
> L'interfaccia **IDODownloadInternal** è deprecata. Usare invece l'interfaccia [IDODownload](../do/nn-do-idodownload.md) .

Recupera un puntatore a un **Variant** che contiene un valore di proprietà di download esteso specifico.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parametri

`propId`

ID di proprietà obbligatorio da ottenere (di tipo **DODownloadPropertyEx**).

`propVal`

Il valore della proprietà risultante, archiviato in una **variante**.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valore restituito|Descrizione|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propid* è sconosciuto.|
|DO_E_WRITE_ONLY_PROPERTY|La proprietà è di sola scrittura e non può essere letta.|
|E_NOT_SET|Questa proprietà non è stata impostata tramite **SetPropertyEx**.|

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | DODownloadInternal. h |