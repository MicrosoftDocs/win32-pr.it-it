---
description: Deprecato. PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando l'oggetto PenInputPanel è in movimento.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Evento PenInputPanel.PanelMoving (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4a152afdef9fcd10fb92fdec55d9a460faf58ca91536e96c9876203fbad44c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596600"
---
# <a name="peninputpanelpanelmoving-event"></a>Evento PenInputPanel.PanelMoving

Deprecato. [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal pannello [di input di testo (TIP).](text-input-panel-reference.md)

Si verifica quando [**l'oggetto PenInputPanel**](peninputpanel-class.md) è in movimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*A sinistra* \[ in, out\]
</dt> <dd>

Nuova posizione orizzontale, o asse x, del bordo sinistro dell'oggetto [**PenInputPanel,**](peninputpanel-class.md) nelle coordinate dello schermo.

</dd> <dt>

*In alto* \[ in, out\]
</dt> <dd>

Nuova posizione verticale, o asse y, del bordo sinistro dell'oggetto [**PenInputPanel,**](peninputpanel-class.md) nelle coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

**L'evento PanelMoving** è progettato per essere usato per modificare la posizione del pannello di input penna modificando i *parametri Left* *e Top.*

I [**metodi MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) [**e Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) provocano la chiamata del codice di posizionamento automatico dell'oggetto [**PenInputPanel**](peninputpanel-class.md) che attiva un evento **PanelMoving.** Di conseguenza, la chiamata di questi metodi **all'interno di un gestore PanelMoving** può comportare un ciclo infinito ricorsivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Peninputpanel**](peninputpanel-class.md)
</dt> </dl>

 

 




