---
description: 'Metodo CTransInPlaceFilter.DecideBufferSize: il metodo DecideBufferSize imposta i requisiti del buffer del pin di output.'
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Metodo CTransInPlaceFilter.DecideBufferSize (Transip.h)
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
ms.openlocfilehash: b3ffb3ec7b1ef59c6e7f3d49e39fbe69e8cc1c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094829"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>Metodo CTransInPlaceFilter.DecideBufferSize

Il `DecideBufferSize` metodo imposta i requisiti del buffer del pin di output.

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

Puntatore [**all'oggetto IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usato dal pin di output.

</dd> <dt>

*pProperties* 
</dt> <dd>

Puntatore alle proprietà dell'allocatore richieste per conteggio, dimensioni e allineamento, come specificato dalla [**struttura ALLOCATOR \_**](/windows/win32/api/strmif/ns-strmif-allocator_properties) PROPERTIES.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                            | Descrizione        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione riuscita<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Operazioni non riuscite<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando la **classe CTransInPlaceFilter** deve fornire una dimensione del buffer al filtro downstream. Se il **filtro CTransInPlaceFilter** è già connesso upstream, usa le proprietà dell'allocatore nella connessione pin upstream. In caso contrario, imposta le dimensioni del buffer su 1 byte come valore segnaposto temporaneo. Quando il filtro upstream si connette, la **classe CTransInPlaceFilter** rinegozia l'allocatore downstream. Per altre informazioni sul processo di connessione pin in questa classe, vedere [**Classe CTransInPlaceFilter.**](ctransinplacefilter.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




