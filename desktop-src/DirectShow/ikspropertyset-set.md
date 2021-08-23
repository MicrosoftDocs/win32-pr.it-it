---
description: Il metodo Set imposta una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: Metodo IKsPropertySet::Set (Ksproxy.h)
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
ms.openlocfilehash: f3669acb7f2d3049b909a4dc2c24363bf478c9b44ad0a91528e1e8ea466399fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639191"
---
# <a name="ikspropertysetset-method"></a>Metodo IKsPropertySet::Set

Il `Set` metodo imposta una proprietà identificata da un GUID del set di proprietà e da un ID proprietà.

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

*guidPropSet* \[ Pollici\]
</dt> <dd>

GUID del set di proprietà.

</dd> <dt>

*dwPropID* \[ Pollici\]
</dt> <dd>

Identificatore della proprietà all'interno del set di proprietà.

</dd> <dt>

*pInstanceData* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene i dati dell'istanza per la proprietà.

</dd> <dt>

*cbInstanceData* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *pInstanceData,* in byte.

</dd> <dt>

*pPropData* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene il valore della proprietà.

</dd> <dt>

*cbPropData* \[ Pollici\]
</dt> <dd>

Sise del buffer *pPropData,* in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                              | Descrizione                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Operazione completata.<br/>                                                         |
| <dl> <dt>**E \_ PROP \_ SET \_ UNSUPPORTED**</dt> </dl> | Il set di proprietà non è supportato.<br/>                               |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl>  | L'ID della proprietà non è supportato per il set di proprietà specificato.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Un'altra interfaccia con questo nome esiste nel file di intestazione dsound.h. Le due interfacce non sono compatibili. **L'interfaccia IKsControl,** documentata in DirectShow DDK, è ora l'interfaccia consigliata per il passaggio di set di proprietà tra i driver WDM e i componenti in modalità utente.

 

È necessario includere Ks.h prima di Ksproxy.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Libreria<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




