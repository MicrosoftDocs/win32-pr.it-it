---
description: Il metodo get \_ DestinationWidth recupera la larghezza del rettangolo di destinazione corrente.
ms.assetid: 7d466d61-1768-48b4-8460-b15d28a294f3
title: CBaseControlVideo.get_DestinationWidth metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6e228d5da753d02cee2f82844d6dbf138bf815db8d6c9ad0df99124b099285f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057151"
---
# <a name="cbasecontrolvideoget_destinationwidth-method"></a>Metodo CBaseControlVideo.get \_ DestinationWidth

Il `get_DestinationWidth` metodo recupera la larghezza del rettangolo di destinazione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DestinationWidth(
   long *pDestinationWidth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestinationWidth* 
</dt> <dd>

Puntatore alla larghezza di destinazione.

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

Questa funzione membro implementa il [**metodo IBasicVideo::get \_ DestinationWidth.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationwidth)

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

 

 




