---
description: Il metodo put Owner imposta la finestra padre della finestra video. La finestra padre inoltra quindi \_ determinati messaggi alla finestra video.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: CBaseControlWindow.put_Owner metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f33e0c26506faea93afc11f51aaba13007c443fc011839efafce436fe9f2b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635893"
---
# <a name="cbasecontrolwindowput_owner-method"></a>Metodo CBaseControlWindow.put \_ Owner

Il metodo imposta la finestra padre della finestra video. La finestra padre inoltra quindi `put_Owner` determinati messaggi alla finestra video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietario* 
</dt> <dd>

Handle per la finestra padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR.

## <a name="remarks"></a>Commenti

Internamente, questo metodo chiama la funzione **SetParent** di Microsoft Win32 per impostare il nuovo proprietario e imposta lo stile della finestra padre su WS \_ CHILD. La finestra padre inoltra quindi determinati set di messaggi (in particolare, i messaggi del mouse e della tastiera) alla finestra video.

Dopo aver impostato il proprietario della finestra video, è necessario impostare il proprietario su **NULL** e lo stile della finestra del proprietario su WS OVERLAPPED e WS CLIPCHILDREN prima di rilasciare il grafico \_ \_ dei filtri. Quando si imposta il proprietario su **NULL,** questo metodo disattiva il bit WS CHILD della finestra \_ padre. Se non si imposta il proprietario su **NULL,** la finestra padre continuerà a passare messaggi alla finestra video e probabilmente si verificheranno errori alla chiusura dell'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




