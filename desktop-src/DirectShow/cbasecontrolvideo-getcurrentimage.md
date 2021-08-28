---
description: Il metodo GetCurrentImage recupera una copia dell'immagine corrente nel renderer.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Metodo CBaseControlVideo.GetCurrentImage (Ctlutil.h)
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
ms.openlocfilehash: 782f540959b134f7ca00c2bc674a64ce60ccb4f6ddf166c79f2597e582ca9fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087571"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>Metodo CBaseControlVideo.GetCurrentImage

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

Restituisce un **valore HRESULT** che dipende dall'implementazione. può essere uno dei valori seguenti o altri valori non elencati.



| Codice restituito                                                                                        | Descrizione                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>             | Esito negativo.<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | Argomento non valido.<br/>                                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | Memoria insufficiente. Restituito quando *il parametro pVideoInfo* è **NULL.**<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Operazione completata.<br/>                                                               |
| <dl> <dt>**VFW \_ E NON IN \_ \_ PAUSA**</dt> </dl> | Impossibile eseguire l'operazione perché il filtro non è in pausa.<br/> |



 

## <a name="remarks"></a>Commenti

Questa funzione membro recupera l'immagine dall'esempio e la copia nel buffer di output. La sezione del video copiata nel buffer di output riflette il rettangolo di origine impostato tramite [**l'interfaccia IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) Non riflette il rettangolo di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




