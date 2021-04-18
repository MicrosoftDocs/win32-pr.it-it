---
description: La funzione CreatePosPassThru crea un oggetto CPosPassThru o un oggetto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Funzione CreatePosPassThru (Ctlutil. h)
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
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331313"
---
# <a name="createpospassthru-function"></a>CreatePosPassThru (funzione)

La `CreatePosPassThru` funzione crea un oggetto [**CPosPassThru**](cpospassthru.md) o un oggetto [**CRendererPosPassThru**](crendererpospassthru.md) .

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

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **null**.

</dd> <dt>

*bRenderer* 
</dt> <dd>

Valore booleano che specifica se il filtro è un renderer. Usare il valore **true** se il filtro è un renderer oppure **false** in caso contrario. Se il valore è **true**, questo metodo crea un'istanza della classe [**CRendererPosPassThru**](crendererpospassthru.md) . Se il valore è **false**, il metodo crea un'istanza della classe **CPosPassThru** .

</dd> <dt>

*pPin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) sul pin di input del filtro.

</dd> <dt>

*ppPassThru* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia **IUnknown** dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo. In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo utilizza l'interfaccia [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) per creare l'oggetto. L'oggetto viene caricato dinamicamente da Quartz.dll.

Se la funzione ha esito positivo, l'interfaccia **IUnknown** restituita presenta un conteggio dei riferimenti in attesa. Il chiamante deve rilasciare l'interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




