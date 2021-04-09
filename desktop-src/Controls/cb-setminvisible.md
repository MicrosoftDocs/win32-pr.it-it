---
title: Messaggio CB_SETMINVISIBLE (COMmctrl. h)
description: Un'applicazione invia un \_ messaggio SETMINVISIBLE CB per impostare il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- Controlli di Windows Message CB_SETMINVISIBLE
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
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119091"
---
# <a name="cb_setminvisible-message"></a>\_Messaggio SETMINVISIBLE CB

Un'applicazione invia un **messaggio \_ SETMINVISIBLE CB** per impostare il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il numero minimo di elementi visibili.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è **true**. In caso contrario, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Quando il numero di elementi nell'elenco a discesa è maggiore del valore minimo, la casella combinata utilizza una barra di scorrimento. Per impostazione predefinita, 30 è il numero minimo di elementi visibili.

Questo messaggio viene ignorato se il controllo casella combinata ha lo stile [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).

Per usare **CB \_ SETMINVISIBLE**, l'applicazione deve specificare comctl32.dll versione 6 nel manifesto. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ GETMINVISIBLE**](cb-getminvisible.md)
</dt> <dt>

[**\_SetMinVisible ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





