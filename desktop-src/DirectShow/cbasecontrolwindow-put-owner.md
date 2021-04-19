---
description: Il \_ metodo Put Owner imposta la finestra padre della finestra video; la finestra padre quindi invia alcuni messaggi alla finestra del video.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Metodo CBaseControlWindow.put_Owner (Ctlutil. h)
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
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331940"
---
# <a name="cbasecontrolwindowput_owner-method"></a>Metodo CBaseControlWindow. put \_ Owner

Il `put_Owner` metodo imposta la finestra padre della finestra video; la finestra padre quindi invia alcuni messaggi alla finestra del video.

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

Internamente, questo metodo chiama la funzione **padre** di Microsoft Win32 per impostare il nuovo proprietario e imposta lo stile della finestra padre su WS \_ child. La finestra padre inoltrerà quindi determinati set di messaggi (in particolare, i messaggi del mouse e della tastiera) alla finestra del video.

Dopo aver impostato il proprietario della finestra video, è necessario impostare il proprietario su **null** e lo stile della finestra del proprietario su WS \_ OVERLAPPED e WS \_ CLIPCHILDREN prima di rilasciare il grafico del filtro. Quando si imposta il proprietario su **null**, questo metodo disattiva il bit figlio WS della finestra padre \_ . Se il proprietario non viene impostato su **null**, la finestra padre continuerà a passare i messaggi alla finestra video ed è probabile che si verifichino errori durante la chiusura dell'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




