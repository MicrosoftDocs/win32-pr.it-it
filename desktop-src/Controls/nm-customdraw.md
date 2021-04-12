---
title: Codice di notifica NM_CUSTOMDRAW (COMmctrl. h)
description: Notifica alla finestra padre di un controllo informazioni sulle operazioni di disegno personalizzate. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- Controlli di Windows per il codice di notifica NM_CUSTOMDRAW
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475155"
---
# <a name="nm_customdraw-notification-code"></a>\_Codice di notifica CUSTOMDRAW Nm

Notifica alla finestra padre di un controllo informazioni sulle operazioni di disegno personalizzate. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura personalizzata correlata al disegno che contiene informazioni sull'operazione di disegno. Nell'elenco seguente vengono specificati i controlli e le relative strutture associate.



| Control                     | Struttura di progetto personalizzata                    |
|-----------------------------|------------------------------------------|
| Rebar, TrackBar e header | [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| Visualizzazione elenco                   | [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| Descrizione comando                     | [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| Visualizzazione struttura                   | [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| Barra degli strumenti                     | [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_DODEFAULT CDRF**</dt> </dl>         | Il controllo viene disegnato automaticamente. Non invierà altri codici di notifica [ \_ CUSTOMDRAW di Nm](nm-customdraw.md) per questo ciclo di disegno. Questo flag non può essere usato con altri flag. <br/>                                                                                                                                                                                                                                 |
| <dl> <dt>**\_DOERASE CDRF**</dt> </dl>           | Il controllo trarrà solo lo sfondo.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**\_NEWFONT CDRF**</dt> </dl>           | L'applicazione ha specificato un nuovo tipo di carattere per l'elemento. il controllo utilizzerà il nuovo tipo di carattere. Per ulteriori informazioni sulla modifica dei tipi di carattere, vedere [modifica di tipi di carattere e colori](custom-draw.md). Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**\_NOTIFYITEMDRAW CDRF**</dt> </dl>    | Il controllo invierà una notifica all'elemento padre di tutte le operazioni di disegno relative agli elementi. Invierà i codici di notifica di [ \_ CUSTOMDRAW](nm-customdraw.md) prima e dopo il disegno degli elementi. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_NOTIFYPOSTERASE CDRF**</dt> </dl>   | Il controllo invierà una notifica al padre dopo la cancellazione di un elemento. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**\_NOTIFYPOSTPAINT CDRF**</dt> </dl>   | Il controllo invierà un codice di notifica [ \_ CUSTOMDRAW Nm](nm-customdraw.md) quando il ciclo di disegno per l'intero controllo è completo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**\_NOTIFYSUBITEMDRAW CDRF**</dt> </dl> | L'applicazione riceverà un codice di notifica [nm \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** impostato su CDDS \_ ITEMPREPAINT \| CDDS \_ sottoelemento prima che ogni elemento secondario di visualizzazione elenco venga disegnato. È quindi possibile specificare il tipo di carattere e il colore per ogni elemento secondario separatamente oppure restituire [**CDRF \_ DODEFAULT**](cdrf-constants.md) per l'elaborazione predefinita. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**\_SKIPDEFAULT CDRF**</dt> </dl>       | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questo errore si verifica quando **dwDrawStage** è uguale a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_SKIPPOSTPAINT CDRF**</dt> </dl>     | Il controllo non trarrà il rettangolo di attivazione intorno a un elemento.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Commenti

Attualmente, i controlli seguenti supportano la funzionalità di estrazione personalizzata: intestazione, visualizzazione elenco, Rebar, barra degli strumenti, descrizione comando, TrackBar e visualizzazione albero. Il progetto personalizzato è supportato anche per i controlli pulsante se si dispone di un manifesto dell'applicazione per assicurarsi che sia disponibile Comctl32.dll versione 6.

Se questo messaggio viene gestito in una procedura di dialogo, è necessario impostare il valore restituito come parte dei dati della finestra prima di restituire **true**. Per ulteriori informazioni, vedere [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Progetto personalizzato](custom-draw.md)
</dt> </dl>

 

