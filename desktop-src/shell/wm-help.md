---
description: Indica che l'utente ha premuto il tasto F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Messaggio WM_HELP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979463"
---
# <a name="wm_help-message"></a>\_Messaggio della Guida WM

Indica che l'utente ha premuto il tasto F1. Se un menu è attivo quando si preme F1, **la \_ Guida di WM** viene inviata alla finestra associata al menu. in caso contrario, la **\_ Guida di WM** viene inviata alla finestra con lo stato attivo della tastiera. Se nessuna finestra dispone dello stato attivo della tastiera, la **\_ Guida WM** viene inviata alla finestra attualmente attiva.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lphi* 
</dt> <dd>

Indirizzo di una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) che contiene informazioni sulla voce di menu, il controllo, la finestra di dialogo o la finestra per la quale è richiesta la guida.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa **la \_ Guida WM** alla finestra padre di una finestra figlio o al proprietario di una finestra di primo livello.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 
