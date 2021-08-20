---
description: "CFactoryTemplate::m_lpfnNew membro: puntatore a una funzione che crea un'istanza dell'oggetto."
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
ms.openlocfilehash: 5a08b0f1b3dc28b70e62866b58a952b12959f0a7f753d5e6b4c847489b52bfd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317721"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>CFactoryTemplate::m \_ lpfnNew member

Puntatore a una funzione che crea un'istanza dell'oggetto .

## <a name="syntax"></a>Sintassi


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Osservazioni

Nella DLL dichiarare una funzione statica che restituisce un puntatore a una nuova istanza dell'oggetto . Nel modello factory impostare la variabile membro **m \_ lpfnNew** sull'indirizzo di questa funzione statica.

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
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




