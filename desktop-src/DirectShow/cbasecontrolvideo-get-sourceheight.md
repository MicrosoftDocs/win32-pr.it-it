---
description: Il \_ metodo Get SourceHeight recupera l'altezza del rettangolo di origine corrente.
ms.assetid: bf727cf6-9143-41f0-a482-782a4178ea92
title: Metodo CBaseControlVideo.get_SourceHeight (Ctlutil. h)
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
ms.openlocfilehash: b724f63907c8372867095b059ff728b4c646df21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327563"
---
# <a name="cbasecontrolvideoget_sourceheight-method"></a>Metodo CBaseControlVideo. Get \_ SourceHeight

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

Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.



| Codice restituito                                                                                           | Descrizione                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ non riescono**</dt> </dl>                | Esito negativo.<br/>                                                              |
| <dl> <dt>**\_puntatore E**</dt> </dl>             | Argomento puntatore **null** .<br/>                                            |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Impossibile eseguire l'operazione perché i pin non sono connessi.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Esito positivo.<br/>                                                              |



 

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) .

Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto. Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione. L'angolo superiore sinistro della finestra è coordinata (0, 0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




