---
description: Il metodo set imposta una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'Metodo IKsPropertySet:: set (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401201"
---
# <a name="ikspropertysetset-method"></a>Metodo IKsPropertySet:: set

Il `Set` metodo imposta una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
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

*pInstanceData* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene i dati dell'istanza per la proprietà.

</dd> <dt>

*cbInstanceData* \[ in\]
</dt> <dd>

Dimensioni del buffer *pInstanceData* in byte.

</dd> <dt>

*pPropData* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene il valore della proprietà.

</dd> <dt>

*cbPropData* \[ in\]
</dt> <dd>

Sise del buffer *pPropData* , in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                              | Descrizione                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Esito positivo.<br/>                                                         |
| <dl> <dt>**\_Set Prop \_ non \_ supportato**</dt> </dl> | Il set di proprietà non è supportato.<br/>                               |
| <dl> <dt>**\_ID Prop \_ non \_ supportato**</dt> </dl>  | ID di proprietà non supportato per il set di proprietà specificato.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome. Le due interfacce non sono compatibili. L'interfaccia **IKsControl** , documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente.

 

Prima di ksproxy. h, è necessario includere KS. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Libreria<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




