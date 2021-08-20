---
description: Richiama la funzionalità helper per l'interfaccia IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: Funzione InvokeIDispatch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 9708ebc5675d918c959be132d16037ac4e128650280b8243dcfe5c48834b602b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041871"
---
# <a name="invokeidispatch-function"></a>Funzione InvokeIDispatch

Richiama la funzionalità helper per l'interfaccia IDispatch.

Questa funzione non deve essere usata dal codice dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDispatch* 
</dt> <dd>

Istanza dell'interfaccia IDispatch.

</dd> <dt>

*Dispid* 
</dt> <dd>

Metodo, proprietà o argomento da passare.

</dd> <dt>

*pDisp* 
</dt> <dd>

Parametri da passare.

</dd> <dt>

*pVarResult* \[ Cambio\]
</dt> <dd>

Struttura che riceve i valori recuperati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. In caso di esito negativo, i possibili codici restituiti includono, ma non sono limitati, i valori illustrati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il valore per *pDispatch non* è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




