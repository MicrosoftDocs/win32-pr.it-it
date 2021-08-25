---
description: La funzione DisplayType invia informazioni su un tipo di supporto al percorso di output di debug. Ignorato nelle build di vendita al dettaglio.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Funzione DisplayType (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a48bc5f4afbfabc9bdc37ff2cfe8c5890629f3fcaacf135979b82523981ed66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906501"
---
# <a name="displaytype-function"></a>Funzione DisplayType

La `DisplayType` funzione invia informazioni su un tipo di supporto al percorso di output di debug. Ignorato nelle build di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*label* 
</dt> <dd>

Stringa contenente un messaggio da visualizzare con le informazioni sul tipo di supporto.

</dd> <dt>

*pmtIn* 
</dt> <dd>

ointer alla [**struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che contiene il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione genera diversi messaggi LOG \_ TRACE. Al livello di registrazione 2 o superiore, la funzione visualizza il tipo principale, il sottotipo e il tipo di formato e i dati del blocco di formato. Al livello di registrazione 5 o superiore, la funzione visualizza informazioni aggiuntive, ad esempio i rettangoli di origine e di destinazione per i tipi di video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




