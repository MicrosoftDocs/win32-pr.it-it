---
description: Il metodo put \_ DestinationWidth imposta la larghezza del rettangolo di destinazione.
ms.assetid: 1e7a4d38-1453-4dfd-8a2f-0f76b352fc64
title: CBaseControlVideo.put_DestinationWidth metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1762a7b86d38ffb4f8feeced3ce002f33fc434d07ed9716d3334aa25db69fe94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056821"
---
# <a name="cbasecontrolvideoput_destinationwidth-method"></a>Metodo CBaseControlVideo.put \_ DestinationWidth

Il `put_DestinationWidth` metodo imposta la larghezza del rettangolo di destinazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_DestinationWidth(
   long DestinationWidth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DestinationWidth* 
</dt> <dd>

Nuova larghezza di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione. può essere uno dei valori seguenti o altri valori non elencati.



| Codice restituito                                                                                           | Descrizione                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Esito negativo.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Argomento non valido.<br/>                                                     |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>             | Argomento del puntatore **NULL.**<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Operazione completata.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Non è possibile eseguire l'operazione perché i pin non sono connessi.<br/> |



 

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

 

 




