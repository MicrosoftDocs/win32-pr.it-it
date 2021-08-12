---
description: Il metodo GetDestinationPosition recupera il rettangolo di destinazione in un'unica operazione atomica.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Metodo CBaseControlVideo.GetDestinationPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b077548e6a427e70d098cbece93cdc033972cf48a664dd85cd0dfab747d88c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661145"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a>Metodo CBaseControlVideo.GetDestinationPosition

Il `GetDestinationPosition` metodo recupera il rettangolo di destinazione in un'unica operazione atomica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLeft* 
</dt> <dd>

Puntatore alla coordinata sinistra del rettangolo di destinazione.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntatore alla coordinata superiore del rettangolo di destinazione.

</dd> <dt>

*pWidth* 
</dt> <dd>

Puntatore alla larghezza del rettangolo di destinazione.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntatore all'altezza del rettangolo di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione. può essere uno dei valori seguenti o altri valori non elencati.



| Codice restituito                                                                                           | Descrizione                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Esito negativo.<br/>                                                              |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>             | Argomento del puntatore **NULL.**<br/>                                            |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Impossibile eseguire l'operazione perché i pin non sono connessi.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Operazione completata.<br/>                                                              |



 

## <a name="remarks"></a>Commenti

Questa funzione membro può essere usata al posto di chiamate separate alle funzioni membro [**CBaseControlVideo::get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo::get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo::get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)e [**CBaseControlVideo::get \_ DestinationHeight.**](cbasecontrolvideo-get-destinationheight.md) Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite [**l'interfaccia IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) Il rettangolo di origine influisce sulla sezione dell'origine video nativa che verrà visualizzata sullo schermo. il rettangolo di destinazione influisce sulla posizione in cui verrà visualizzato il video quando viene riprodotto. Il rettangolo di destinazione è relativo all'area client della finestra in cui viene riprodotto. L'angolo superiore sinistro della finestra è la coordinata (0,0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




