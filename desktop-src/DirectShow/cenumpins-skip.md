---
description: Il metodo Skip ignora un numero specificato di segnaposto nella sequenza di enumerazione. Questo metodo implementa il metodo IEnumPins::Skip.
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Metodo CEnumPins.Skip (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02a499c38564fba4671e5c6dbf53bc59dcf9a1acd925f9cef4d558456b675efd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389641"
---
# <a name="cenumpinsskip-method"></a>Metodo CEnumPins.Skip

Il `Skip` metodo ignora un numero specificato di segnaposto nella sequenza di enumerazione. Questo metodo implementa il [**metodo IEnumPins::Skip.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cPins* 
</dt> <dd>

Numero di pin da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Ignorato oltre la fine della sequenza.<br/>                                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                                                                    |
| <dl> <dt>**ENUMERAZIONE VFW \_ \_ NON \_ \_ \_ SINCRONIZZATA**</dt> </dl> | Lo stato del filtro è cambiato e ora è incoerente con l'enumeratore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




