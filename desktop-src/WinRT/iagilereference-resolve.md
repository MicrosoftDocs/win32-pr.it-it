---
description: Ottiene l'ID interfaccia di un riferimento Agile a un oggetto .
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: Metodo IAgileReference::Resolve
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 0b58013ba81bb394715a0042f3f3d7435a381fa01f5b985bd9ad81d12122441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758777"
---
# <a name="iagilereferenceresolve-method"></a>Metodo IAgileReference::Resolve

Ottiene l'ID interfaccia di un riferimento Agile a un oggetto .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ Pollici\]
</dt> <dd>

ID interfaccia dell'interfaccia da recuperare dal riferimento Agile. Non è necessario che sia uguale all'interfaccia registrata.

</dd> <dt>

*ppvObjectReference* \[ out, retval\]
</dt> <dd>

Al termine, \* *ppvObjectReference* è un puntatore all'interfaccia specificata da *riid*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore restituito                                                                              | Descrizione                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>          | Metodo completato correttamente.<br/>                                  |
| <dl> <dt>E \_ NOINTERFACE</dt> </dl> | L'interfaccia richiesta non viene implementata nell'oggetto registrato.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare la [**funzione RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) per creare un riferimento Agile a un oggetto. Chiamare il **metodo Resolve** per localizzare l'oggetto nell'apartment in cui viene **chiamato Resolve.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




