---
description: Il metodo get \_ Caption recupera la didascalia della finestra corrente.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: CBaseControlWindow.get_Caption metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f05501adbd486eaa60e939aacfdd5896c0fbcae059673029f04fcca8aeb742a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640890"
---
# <a name="cbasecontrolwindowget_caption-method"></a>Metodo CBaseControlWindow.get \_ Caption

Il `get_Caption` metodo recupera la didascalia della finestra corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstrCaption* 
</dt> <dd>

Puntatore alla didascalia della finestra corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

La maggior parte delle finestre di primo livello in un desktop basato Windows dispone di un titolo (didascalia) associato. È possibile eseguire query su questa proprietà e impostata tramite [**l'interfaccia IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Qualsiasi didascalia impostata sarà visibile solo se alla finestra è applicato lo stile \_ WS CAPTION. In caso contrario, la didascalia può comunque essere impostata (e recuperata), anche se non sarà visibile all'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




