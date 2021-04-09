---
title: Messaggio WM_CTLCOLORBTN (winuser. h)
description: Il \_ messaggio WM CTLCOLORBTN viene inviato alla finestra padre di un pulsante prima di disegnare il pulsante. La finestra padre può modificare il testo del pulsante e i colori di sfondo. Tuttavia, solo i pulsanti creati dal proprietario rispondono alla finestra padre che elabora questo messaggio.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- Controlli di Windows Message WM_CTLCOLORBTN
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
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963749"
---
# <a name="wm_ctlcolorbtn-message"></a>\_Messaggio CTLCOLORBTN WM

Il messaggio **WM \_ CTLCOLORBTN** viene inviato alla finestra padre di un pulsante prima di disegnare il pulsante. La finestra padre può modificare il testo del pulsante e i colori di sfondo. Tuttavia, solo i pulsanti creati dal proprietario rispondono alla finestra padre che elabora questo messaggio.


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**HDC** che specifica l'handle per il contesto di visualizzazione per il pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

**HWND** che specifica l'handle per il pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire un handle a un pennello. Il sistema utilizza il pennello per disegnare lo sfondo del pulsante.

## <a name="remarks"></a>Commenti

Se l'applicazione restituisce un pennello creato, ad esempio tramite la funzione [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) , l'applicazione deve liberare il pennello. Se l'applicazione restituisce un pennello di sistema, ad esempio uno recuperato dalla funzione [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) , l'applicazione non deve liberare il pennello.

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per il pulsante. [**I pulsanti con lo stile \_ BS**](button-styles.md)Button, [**BS \_ DEFPUSHBUTTON**](button-styles.md)o [**BS \_ PUSHLIKE**](button-styles.md) non utilizzano il pennello restituito. I pulsanti con questi stili vengono sempre disegnati con i colori di sistema predefiniti. Il disegno dei pulsanti di push richiede diversi pennelli: faccia, evidenziazione e ombreggiatura, ma il messaggio **WM \_ CTLCOLORBTN** consente la restituzione di un solo pennello. Per fornire un aspetto personalizzato per i pulsanti di push, utilizzare un pulsante creato dal proprietario. Per ulteriori informazioni, vedere [creazione di controlli Owner-Drawn](user-controls-intro.md).

Il messaggio **WM \_ CTLCOLORBTN** non viene mai inviato tra i thread. Viene inviato solo all'interno di un thread.

Il colore del testo di una casella di controllo o di un pulsante di opzione si applica alla casella o al pulsante, al segno di spunta e al testo. Il rettangolo di attivazione per questi pulsanti rimane il colore predefinito del sistema (in genere nero). Il colore del testo di una casella di gruppo si applica al testo ma non alla riga che definisce la casella. Il colore del testo di un pulsante di push si applica solo al relativo rettangolo di attivazione; non influisce sul colore del testo.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore. Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita. Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

