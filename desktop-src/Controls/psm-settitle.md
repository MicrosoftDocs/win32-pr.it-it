---
title: PSM_SETTITLE messaggio (Prsht.h)
description: Imposta il titolo di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet SetTitle.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE controlli di Windows messaggio
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
ms.openlocfilehash: 782d5ebf3e7fe0850b89d9f52f0dc5c406dbd41c9bdad694b41b8ae9ea4c8b0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985451"
---
# <a name="psm_settitle-message"></a>Messaggio \_ SETTITLE PSM

Imposta il titolo di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che indica se includere il prefisso "Properties for" o il suffisso "Properties" (a seconda della versione) con la stringa del titolo specificata. Se questo valore è PSH \_ PROPTITLE, viene incluso il prefisso o il suffisso.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che contiene la stringa del titolo. Se la [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) di questo parametro **è NULL,** la finestra delle proprietà carica la risorsa stringa specificata in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

In una procedura guidata Di Questo messaggio può essere usato per modificare dinamicamente il titolo di una pagina interna. ad esempio quando si gestisce la [notifica \_ PSN SETACTIVE.](psn-setactive.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETTITLEW** (Unicode) e **PSM \_ SETTITLEA** (ANSI)<br/>              |



 

