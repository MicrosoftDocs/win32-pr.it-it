---
description: Il metodo QuerySupported determina se un oggetto supporta un set di proprietà specificato.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: Metodo IKsPropertySet::QuerySupported (Ks.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 7c79e81171349e2c481535eeab212717de072b17778b052dac3fc377cea0e094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792321"
---
# <a name="ikspropertysetquerysupported-method"></a>Metodo IKsPropertySet::QuerySupported

Il `QuerySupported` metodo determina se un oggetto supporta un set di proprietà specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*guidPropSet* \[ Pollici\]
</dt> <dd>

GUID del set di proprietà.

</dd> <dt>

*dwPropID* \[ Pollici\]
</dt> <dd>

Identificatore della proprietà all'interno del set di proprietà.

</dd> <dt>

*pTypeSupport* \[ Cambio\]
</dt> <dd>

Puntatore a un valore in cui archiviare i flag che indicano il supporto fornito dal driver. I flag supportati includono i seguenti.



| Valore                    | Descrizione                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| KSPROPERTY \_ SUPPORT \_ GET | È possibile recuperare la proprietà chiamando il [**metodo IKsPropertySet::Get.**](ikspropertyset-get.md) |
| KSPROPERTY \_ SUPPORT \_ SET | È possibile modificare la proprietà chiamando [**IKsPropertySet::Set**](ikspropertyset-set.md).              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                              | Descrizione                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | La combinazione di set di proprietà e ID di proprietà specificata è supportata.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                | Il set di proprietà non è supportato.<br/>                                       |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl>  | L'ID proprietà non è supportato per il set di proprietà specificato.<br/>         |
| <dl> <dt>**E \_ PROP \_ SET \_ UNSUPPORTED**</dt> </dl> | Il set di proprietà non è supportato.<br/>                                       |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Un'altra interfaccia con questo nome esiste nel file di intestazione dsound.h. Le due interfacce non sono compatibili. **L'interfaccia IKsControl,** documentata in DirectShow DDK, è ora l'interfaccia consigliata per il passaggio di set di proprietà tra i driver WDM e i componenti in modalità utente.

 

È necessario includere Ks.h prima di Ksproxy.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                             |
| Intestazione<br/>                   | <dl> <dt>Ks.h; </dt> <dt>Ksproxy.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




