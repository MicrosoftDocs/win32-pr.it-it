---
title: Messaggio SETRGBSTRING (COMMDLG. h)
description: La procedura di hook di una finestra di dialogo colore, CCHookProc, può inviare il messaggio registrato SETRGBSTRING alla finestra di dialogo per impostare la selezione del colore corrente.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Finestre di dialogo del messaggio SETRGBSTRING
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742586"
---
# <a name="setrgbstring-message"></a>Messaggio SETRGBSTRING

La procedura di hook di una finestra di dialogo **colore** , [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), può inviare il messaggio registrato **SETRGBSTRING** alla finestra di dialogo per impostare la selezione del colore corrente.


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore RGB del colore da selezionare nella finestra di dialogo **colore** . È possibile usare la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) per specificare le intensità rossa, verde e blu di un valore di colore RGB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Se *lParam* corrisponde a uno dei colori di base o a uno dei 16 colori personalizzati, la routine della finestra di dialogo Seleziona tale colore. La routine della finestra di dialogo Aggiorna anche tutti i controlli nell'estensione di colore personalizzata della finestra di dialogo **colore** , se è aperta.

Se *lParam* non corrisponde a un colore di base o personalizzato, la procedura della finestra di dialogo non modifica la selezione di colore corrente, ma aggiorna i controlli colore personalizzati, se visibili.

## <a name="examples"></a>Esempio

Il codice di esempio seguente ottiene l'identificatore del messaggio **SETRGBSTRING** , quindi imposta la selezione del colore su blu.


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SETRGBSTRINGW** (Unicode) e **SETRGBSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

