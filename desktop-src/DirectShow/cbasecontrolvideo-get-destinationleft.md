---
description: Il metodo get \_ DestinationLeft recupera la coordinata sinistra del rettangolo di destinazione corrente.
ms.assetid: f1c6d784-7ec3-4d44-a3fb-c1e3b988e392
title: CBaseControlVideo.get_DestinationLeft metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ec35cc3fa831218fb7c5c4810643d58b9c9d303a9501d10969d847649c2efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661517"
---
# <a name="cbasecontrolvideoget_destinationleft-method"></a>Metodo CBaseControlVideo.get \_ DestinationLeft

Il `get_DestinationLeft` metodo recupera la coordinata sinistra del rettangolo di destinazione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DestinationLeft(
   long *pDestinationLeft
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestinationLeft* 
</dt> <dd>

Puntatore alla coordinata sinistra del rettangolo di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione. può essere uno dei valori seguenti o altri valori non elencati.



| Codice restituito                                                                                           | Descrizione                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Esito negativo.<br/>                                                              |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>             | Argomento del puntatore **NULL.**<br/>                                            |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Non è possibile eseguire l'operazione perché i pin non sono connessi.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Operazione completata.<br/>                                                              |



 

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IBasicVideo::get \_ DestinationLeft.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft)

Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite [**l'interfaccia IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) Il rettangolo di origine influisce sulla sezione dell'origine video nativa che verrà visualizzata sullo schermo. Il rettangolo di destinazione influisce sulla posizione in cui verrà visualizzato il video durante la riproduzione. Il rettangolo di destinazione è relativo all'area client della finestra in cui viene riprodotto. L'angolo superiore sinistro della finestra è la coordinata (0,0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




