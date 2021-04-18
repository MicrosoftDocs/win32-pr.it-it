---
description: 'Il metodo Skip ignora un numero specificato di tipi di supporti. Questo metodo implementa il metodo IEnumMediaTypes:: Skip.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Metodo CEnumMediaTypes. Skip (Amfilter. h)
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
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329849"
---
# <a name="cenummediatypesskip-method"></a>Metodo CEnumMediaTypes. Skip

Il `Skip` metodo ignora un numero specificato di tipi di supporti. Questo metodo implementa il metodo [**IEnumMediaTypes:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .

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

Numero di tipi di supporto da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Ignorato oltre la fine della sequenza.<br/>                                    |
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                                                                 |
| <dl> <dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt> </dl> | Lo stato del PIN è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




