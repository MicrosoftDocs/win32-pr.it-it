---
description: Il metodo put \_ DestinationHeight imposta l'altezza del rettangolo di destinazione.
ms.assetid: 2cb7af2b-69dc-4e86-b2cf-34223c9e5a1b
title: CBaseControlVideo.put_DestinationHeight metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed1b8c43b835b1996f2f6dcb512b741f130235b86905b90fc0886c9cc0f7fd9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017429"
---
# <a name="cbasecontrolvideoput_destinationheight-method"></a>Metodo DestinationHeight CBaseControlVideo.put \_

Il `put_DestinationHeight` metodo imposta l'altezza del rettangolo di destinazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DestinationHeight(
   long DestinationHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DestinationHeight* 
</dt> <dd>

Nuova altezza di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione. può essere uno dei valori seguenti o altri valori non elencati.



| Codice restituito                                                                                           | Descrizione                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Esito negativo.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Argomento non valido.<br/>                                                     |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>             | Argomento del puntatore **NULL.**<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Operazione completata.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Impossibile eseguire l'operazione perché i pin non sono connessi.<br/> |



 

## <a name="remarks"></a>Commenti

Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite [**l'interfaccia IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) Il rettangolo di origine influisce sulla sezione dell'origine video nativa che verrà visualizzata sullo schermo. il rettangolo di destinazione influisce sulla posizione in cui verrà visualizzato il video quando viene riprodotto. Il rettangolo di destinazione è relativo all'area client della finestra in cui viene riprodotto. L'angolo superiore sinistro della finestra è la coordinata (0,0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




