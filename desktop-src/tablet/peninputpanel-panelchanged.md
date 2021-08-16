---
description: Deprecato. PenInputPanel è stato sostituito dal pannello input di testo (TIP). Si verifica quando l'oggetto PenInputPanel cambia da un layout all'altro.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel.PanelChanged (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f722609ae71761a2a2a05c743aba7bfd83b7d4ff8689333bf2093d4dc21345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856520"
---
# <a name="peninputpanelpanelchanged-event"></a>Evento PenInputPanel.PanelChanged

Deprecato. [**PenInputPanel è**](peninputpanel-class.md) stato sostituito dal [pannello input di testo (TIP).](text-input-panel-reference.md)

Si verifica quando [**l'oggetto PenInputPanel**](peninputpanel-class.md) cambia da un layout all'altro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewPanelType* \[ Pollici\]
</dt> <dd>

Nuovo tipo di pannello usato per l'input all'interno [**dell'oggetto PenInputPanel,**](peninputpanel-class.md) dopo **l'evento PanelChanged.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Quando si crea un [**oggetto PenInputPanel,**](peninputpanel-class.md) [**la scrittura manuale**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) è l'impostazione predefinita di **PanelType.** Se si modifica il pannello impostando la proprietà [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) prima che il pannello di input penna diventi attivo per la prima volta, si verifica un evento **PanelChanged.**

**L'evento PanelChanged** non viene generato quando l'utente cambia tra i pannelli di scrittura lined e boxed.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Peninputpanel**](peninputpanel-class.md)
</dt> </dl>

 

 
