---
description: Ottiene l'ID di interfaccia di un riferimento agile a un oggetto.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'Metodo IAgileReference:: Resolve'
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
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307080"
---
# <a name="iagilereferenceresolve-method"></a>Metodo IAgileReference:: Resolve

Ottiene l'ID di interfaccia di un riferimento agile a un oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

ID di interfaccia dell'interfaccia da recuperare dal riferimento agile. Non è necessario che corrisponda all'interfaccia registrata.

</dd> <dt>

*ppvObjectReference* \[ out, retval\]
</dt> <dd>

Al termine, \* *ppvObjectReference* è un puntatore all'interfaccia specificata da *riid*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore restituito                                                                              | Descrizione                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>\_OK</dt> </dl>          | Metodo completato correttamente.<br/>                                  |
| <dl> <dt>E \_ NOinterface</dt> </dl> | L'interfaccia richiesta non è implementata nell'oggetto registrato.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare la funzione [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) per creare un riferimento agile a un oggetto. Chiamare il metodo **Resolve** per localizzare l'oggetto nell'Apartment in cui viene chiamata la **risoluzione** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>            |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




