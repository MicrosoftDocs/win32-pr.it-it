---
description: Il metodo DecideBufferSize imposta i requisiti del buffer del PIN di output.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Metodo CTransInPlaceFilter. DecideBufferSize (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326395"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>CTransInPlaceFilter. DecideBufferSize, metodo

Il `DecideBufferSize` metodo imposta i requisiti del buffer del PIN di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlloc* 
</dt> <dd>

Puntatore all'oggetto [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usato dal pin di output.

</dd> <dt>

*pProperties* 
</dt> <dd>

Puntatore alle proprietà allocatore richieste per conteggio, dimensioni e allineamento, come specificato dalla struttura delle [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                            | Descrizione        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Operazione riuscita<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Errore<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando la classe **CTransInPlaceFilter** deve fornire una dimensione del buffer al filtro downstream. Se il filtro **CTransInPlaceFilter** è già connesso a upstream, USA le proprietà dell'allocatore nella connessione pin upstream. In caso contrario, le dimensioni del buffer vengono impostate su 1 byte come valore temporaneo del segnaposto. Quando il filtro upstream si connette, la classe **CTransInPlaceFilter** rinegozia l'allocatore downstream. Per ulteriori informazioni sul processo di connessione del PIN in questa classe, vedere [**classe CTransInPlaceFilter**](ctransinplacefilter.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




