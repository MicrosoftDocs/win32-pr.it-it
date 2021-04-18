---
description: La \_ macro DECLARE IUnknown dichiara i tre metodi dell'interfaccia di base per una nuova interfaccia.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330661"
---
# <a name="declare_iunknown"></a>DICHIARARE \_ IUnknown

La macro **Declare \_ IUnknown** dichiara i tre metodi dell'interfaccia di base per una nuova interfaccia.

**Sintassi**

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a>Commenti

Quando si crea una nuova interfaccia, deve derivare da **IUnknown**, che ha tre metodi: **QueryInterface**, **AddRef** e **Release**. Questa macro semplifica il processo di dichiarazione dichiarando ognuno di questi metodi per la nuova interfaccia.

Questa macro funziona solo con le classi che derivano, direttamente o indirettamente, dalla classe [**CUnknown**](cunknown.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni helper COM**](com-helper-functions.md)
</dt> <dt>

[**CUnknown:: GetOwner**](cunknown-getowner.md)
</dt> <dt>

[Come implementare IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




