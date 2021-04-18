---
description: 'Il metodo seproperties specifica il numero di buffer da allocare e le dimensioni di ogni buffer. Questo metodo implementa il metodo IMemAllocator:: SetValue.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Metodo CBaseAllocator. seproperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331800"
---
# <a name="cbaseallocatorsetproperties-method"></a>Metodo CBaseAllocator. seproperties

Il `SetProperties` metodo specifica il numero di buffer da allocare e le dimensioni di ogni buffer. Questo metodo implementa il metodo [**IMemAllocator::**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) SetValue.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRequest* 
</dt> <dd>

Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer.

</dd> <dt>

*pActual* 
</dt> <dd>

Puntatore a una struttura di **\_ proprietà dell'allocatore** che riceve le proprietà effettive del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                                 | Descrizione                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                        | Esito positivo.<br/>                                                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>                   | Argomento puntatore **null** .<br/>                                 |
| <dl> <dt>**è \_ \_ già stato \_ eseguito il commit di VFW**</dt> </dl>   | Non è possibile modificare la memoria allocata mentre il filtro è attivo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | È stato specificato un allineamento non valido.<br/>                        |
| <dl> <dt>**\_buffer VFW E in \_ \_ attesa**</dt> </dl> | Uno o più buffer sono ancora attivi.<br/>                      |



 

## <a name="remarks"></a>Commenti

Questo metodo specifica i requisiti del buffer, ma non alloca i buffer. Chiamare il metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) per allocare i buffer.

Il chiamante alloca due strutture delle proprietà dell'ALLOCAtore \_ . Il parametro *pRequest* contiene i requisiti del buffer del chiamante, inclusi il numero di buffer e le dimensioni di ogni buffer. Quando il metodo viene restituito, il parametro *pActual* contiene le proprietà del buffer effettive, impostate dall'allocatore. Nella classe di base, supponendo che il metodo abbia esito positivo, le proprietà effettive corrispondono sempre alle proprietà richieste. Le classi derivate potrebbero ignorare questo comportamento.

L'allocatore non deve essere sottoposta a commit e non deve avere buffer in attesa. Nella classe di base, l'allineamento deve essere uguale a 1. La classe [**CMemAllocator**](cmemallocator.md) esegue l'override di questo requisito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




