---
description: Il metodo QuerySupported determina se un oggetto supporta un set di proprietà specificato.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Metodo IKsPropertySet:: QuerySupported (KS. h)'
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
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225397"
---
# <a name="ikspropertysetquerysupported-method"></a>Metodo IKsPropertySet:: QuerySupported

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

*guidPropSet* \[ in\]
</dt> <dd>

GUID del set di proprietà.

</dd> <dt>

*dwPropID* \[ in\]
</dt> <dd>

Identificatore della proprietà all'interno del set di proprietà.

</dd> <dt>

*pTypeSupport* \[ out\]
</dt> <dd>

Puntatore a un valore in cui archiviare i flag che indicano il supporto fornito dal driver. I flag supportati sono i seguenti.



| Valore                    | Descrizione                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| KSPROPERTY \_ supporto \_ Get | È possibile recuperare la proprietà chiamando il metodo [**IKsPropertySet:: Get**](ikspropertyset-get.md) . |
| \_set di supporto KSPROPERTY \_ | È possibile modificare la proprietà chiamando [**IKsPropertySet:: set**](ikspropertyset-set.md).              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                              | Descrizione                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Il set di proprietà e la combinazione di ID proprietà specificati sono supportati.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                | Il set di proprietà non è supportato.<br/>                                       |
| <dl> <dt>**\_ID Prop \_ non \_ supportato**</dt> </dl>  | ID di proprietà non supportato per il set di proprietà specificato.<br/>         |
| <dl> <dt>**\_Set Prop \_ non \_ supportato**</dt> </dl> | Il set di proprietà non è supportato.<br/>                                       |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome. Le due interfacce non sono compatibili. L'interfaccia **IKsControl** , documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente.

 

Prima di ksproxy. h, è necessario includere KS. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                             |
| Intestazione<br/>                   | <dl> <dt>KS. h; </dt> <dt>Ksproxy. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




