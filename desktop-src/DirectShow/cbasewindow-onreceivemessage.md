---
description: Il metodo OnReceiveMessage gestisce i messaggi della finestra.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Metodo CBaseWindow.OnReceiveMessage (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a5dbfb84edef1f5257cfda8cae08d27b219909f47a7d88fd29580ae12e48b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657964"
---
# <a name="cbasewindowonreceivemessage-method"></a>Metodo CBaseWindow.OnReceiveMessage

Il `OnReceiveMessage` metodo gestisce i messaggi della finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Umsg* 
</dt> <dd>

Identificatore del messaggio.

</dd> <dt>

*wParam* 
</dt> <dd>

Primo parametro del messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Secondo parametro del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 se il messaggio è stato elaborato oppure 1 se il messaggio non è stato elaborato.

## <a name="remarks"></a>Commenti

La classe base gestisce i messaggi seguenti:

-   WM \_ CLOSE
-   WM \_ MOVE
-   WM \_ PALETTECHANGED
-   WM \_ QUERYNEWPALETTE
-   DIMENSIONI \_ WM
-   WM \_ SYSCOLORCHANGE

Una classe derivata può eseguire l'override di questo metodo per gestire altri messaggi. La classe derivata deve chiamare il metodo della classe base per gestire eventuali messaggi ignorati dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




