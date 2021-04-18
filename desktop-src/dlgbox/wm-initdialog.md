---
title: Messaggio WM_INITDIALOG (winuser. h)
description: Inviato alla routine della finestra di dialogo immediatamente prima della visualizzazione di una finestra di dialogo. Le routine della finestra di dialogo utilizzano in genere questo messaggio per inizializzare i controlli e per eseguire altre attività di inizializzazione che influiscono sull'aspetto della finestra di dialogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- Finestre di dialogo WM_INITDIALOG messaggio
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
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302082"
---
# <a name="wm_initdialog-message"></a>\_Messaggio INITDIALOG WM

Inviato alla routine della finestra di dialogo immediatamente prima della visualizzazione di una finestra di dialogo. Le routine della finestra di dialogo utilizzano in genere questo messaggio per inizializzare i controlli e per eseguire altre attività di inizializzazione che influiscono sull'aspetto della finestra di dialogo.


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il controllo per ricevere lo stato attivo della tastiera predefinito. Il sistema assegna lo stato attivo della tastiera predefinito solo se la routine della finestra di dialogo restituisce **true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Dati di inizializzazione aggiuntivi. Questi dati vengono passati al sistema come parametro *lParam* in una chiamata alla funzione [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)o [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) usata per creare la finestra di dialogo. Per le finestre delle proprietà, questo parametro è un puntatore alla struttura [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) usata per creare la pagina. Questo parametro è zero se viene utilizzata un'altra funzione di creazione della finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine della finestra di dialogo deve restituire **true** per indirizzare il sistema in modo da impostare lo stato attivo sulla tastiera sul controllo specificato da *wParam*. In caso contrario, deve restituire **false** per impedire che il sistema imposti lo stato attivo della tastiera predefinito.

La routine della finestra di dialogo deve restituire direttamente il valore. Il valore **DWL \_ MSGRESULT** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

## <a name="remarks"></a>Commenti

Il controllo che riceve lo stato attivo predefinito è sempre il primo controllo nella finestra di dialogo visibile, non disabilitato e con lo stile **WS \_ TABSTOP** . Quando la routine della finestra di dialogo restituisce **true**, il sistema controlla il controllo per verificare che la procedura non sia stata disabilitata. Se è stato disabilitato, il sistema imposta lo stato attivo della tastiera sul controllo successivo visibile, non disabilitato e con **WS \_ TABSTOP**.

Un'applicazione può restituire **false** solo se ha impostato lo stato attivo su uno dei controlli della finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



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

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

