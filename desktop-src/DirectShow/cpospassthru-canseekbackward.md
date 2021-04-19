---
description: "Il metodo CanSeekBackward determina se è possibile cercare il flusso all'indietro. Questo metodo implementa il metodo IMediaPosition:: CanSeekBackward."
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Metodo CPosPassThru. CanSeekBackward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325659"
---
# <a name="cpospassthrucanseekbackward-method"></a>CPosPassThru. CanSeekBackward, metodo

Il `CanSeekBackward` metodo determina se è possibile cercare il flusso all'indietro. Questo metodo implementa il metodo [**IMediaPosition:: CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCanSeekBackward* 
</dt> <dd>

Puntatore a una variabile che riceve il valore OATRUE se il filtro può cercare indietro o OAFALSE in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




