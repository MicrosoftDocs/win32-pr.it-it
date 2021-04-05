---
title: Messaggio PGM_SETSCROLLINFO (COMmctrl. h)
description: Imposta i parametri di scorrimento del controllo pager, inclusi il valore di timeout, le righe per ogni timeout e i pixel per riga. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro SetScrollInfo di cercapersone.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- Controlli di Windows Message PGM_SETSCROLLINFO
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873654"
---
# <a name="pgm_setscrollinfo-message"></a>\_Messaggio SETSCROLLINFO PGM

\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Imposta i parametri di scorrimento del controllo pager, inclusi il valore di timeout, le righe per ogni timeout e i pixel per riga. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetScrollInfo di cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Uint** che specifica il valore di timeout per lo scorrimento, espresso in millisecondi.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un **uint** che specifica il numero di righe da scorrere per ogni timeout. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un **uint** che specifica il numero di pixel per riga.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

Il valore di timeout *wParam* controlla la velocità con cui il controllo pager genera gli eventi di scorrimento quando il controllo ha acquisito l'input del mouse e viene premuto il pulsante sinistro del mouse. I valori più piccoli generano uno scorrimento più veloce; i valori maggiori comportano uno scorrimento più lento. Il valore predefinito è un ottavo dell'ora di doppio clic. Per ulteriori informazioni, vedere [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).

Per impostazione predefinita, con ogni evento di scorrimento il controllo pager scorre una quantità uguale all'intera larghezza o altezza del controllo, a seconda che il controllo pager abbia un orientamento orizzontale o verticale. I valori in *lParam* vengono utilizzati per eseguire l'override della quantità predefinita di scorrimento. Se vengono specificati valori diversi da zero, la quantità di scorrimento è il prodotto dei due valori (LOWORD (*lParam*) \* HIWORD (*lParam*)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Cercapersone \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

