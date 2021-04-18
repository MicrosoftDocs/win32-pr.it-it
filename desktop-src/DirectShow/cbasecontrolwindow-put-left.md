---
description: Il \_ metodo Put left Imposta la coordinata sinistra per la finestra.
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: Metodo CBaseControlWindow.put_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1dcd56bc10e60d263ce385246a6ea01aee721bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331944"
---
# <a name="cbasecontrolwindowput_left-method"></a>Metodo Left di CBaseControlWindow. put \_

Il `put_Left` metodo imposta la coordinata sinistra per la finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sinistra* 
</dt> <dd>

Nuova coordinata sinistra, espressa in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

La finestra è posizionata sul desktop. Questo è espresso in pixel da quattro coordinate, a sinistra, in alto, a destra e in basso. Le interfacce automatizzate da OLE generalmente esprimono questa posizione attraverso Left, top, Width e Height. si tratta della convenzione usata in DirectShow. Tutte le coordinate sono espresse in pixel e la modifica di tutte le coordinate aggiornerà immediatamente la finestra.

L'impostazione delle coordinate di sinistra o superiore sposta la finestra verso sinistra o verso l'alto rispettivamente; Queste coordinate non hanno alcun effetto sulla larghezza e sull'altezza della finestra. Analogamente, l'impostazione della larghezza e dell'altezza non influisce sulle coordinate di sinistra e di primo livello.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




