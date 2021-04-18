---
description: Il metodo OnReceiveMessage gestisce i messaggi della finestra.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Metodo CBaseWindow. OnReceiveMessage (Winutil. h)
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
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325761"
---
# <a name="cbasewindowonreceivemessage-method"></a>CBaseWindow. OnReceiveMessage, metodo

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

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*uMsg* 
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

-   \_chiusura WM
-   \_spostamento WM
-   \_PALETTECHANGED WM
-   \_QUERYNEWPALETTE WM
-   \_dimensioni WM
-   \_SYSCOLORCHANGE WM

Una classe derivata può eseguire l'override di questo metodo per gestire altri messaggi. La classe derivata deve chiamare il metodo della classe base per gestire tutti i messaggi ignorati dalla classe derivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




