---
description: "CFactoryTemplate::m_lpfnNew membro : puntatore a una funzione che crea un'istanza dell'oggetto."
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: Membro CFactoryTemplate::m_lpfnNew (Combase.h)
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
ms.openlocfilehash: ee4ec8e1503d3b260e025d154624b2d7c09bb49b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095649"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>CFactoryTemplate::m \_ lpfnNew member

Puntatore a una funzione che crea un'istanza dell'oggetto .

## <a name="syntax"></a>Sintassi


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Osservazioni

Nella DLL dichiarare una funzione statica che restituisce un puntatore a una nuova istanza dell'oggetto. Nel modello factory impostare la variabile **membro m \_ lpfnNew** sull'indirizzo di questa funzione statica.

Il tipo di puntatore a funzione [**è LPFNNewCOMObject**](lpfnnewcomobject.md).

L'esempio seguente illustra una funzione tipica per **m \_ lpfnNew**:


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
| Intestazione<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




