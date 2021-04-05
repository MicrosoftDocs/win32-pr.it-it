---
title: Messaggio CB_GETMINVISIBLE (COMmctrl. h)
description: Ottiene il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- Controlli di Windows Message CB_GETMINVISIBLE
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873794"
---
# <a name="cb_getminvisible-message"></a>\_Messaggio GETMINVISIBLE CB

Ottiene il numero minimo di elementi visibili nell'elenco a discesa di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero minimo di elementi visibili.

## <a name="remarks"></a>Commenti

Quando il numero di elementi nell'elenco a discesa è maggiore del valore minimo, la casella combinata utilizza una barra di scorrimento.

Questo messaggio viene ignorato se il controllo casella combinata ha lo stile [**CBS \_ NOINTEGRALHEIGHT**](combo-box-styles.md).

Per usare **CB \_ GETMINVISIBLE**, l'applicazione deve specificare comctl32.dll versione 6 nel manifesto. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

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

[**CB \_ SETMINVISIBLE**](cb-setminvisible.md)
</dt> <dt>

[**\_GetMinVisible ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





