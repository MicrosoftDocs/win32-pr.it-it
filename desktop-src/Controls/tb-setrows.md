---
title: Messaggio TB_SETROWS (COMmctrl. h)
description: Imposta il numero di righe di pulsanti in una barra degli strumenti.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- Controlli di Windows Message TB_SETROWS
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048768"
---
# <a name="tb_setrows-message"></a>\_Messaggio di righe TB

Imposta il numero di righe di pulsanti in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il numero di righe richieste. Il numero minimo di righe è uno e il numero massimo di righe è uguale al numero di pulsanti nella barra degli strumenti.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un **bool** che indica se creare più righe rispetto a quelle richieste quando il sistema non è in grado di creare il numero di righe specificato da *wParam*. Se **true**, il sistema crea più righe. Se **false**, il sistema crea un minor numero di righe.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo delimitatore della barra degli strumenti dopo l'impostazione delle righe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Poiché il sistema non suddivide i gruppi di pulsanti quando si imposta il numero di righe, il numero di righe risultante potrebbe essere diverso da quello richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

