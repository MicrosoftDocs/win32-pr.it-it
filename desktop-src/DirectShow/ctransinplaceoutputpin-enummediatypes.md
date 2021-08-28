---
description: 'Metodo CTransInPlaceOutputPin.EnumMediaTypes: il metodo EnumMediaTypes enumera i tipi di supporti preferiti del pin. Questo metodo implementa il metodo IPin::EnumMediaTypes.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Metodo CTransInPlaceOutputPin.EnumMediaTypes (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7a351f947b0526b8daf77b0b15ea0d2a2894ef6ff90390be484b5d0ce4b7fa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076171"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>Metodo CTransInPlaceOutputPin.EnumMediaTypes

Il `EnumMediaTypes` metodo enumera i tipi di supporti preferiti del pin. Questo metodo implementa il [**metodo IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* 
</dt> <dd>

Riceve un puntatore [**all'interfaccia IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Memoria insufficiente.<br/>                     |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>             | **Puntatore NULL.**<br/>                        |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin di input del filtro non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce **l'interfaccia IEnumMediaTypes** dal pin di output upstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




