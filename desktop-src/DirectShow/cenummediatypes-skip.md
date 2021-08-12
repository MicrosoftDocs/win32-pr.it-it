---
description: Il metodo Skip ignora un numero specificato di tipi di supporti. Questo metodo implementa il metodo IEnumMediaTypes::Skip.
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Metodo CEnumMediaTypes.Skip (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a9930472b5c8a2873ca0a7f3280565bd41ac6b0aac7e1e33303464d3a2c1ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656446"
---
# <a name="cenummediatypesskip-method"></a>Metodo CEnumMediaTypes.Skip

Il `Skip` metodo ignora un numero specificato di tipi di supporti. Questo metodo implementa il [**metodo IEnumMediaTypes::Skip.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Numero di tipi di supporti da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Ignorato oltre la fine della sequenza.<br/>                                    |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                                                                 |
| <dl> <dt>**ENUMERAZIONE VFW \_ \_ NON \_ \_ \_ SINCRONIZZATA**</dt> </dl> | Lo stato del pin è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




