---
description: Il metodo Get recupera una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'Metodo IKsPropertySet:: Get (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481764"
---
# <a name="ikspropertysetget-method"></a>Metodo IKsPropertySet:: Get

Il metodo **Get** recupera una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
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

Puntatore a una matrice di byte che contiene i dati dell'istanza per la proprietà.

</dd> <dt>

*cbInstanceData* \[ in\]
</dt> <dd>

Dimensioni in byte della matrice specificata in *pInstanceData*.

</dd> <dt>

*pPropData* \[ out\]
</dt> <dd>

Puntatore a una matrice di byte che riceve i dati della proprietà.

</dd> <dt>

*cbPropData* \[ in\]
</dt> <dd>

Dimensioni in byte della matrice specificata in *pPropData*.

</dd> <dt>

*pcbReturned* \[ out\]
</dt> <dd>

Riceve il numero di byte che il metodo copia nella matrice *pPropData* .

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
> Nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome. Le due interfacce non sono compatibili. L'interfaccia [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente.

 

Per recuperare una proprietà, allocare un buffer che verrà compilato da questo metodo. Per determinare le dimensioni del buffer necessarie, specificare **null** per *pPropData* e zero (0) per *cbPropData*. Questo metodo restituisce le dimensioni del buffer necessarie in *pcbReturned*.

Prima di ksproxy. h, è necessario includere KS. h.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene eseguita una query su un PIN per la relativa categoria pin, recuperando la proprietà di **\_ \_ categoria AMPROPERTY pin** . (Vedere [impostare la proprietà pin](pin-property-set.md)).


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



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

 

 
