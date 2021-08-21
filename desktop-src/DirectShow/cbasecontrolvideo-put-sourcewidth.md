---
description: Il metodo put \_ SourceWidth imposta la larghezza del rettangolo di origine.
ms.assetid: 0becea4f-e47e-4f64-ab95-0ee333ad48f3
title: CBaseControlVideo.put_SourceWidth metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbc984e0baad4b2a4a287c6265df35c8d4ddccdd903e0ff79b80cc95f6cf8453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158653"
---
# <a name="cbasecontrolvideoput_sourcewidth-method"></a>Metodo SourceWidth CBaseControlVideo.put \_

Il `put_SourceWidth` metodo imposta la larghezza del rettangolo di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SourceWidth(
   long SourceWidth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SourceWidth* 
</dt> <dd>

Nuova larghezza del rettangolo di origine.

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

 

 




