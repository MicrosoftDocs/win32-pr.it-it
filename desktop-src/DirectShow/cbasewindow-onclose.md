---
description: Il metodo OnClose gestisce i messaggi WM \_ CLOSE.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Metodo CBaseWindow.OnClose (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 880e82ca527972b5074ac290fda34ad1c7868a33cbbe1cad12885b56720cef99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635141"
---
# <a name="cbasewindowonclose-method"></a>Metodo CBaseWindow.OnClose

Il `OnClose` metodo gestisce i messaggi WM \_ CLOSE.

## <a name="syntax"></a>Sintassi


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE.**

## <a name="remarks"></a>Commenti

Nella classe di base questo metodo nasconde semplicemente la finestra. In genere, una classe derivata eseguirà l'override di questo metodo in modo che invii anche un evento [**\_ EC USERABORT.**](ec-userabort.md) Non eseguire l'override del metodo per eliminare la finestra. Chiamare invece il [**metodo CBaseWindow::D oneWithWindow**](cbasewindow-donewithwindow.md) quando il filtro proprietario viene eliminato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




