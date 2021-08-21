---
title: TB_LOADIMAGES messaggio (Commctrl.h)
description: Carica le immagini dei pulsanti definite dal sistema nell'elenco di immagini di un controllo barra degli strumenti.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES di controllo Windows messaggio
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
ms.openlocfilehash: df2cfae5e1658dec2652eb68cae4283dd0df697ad055434f1290cc0da7c2b485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168197"
---
# <a name="tb_loadimages-message"></a>TB \_ DI MESSAGGIO LOADIMAGES

Carica le immagini dei pulsanti definite dal sistema nell'elenco di immagini di un controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di un elenco di immagini di pulsante definito dal sistema. Questo parametro può essere impostato su uno dei valori seguenti.



| Valore                                                                                                                                                                                | Significato                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**IDB \_ HIST \_ LARGE \_ COLOR**</dt> </dl> | Windows Bitmap di Explorer di grandi dimensioni.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**IDB \_ HIST \_ SMALL \_ COLOR**</dt> </dl> | Windows Bitmap di Explorer di piccole dimensioni.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**IDB \_ STD \_ LARGE \_ COLOR**</dt> </dl>    | Bitmap standard di grandi dimensioni.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**IDB \_ STD \_ SMALL \_ COLOR**</dt> </dl>    | Bitmap standard di piccole dimensioni.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**IDB \_ VIEW \_ LARGE \_ COLOR**</dt> </dl> | Visualizzare bitmap di grandi dimensioni.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**IDB \_ VIEW \_ SMALL \_ COLOR**</dt> </dl> | Visualizzare bitmap di piccole dimensioni.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**IDB \_ HIST \_ NORMAL**</dt> </dl>                 | Windows Explorer sposta i pulsanti e le bitmap preferiti in stato normale.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**IDB \_ HIST \_ HOT**</dt> </dl>                          | Windows Pulsanti di spostamento di Explorer e bitmap preferiti in stato attivo.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**IDB \_ HIST \_ DISABLED**</dt> </dl>           | Windows Pulsanti di spostamento di Explorer e bitmap preferiti in stato disabilitato.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**IDB \_ HIST \_ PRESSED**</dt> </dl>              | Windows Explorer sposta i pulsanti e le bitmap preferiti nello stato premuto.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle di istanza. Questo parametro deve essere impostato su HINST \_ COMMCTRL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Numero di immagini nell'elenco di immagini. Restituisce zero se la barra degli strumenti non contiene un elenco di immagini o se l'elenco di immagini esistente è vuoto.

## <a name="remarks"></a>Commenti

È necessario usare i valori di indice delle immagini appropriati quando si preparano [**le strutture TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) prima di inviare il messaggio [**\_ ADDBUTTONS tb.**](tb-addbuttons.md) Per un elenco dei valori di indice delle immagini per queste bitmap preimpostate, vedere [Toolbar Standard Button Image Index Values](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Esempio

Il codice di esempio seguente carica le immagini a colori di piccole dimensioni standard del sistema.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ ADDBITMAP**](tb-addbitmap.md)
</dt> </dl>

 

 





