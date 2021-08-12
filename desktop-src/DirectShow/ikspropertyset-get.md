---
description: Il metodo Get recupera una proprietà identificata da un GUID del set di proprietà e da un ID proprietà.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: Metodo IKsPropertySet::Get (Ksproxy.h)
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
ms.openlocfilehash: fbfd44002270209c055b5a4003d9062a6821aeffb3ce71de7977fc20d0c64e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652243"
---
# <a name="ikspropertysetget-method"></a>Metodo IKsPropertySet::Get

Il **metodo Get** recupera una proprietà identificata da un GUID del set di proprietà e da un ID proprietà.

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

*guidPropSet* \[ Pollici\]
</dt> <dd>

GUID del set di proprietà .

</dd> <dt>

*dwPropID* \[ Pollici\]
</dt> <dd>

Identificatore della proprietà all'interno del set di proprietà.

</dd> <dt>

*pInstanceData* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di byte che contiene i dati dell'istanza per la proprietà.

</dd> <dt>

*cbInstanceData* \[ Pollici\]
</dt> <dd>

Dimensione della matrice specificata in *pInstanceData,* in byte.

</dd> <dt>

*pPropData* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di byte che riceve i dati della proprietà.

</dd> <dt>

*cbPropData* \[ Pollici\]
</dt> <dd>

Dimensione della matrice specificata in *pPropData,* in byte.

</dd> <dt>

*pcbReturned* \[ Cambio\]
</dt> <dd>

Riceve il numero di byte copiati dal metodo nella *matrice pPropData.*

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
> Un'altra interfaccia con questo nome esiste nel file di intestazione dsound.h. Le due interfacce non sono compatibili. [L'interfaccia IKsControl,](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) documentata in DirectShow DDK, è ora l'interfaccia consigliata per il passaggio di set di proprietà tra i driver WDM e i componenti in modalità utente.

 

Per recuperare una proprietà, allocare un buffer che verrà quindi riempito da questo metodo. Per determinare le dimensioni del buffer necessarie, specificare **NULL** per *pPropData* e zero (0) per *cbPropData*. Questo metodo restituisce le dimensioni del buffer necessarie in *pcbReturned.*

È necessario includere Ks.h prima di Ksproxy.h.

## <a name="examples"></a>Esempio

L'esempio seguente esegue una query su un pin per la relativa categoria di pin recuperando la **proprietà AMPROPERTY \_ PIN \_ CATEGORY.** Vedere Aggiungere [un set di proprietà.](pin-property-set.md)


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

 

 
