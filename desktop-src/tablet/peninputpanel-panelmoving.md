---
description: Deprecato. L'oggetto PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando l'oggetto PenInputPanel viene spostato.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Evento PenInputPanel. PanelMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319157"
---
# <a name="peninputpanelpanelmoving-event"></a>PenInputPanel. PanelMoving, evento

Deprecato. L'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).

Si verifica quando l'oggetto [**PenInputPanel**](peninputpanel-class.md) viene spostato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

A *sinistra* \[ in uscita\]
</dt> <dd>

Nuova posizione orizzontale, o asse x, del bordo sinistro dell'oggetto [**PenInputPanel**](peninputpanel-class.md) , in coordinate dello schermo.

</dd> <dt>

In *alto* \[ in uscita\]
</dt> <dd>

Nuova posizione verticale, o asse y, del bordo sinistro dell'oggetto [**PenInputPanel**](peninputpanel-class.md) , in coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'evento **PanelMoving** è progettato per essere usato per modificare la posizione del pannello input penna cambiando i parametri *Left* e *Top* .

I metodi [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) e [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) fanno sì che l'oggetto [**PenInputPanel**](peninputpanel-class.md) chiami il codice di posizionamento automatico che attiva un evento **PanelMoving** . Di conseguenza, la chiamata di questi metodi all'interno di un gestore **PanelMoving** può causare un ciclo infinito ricorsivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




