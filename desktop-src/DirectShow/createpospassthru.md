---
description: La funzione CreatePosPassThru crea un oggetto CPosPassThru o un oggetto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Funzione CreatePosPassThru (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0118299bd328d09d77ccbb8d5258b25c0ac57bdc21fc7a47f642374e8be12357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908751"
---
# <a name="createpospassthru-function"></a>Funzione CreatePosPassThru

La `CreatePosPassThru` funzione crea un oggetto [**CPosPassThru**](cpospassthru.md) o [**un oggetto CRendererPosPassThru.**](crendererpospassthru.md)

## <a name="syntax"></a>Sintassi


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAgg* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*bRenderer* 
</dt> <dd>

Valore booleano che specifica se il filtro è un renderer. Usare il valore **TRUE se** il filtro è un renderer oppure FALSE **in caso** contrario. Se il valore è **TRUE,** questo metodo crea un'istanza della [**classe CRendererPosPassThru.**](crendererpospassthru.md) Se il valore è **FALSE,** il metodo crea un'istanza della **classe CPosPassThru.**

</dd> <dt>

*pPin* 
</dt> <dd>

Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) sul pin di input del filtro.

</dd> <dt>

*ppPassThru* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore **all'interfaccia IUnknown** dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo. In caso contrario, restituisce **un valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo usa [**l'interfaccia ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) per creare l'oggetto . L'oggetto viene caricato dinamicamente da Quartz.dll.

Se la funzione ha esito positivo, **l'interfaccia IUnknown restituita** ha un conteggio dei riferimenti in sospeso. Il chiamante deve rilasciare l'interfaccia .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




