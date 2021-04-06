---
title: Messaggio PSM_SETTITLE (Prsht. h)
description: Imposta il titolo di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- Controlli di Windows Message PSM_SETTITLE
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963799"
---
# <a name="psm_settitle-message"></a>\_Messaggio di proprietà PSM

Imposta il titolo di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che indica se includere il prefisso "Properties per" o il suffisso "Properties" (a seconda della versione) con la stringa del titolo specificata. Se questo valore è PSH \_ PROPTITLE, viene incluso il prefisso o il suffisso.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer contenente la stringa del titolo. Se il [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) di questo parametro è **null**, la finestra delle proprietà carica la risorsa di stringa specificata in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

In una procedura guidata Aero questo messaggio può essere utilizzato per modificare dinamicamente il titolo di una pagina interna; ad esempio, quando si gestisce la notifica [ \_ seactive PSN](psn-setactive.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETTITLEW** (Unicode) e **PSM \_ setitlea** (ANSI)<br/>              |



 

