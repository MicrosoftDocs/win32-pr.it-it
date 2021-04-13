---
description: Deprecato. L'oggetto PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica in seguito alla modifica dell'oggetto PenInputPanel tra layout.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel. PanelChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347871"
---
# <a name="peninputpanelpanelchanged-event"></a>PenInputPanel. PanelChanged, evento

Deprecato. L'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).

Si verifica in seguito alla modifica dell'oggetto [**PenInputPanel**](peninputpanel-class.md) tra layout.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewPanelType* \[ in\]
</dt> <dd>

Nuovo tipo di pannello usato per l'input all'interno dell'oggetto [**PenInputPanel**](peninputpanel-class.md) , dopo l'attivazione dell'evento **PanelChanged** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Quando si crea un oggetto [**PenInputPanel**](peninputpanel-class.md) , la [**grafia**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) è il **PanelType** predefinito. Se si modifica il pannello impostando la proprietà [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) prima che il pannello input penna diventi attivo per la prima volta, si verifica un evento **PanelChanged** .

L'evento **PanelChanged** non viene generato quando l'utente cambia tra i pad di scrittura riga e boxed.

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

 

 
