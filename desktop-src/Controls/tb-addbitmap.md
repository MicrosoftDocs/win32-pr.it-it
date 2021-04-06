---
title: Messaggio TB_ADDBITMAP (COMmctrl. h)
description: Aggiunge una o più immagini all'elenco di immagini dei pulsanti disponibili per una barra degli strumenti.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- Controlli di Windows Message TB_ADDBITMAP
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743970"
---
# <a name="tb_addbitmap-message"></a>TB \_ ADDBITMAP messaggio

Aggiunge una o più immagini all'elenco di immagini dei pulsanti disponibili per una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di immagini di pulsanti nella bitmap. Se *lParam* specifica una bitmap definita dal sistema, questo parametro viene ignorato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) che contiene l'identificatore di una risorsa bitmap e l'handle per l'istanza del modulo con il file eseguibile che contiene la risorsa bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della prima nuova immagine, se ha esito positivo, oppure-1 in caso contrario.

## <a name="remarks"></a>Commenti

Se la barra degli strumenti è stata creata utilizzando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , è necessario inviare il messaggio [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) alla barra degli strumenti prima di inviare **TB \_ ADDBITMAP**.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creata una bitmap da una risorsa (IDB \_ bitmap1), viene eseguito il mapping del colore di sfondo (nero in questo caso) al colore della superficie del pulsante di sistema e viene aggiunto alla barra degli strumenti.


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

