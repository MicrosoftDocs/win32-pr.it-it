---
description: Il metodo get \_ SourceHeight recupera l'altezza del rettangolo di origine corrente.
ms.assetid: bf727cf6-9143-41f0-a482-782a4178ea92
title: CBaseControlVideo.get_SourceHeight metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0019678054b8cce9aafad302818f40d2076931b27295c43d57b71e8e13eb7b95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057121"
---
# <a name="cbasecontrolvideoget_sourceheight-method"></a>Metodo CBaseControlVideo.get \_ SourceHeight

Il `get_SourceHeight` metodo recupera l'altezza del rettangolo di origine corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SourceHeight(
   long *pSourceHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSourceHeight* 
</dt> <dd>

Puntatore all'altezza del rettangolo di origine.

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

Questa funzione membro implementa il [**metodo IBasicVideo::get \_ SourceHeight.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight)

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

 

 




