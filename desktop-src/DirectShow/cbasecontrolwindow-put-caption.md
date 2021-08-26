---
description: Il metodo put \_ Caption imposta il titolo o la didascalia della finestra.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: CBaseControlWindow.put_Caption metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c7f0c9da5ad2c3ae409e14a1ca9918a0c1aa7ef04615ab4d647ce1a3467c7311
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983701"
---
# <a name="cbasecontrolwindowput_caption-method"></a>Metodo CBaseControlWindow.put \_ Caption

Il `put_Caption` metodo imposta il titolo o la didascalia della finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strCaption* 
</dt> <dd>

Nuova didascalia della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La maggior parte delle finestre di primo livello in Windows desktop basato su Windows è associata a un titolo (didascalia). È possibile eseguire query su questa proprietà e impostata tramite [**l'interfaccia IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Qualsiasi didascalia impostata sarà visibile solo se alla finestra è applicato lo stile WS \_ CAPTION. In caso contrario, la didascalia può comunque essere impostata (e recuperata), anche se non sarà visibile all'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




