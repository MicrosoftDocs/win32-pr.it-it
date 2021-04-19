---
description: Il \_ metodo Get AvgSyncOffset recupera la media del tempo in millisecondi tra la scadenza di ogni frame e il rendering effettivo per tutti i frame dall'avvio del flusso.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Metodo CBaseVideoRenderer.get_AvgSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326425"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>Metodo CBaseVideoRenderer. Get \_ AvgSyncOffset

Il `get_AvgSyncOffset` metodo recupera la media del tempo in millisecondi tra la scadenza di ogni frame e il rendering effettivo per tutti i frame dall'avvio del flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*piAvg* 
</dt> <dd>

Puntatore alla media del tempo descritto in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IQualProp:: Get \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




