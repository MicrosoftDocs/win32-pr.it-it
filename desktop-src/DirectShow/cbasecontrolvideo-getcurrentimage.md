---
description: Il metodo GetCurrentImage recupera una copia dell'immagine corrente nel renderer.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Metodo CBaseControlVideo. GetCurrentImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333802"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>CBaseControlVideo. GetCurrentImage, metodo

Il `GetCurrentImage` metodo recupera una copia dell'immagine corrente nel renderer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Puntatore alla dimensione del buffer di output.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Puntatore al buffer di output per l'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.



| Codice restituito                                                                                        | Descrizione                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ non riescono**</dt> </dl>             | Esito negativo.<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | Argomento non valido.<br/>                                                      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>      | Memoria insufficiente. Restituito quando il parametro *pVideoInfo* è **null**.<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Esito positivo.<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ non \_ sospeso**</dt> </dl> | Non è stato possibile eseguire l'operazione perché il filtro non è sospeso.<br/> |



 

## <a name="remarks"></a>Commenti

Questa funzione membro recupera l'immagine dall'esempio e la copia nel buffer di output. La sezione del video copiato nel buffer di output riflette il rettangolo di origine impostato tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Non riflette il rettangolo di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




