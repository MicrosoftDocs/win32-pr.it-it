---
title: Messaggio TB_LOADIMAGES (COMmctrl. h)
description: Carica le immagini dei pulsanti definite dal sistema nell'elenco immagini di un controllo Toolbar.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- Controlli di Windows Message TB_LOADIMAGES
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478089"
---
# <a name="tb_loadimages-message"></a>TB \_ LOADIMAGES messaggio

Carica le immagini dei pulsanti definite dal sistema nell'elenco immagini di un controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di un elenco di immagini di un pulsante definito dal sistema. Questo parametro può essere impostato su uno dei valori seguenti.



| Valore                                                                                                                                                                                | Significato                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**\_colore di \_ grandi dimensioni \_ di IDB**</dt> </dl> | Bitmap di Esplora risorse di grandi dimensioni.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**colore di un \_ piccolo cron di IDB \_ \_**</dt> </dl> | Bitmap di Esplora risorse di dimensioni ridotte.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**\_ \_ colore large standard \_ IDB**</dt> </dl>    | Bitmap standard di grandi dimensioni.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**\_ \_ piccolo colore STD \_ IDB**</dt> </dl>    | Bitmap standard in dimensioni ridotte.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**\_visualizzazione IDB \_ - \_ colore grande**</dt> </dl> | Visualizza le bitmap in grandi dimensioni.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**\_ \_ colore piccolo visualizzazione \_ IDB**</dt> </dl> | Visualizzare bitmap di dimensioni ridotte.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**normale di IDB \_ \_**</dt> </dl>                 | Pulsanti di spostamento di Esplora risorse e bitmap preferiti nello stato normale.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**accesso frequente \_ a IDB \_**</dt> </dl>                          | Pulsanti di spostamento di Esplora risorse e bitmap preferiti nello stato attivo.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**IDB \_ è \_ disabilitato**</dt> </dl>           | Pulsanti di spostamento di Esplora risorse e bitmap preferiti nello stato disabilitato.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**stato di IDB \_ \_ premuto**</dt> </dl>              | Pulsanti di spostamento di Esplora risorse e bitmap preferiti nello stato premuto.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle di istanza. Questo parametro deve essere impostato su HINST \_ COMmctrl.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Numero di immagini nell'elenco immagini. Restituisce zero se la barra degli strumenti non dispone di un elenco di immagini o se l'elenco di immagini esistente è vuoto.

## <a name="remarks"></a>Commenti

Quando si preparano le strutture [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) prima di inviare il messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) , è necessario usare i valori di indice immagine appropriati. Per un elenco dei valori di indice immagine per le bitmap predefinite, vedere [valori di indice dell'immagine del pulsante standard della barra degli strumenti](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Esempio

Il codice di esempio seguente carica le immagini a colori standard di sistema Small.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ ADDBITMAP**](tb-addbitmap.md)
</dt> </dl>

 

 





