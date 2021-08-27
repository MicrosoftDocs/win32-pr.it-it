---
description: Il metodo SetDefaultSourcePosition imposta di nuovo il renderer su usando la posizione di origine predefinita (in genere tutto il video nativo).
ms.assetid: 1ac03298-4c25-45f7-9719-ea03fe4699b2
title: Metodo CBaseControlVideo.SetDefaultSourcePosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab067e9041a937c37e0df2bf9998dd1ecb7a6d1d434a4f10e1b2e1e1b50e6f75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087491"
---
# <a name="cbasecontrolvideosetdefaultsourceposition-method"></a>Metodo CBaseControlVideo.SetDefaultSourcePosition

Il `SetDefaultSourcePosition` metodo imposta nuovamente il renderer su usando la posizione di origine predefinita (in genere tutto il video nativo).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefaultSourcePosition();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione. può essere uno dei valori seguenti o altri valori non elencati.



| Codice restituito                                                                                           | Descrizione                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Esito negativo.<br/>                                                              |
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

 

 




