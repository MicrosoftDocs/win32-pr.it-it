---
description: Il metodo DoSetWindowForeground porta la finestra in primo piano.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Metodo CBaseWindow.DoSetWindowForeground (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f0d0dd99f5e2c5e5afffb78066a9380c56f744a4ba54b64bf987df15ea58862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658020"
---
# <a name="cbasewindowdosetwindowforeground-method"></a>Metodo CBaseWindow.DoSetWindowForeground

Il `DoSetWindowForeground` metodo porta la finestra in primo piano.

## <a name="syntax"></a>Sintassi


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bFocus* 
</dt> <dd>

Valore booleano che specifica se assegnare lo stato attivo alla finestra. Se il valore è **TRUE,** la finestra ottiene lo stato attivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




