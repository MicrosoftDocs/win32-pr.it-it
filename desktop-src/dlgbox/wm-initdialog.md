---
title: WM_INITDIALOG messaggio (Winuser.h)
description: Inviato alla routine della finestra di dialogo immediatamente prima che venga visualizzata una finestra di dialogo. Le procedure della finestra di dialogo usano in genere questo messaggio per inizializzare i controlli ed eseguire qualsiasi altra attività di inizializzazione che influisce sull'aspetto della finestra di dialogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e272ac93514fb60069a9217c3100318f95b1e9a8c77d9e75af56e2e7fbfbf66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117771"
---
# <a name="wm_initdialog-message"></a>Messaggio \_ WM INITDIALOG

Inviato alla routine della finestra di dialogo immediatamente prima che venga visualizzata una finestra di dialogo. Le procedure della finestra di dialogo usano in genere questo messaggio per inizializzare i controlli ed eseguire qualsiasi altra attività di inizializzazione che influisce sull'aspetto della finestra di dialogo.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il controllo per ricevere lo stato attivo predefinito della tastiera. Il sistema assegna lo stato attivo predefinito della tastiera solo se la routine della finestra di dialogo restituisce **TRUE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Dati di inizializzazione aggiuntivi. Questi dati vengono passati al sistema come parametro *lParam* in una chiamata alla funzione [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)o [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) usata per creare la finestra di dialogo. Per le finestre delle proprietà, questo parametro è un puntatore alla [**struttura PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) usata per creare la pagina. Questo parametro è zero se viene usata qualsiasi altra funzione di creazione della finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine della finestra di dialogo deve restituire **TRUE** per indirizzare il sistema a impostare lo stato attivo della tastiera sul controllo specificato da *wParam*. In caso contrario, deve restituire **FALSE** per impedire al sistema di impostare lo stato attivo predefinito della tastiera.

La routine della finestra di dialogo deve restituire direttamente il valore . Il **valore \_ MSGRESULT DWL** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="remarks"></a>Commenti

Il controllo per ricevere lo stato attivo predefinito della tastiera è sempre il primo controllo della finestra di dialogo visibile, non disabilitato e con lo **stile \_ WS TABSTOP.** Quando la routine della finestra di dialogo restituisce **TRUE,** il sistema controlla il controllo per assicurarsi che la procedura non lo abbia disabilitato. Se è stato disabilitato, il sistema imposta lo stato attivo della tastiera sul controllo successivo visibile, non disabilitato e con **WS \_ TABSTOP**.

Un'applicazione può restituire **FALSE** solo se lo stato attivo della tastiera è stato impostato su uno dei controlli della finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[**Setfocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

