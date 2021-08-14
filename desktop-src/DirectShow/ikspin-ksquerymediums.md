---
description: Il metodo KsQueryMediums recupera i medie supportati da un pin.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: Metodo IKsPin::KsQueryMediums (Ksproxy.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 33edb7cb2ca959080878f7ce735930ceec9d95dc2f829aef6d50f72d764f2f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398937"
---
# <a name="ikspinksquerymediums-method"></a>Metodo IKsPin::KsQueryMediums

Il `KsQueryMediums` metodo recupera i medie supportati da un pin.

## <a name="syntax"></a>Sintassi


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppmi* \[ Cambio\]
</dt> <dd>

Indirizzo di un puntatore a [**una struttura KSMULTIPLE \_ ITEM.**](ksmultiple-item.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo restituisce una struttura [**KSMULTIPLE \_ ITEM**](ksmultiple-item.md) allocata dall'attività, seguita da zero o più strutture [**REGPINMEDIUM.**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) Il **membro Count** della struttura **KSMULTIPLE \_ ITEM** specifica il numero di **strutture REGPINMEDIUM.** Ogni **struttura REGPINMEDIUM** definisce un supporto supportato dal pin.

Il chiamante deve liberare le strutture restituite usando la **funzione CoTaskMemFree.**

È necessario includere Ks.h prima di Ksproxy.h.

## <a name="examples"></a>Esempio

La funzione helper seguente tenta di trovare una corrispondenza tra un pin e un supporto specificato.


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
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

[**Interfaccia IKsPin**](ikspin.md)
</dt> <dt>

[Filtri del driver di classe WDM](wdm-class-driver-filters.md)
</dt> </dl>

 

 




