---
title: CB_SETMINVISIBLE messaggio (Commctrl.h)
description: Un'applicazione invia un messaggio CB SETMINVISIBLE per impostare il numero minimo di elementi visibili nell'elenco \_ a discesa di una casella combinata.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9790c43141ef836c1dec86304f260b0490854b593b7005b594d2a718332296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063321"
---
# <a name="cb_setminvisible-message"></a>CB \_ SETMINVISIBLE message

Un'applicazione invia un **messaggio \_ CB SETMINVISIBLE** per impostare il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il numero minimo di elementi visibili.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è **TRUE.** In caso contrario, il valore restituito **è FALSE.**

## <a name="remarks"></a>Commenti

Quando il numero di elementi nell'elenco a discesa è maggiore del minimo, la casella combinata usa una barra di scorrimento. Per impostazione predefinita, 30 è il numero minimo di elementi visibili.

Questo messaggio viene ignorato se il controllo casella combinata ha lo stile [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).

Per usare **CB \_ SETMINVISIBLE,** l'applicazione deve specificare comctl32.dll versione 6 nel manifesto. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ GETMINVISIBLE**](cb-getminvisible.md)
</dt> <dt>

[**ComboBox \_ SetMinVisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





