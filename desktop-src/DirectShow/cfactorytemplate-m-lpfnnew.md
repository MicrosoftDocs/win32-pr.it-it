---
description: Puntatore a una funzione che crea un'istanza dell'oggetto.
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Membro CFactoryTemplate:: m_lpfnNew (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329821"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>Membro lpfnNew di CFactoryTemplate:: m \_

Puntatore a una funzione che crea un'istanza dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Osservazioni

Nella DLL dichiarare una funzione statica che restituisce un puntatore a una nuova istanza dell'oggetto. Nel modello Factory impostare la variabile membro **\_ lpfnNew m** sull'indirizzo della funzione statica.

Il tipo di puntatore a funzione è [**LPFNNewCOMObject**](lpfnnewcomobject.md).

Nell'esempio seguente viene illustrata una funzione tipica per **m \_ lpfnNew**:


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




