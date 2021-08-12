---
description: Il metodo GetSourcePosition recupera la posizione e le dimensioni del rettangolo di origine in un'unica operazione atomica.
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: Metodo CBaseControlVideo.GetSourcePosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ed52109284d9c9f8aa7884f4a0e361ec1a8f5564d0a22ae7fbf528d35a5e6ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661075"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a>Metodo CBaseControlVideo.GetSourcePosition

Il `GetSourcePosition` metodo recupera la posizione e le dimensioni del rettangolo di origine in un'operazione atomica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSourcePosition(
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

Puntatore alla coordinata sinistra del rettangolo di origine.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntatore alla coordinata superiore del rettangolo di origine.

</dd> <dt>

*pWidth* 
</dt> <dd>

Puntatore alla larghezza del rettangolo di origine.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntatore all'altezza del rettangolo di origine.

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

 

 




