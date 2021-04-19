---
description: Il \_ metodo Get jitter recupera la deviazione standard del tempo in millisecondi tra ogni frame e il successivo per tutti i frame dall'avvio dello streaming.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Metodo CBaseVideoRenderer.get_Jitter (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326416"
---
# <a name="cbasevideorendererget_jitter-method"></a>Metodo CBaseVideoRenderer. Get \_ jitter

Il `get_Jitter` metodo recupera la deviazione standard di tempo in millisecondi tra ogni frame e il successivo per tutti i frame dall'avvio dello streaming.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*piJitter* 
</dt> <dd>

Puntatore alla deviazione standard del tempo di interframe, in millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IQualProp:: Get \_ jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




