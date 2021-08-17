---
title: WM_CTLCOLORBTN messaggio (Winuser.h)
description: Il messaggio WM \_ CTLCOLORBTN viene inviato alla finestra padre di un pulsante prima di disegnare il pulsante. La finestra padre può modificare il testo e i colori di sfondo del pulsante. Tuttavia, solo i pulsanti disegnati dal proprietario rispondono alla finestra padre che elabora questo messaggio.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN di controllo Windows messaggio
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5689d7c76499f1ed180f76831af325c5e311bf06e052ea1446805c39ddf8642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407640"
---
# <a name="wm_ctlcolorbtn-message"></a>Messaggio \_ WM CTLCOLORBTN

Il **messaggio WM \_ CTLCOLORBTN** viene inviato alla finestra padre di un pulsante prima di disegnare il pulsante. La finestra padre può modificare il testo e i colori di sfondo del pulsante. Tuttavia, solo i pulsanti disegnati dal proprietario rispondono alla finestra padre che elabora questo messaggio.


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Oggetto **HDC** che specifica l'handle per il contesto di visualizzazione per il pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

**HWND che** specifica l'handle per il pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire un handle a un pennello. Il sistema usa il pennello per disegnare lo sfondo del pulsante.

## <a name="remarks"></a>Commenti

Se l'applicazione restituisce un pennello creato ,ad esempio usando la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect,**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) l'applicazione deve liberare il pennello. Se l'applicazione restituisce un pennello di sistema,ad esempio un pennello recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush,**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) non è necessario liberare il pennello.

Per impostazione predefinita, [**la funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il pulsante. I pulsanti con [**gli stili \_ BS PUSHBUTTON**](button-styles.md), [**BS \_ DEFPUSHBUTTON**](button-styles.md)o [**BS \_ PUSHLIKE**](button-styles.md) non usano il pennello restituito. I pulsanti con questi stili vengono sempre disegnati con i colori di sistema predefiniti. Il disegno di pulsanti di push richiede diversi pennelli: viso, evidenziazione e ombreggiatura, ma il messaggio **WM \_ CTLCOLORBTN** consente di restituire un solo pennello. Per fornire un aspetto personalizzato per i pulsanti di push, usare un pulsante disegnato dal proprietario. Per altre informazioni, vedere [Creating Owner-Drawn Controls](user-controls-intro.md).

Il **messaggio WM \_ CTLCOLORBTN** non viene mai inviato tra thread. Viene inviato solo all'interno di un thread.

Il colore del testo di una casella di controllo o di un pulsante di opzione si applica alla casella o al pulsante, al segno di spunta e al testo. Il rettangolo di attivazione per questi pulsanti rimane il colore predefinito del sistema (in genere nero). Il colore del testo di una casella di gruppo si applica al testo, ma non alla riga che la definisce. Il colore del testo di un pulsante di pressione si applica solo al relativo rettangolo di attivazione; non influisce sul colore del testo.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a **un \_ int PTR** e restituire direttamente il valore. Se la routine della finestra di dialogo **restituisce FALSE,** viene eseguita la gestione dei messaggi predefinita. Il valore MSGRESULT DWL \_ impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelezionarePalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

