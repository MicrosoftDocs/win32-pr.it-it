---
description: Il metodo SetDefaultDestinationPosition imposta di nuovo il renderer sull'utilizzo della posizione di destinazione predefinita (in genere l'intera area client della finestra).
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: Metodo CBaseControlVideo. SetDefaultDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a959f462d410b83588fb1a8df87cebffd879d8ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325392"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a>CBaseControlVideo. SetDefaultDestinationPosition, metodo

Il `SetDefaultDestinationPosition` metodo imposta di nuovo il renderer sull'utilizzo della posizione di destinazione predefinita (in genere l'intera area client della finestra).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.



| Codice restituito                                                                                           | Descrizione                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ non riescono**</dt> </dl>                | Esito negativo.<br/>                                                              |
| <dl> <dt>**NOERROR**</dt> </dl>                | Esito positivo.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Impossibile eseguire l'operazione perché i pin non sono connessi.<br/> |



 

## <a name="remarks"></a>Commenti

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

 

 




