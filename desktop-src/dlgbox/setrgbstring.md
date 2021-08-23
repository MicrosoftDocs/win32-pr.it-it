---
title: Messaggio SETRGBSTRING (Commdlg.h)
description: La procedura hook di una finestra di dialogo Colore, CCHookProc, può inviare il messaggio registrato SETRGBSTRING alla finestra di dialogo per impostare la selezione del colore corrente.
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
ms.openlocfilehash: 8322bb07300ce188684f5097232563e80721fadf0f614c24ac5f7b2d034c1fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985311"
---
# <a name="setrgbstring-message"></a>Messaggio SETRGBSTRING

La routine hook di **una** finestra di dialogo Colore, [*CCHookProc,*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)può inviare il messaggio **registrato SETRGBSTRING** alla finestra di dialogo per impostare la selezione del colore corrente.


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

Valore RGB del colore da selezionare nella finestra **di dialogo** Colore. È possibile usare la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) per specificare le intensità rosso, verde e blu di un valore di colore RGB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Se *lParam corrisponde* a uno dei colori di base o a uno dei 16 colori personalizzati, la procedura della finestra di dialogo seleziona tale colore. La procedura della finestra di dialogo aggiorna anche  tutti i controlli nell'estensione colore personalizzata della finestra di dialogo Colore, se aperta.

Se *lParam* non corrisponde a un colore di base o personalizzato, la procedura della finestra di dialogo non modifica la selezione del colore corrente, ma aggiorna i controlli colore personalizzati, se sono visibili.

## <a name="examples"></a>Esempio

Il codice di esempio seguente ottiene **l'identificatore del messaggio SETRGBSTRING** e quindi imposta la selezione dei colori su blu.


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
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |
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

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> </dl>

 

