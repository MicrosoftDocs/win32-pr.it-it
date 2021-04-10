---
title: Messaggio WM_CHOOSEFONT_SETFLAGS (COMMDLG. h)
description: Un'applicazione invia il \_ \_ messaggio di flag ChooseFont di WM a una finestra di dialogo tipo di carattere per impostare le opzioni di visualizzazione per la finestra di dialogo.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Finestre di dialogo WM_CHOOSEFONT_SETFLAGS messaggio
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120571"
---
# <a name="wm_choosefont_setflags-message"></a>Messaggio di FLAG di WM \_ ChooseFont \_

Un'applicazione invia il messaggio di **\_ \_ flag ChooseFont di WM** a una finestra di dialogo **tipo di carattere** per impostare le opzioni di visualizzazione per la finestra di dialogo.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contenente nuove impostazioni nel membro dei **flag** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea una finestra di dialogo del **tipo di carattere** e usa una struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per specificare i valori iniziali per il membro dei **flag** . Utilizzare il messaggio di **\_ \_ flag ChooseFont di WM** per specificare valori diversi per il membro dei **flag** mentre è aperta la finestra di dialogo **tipo di carattere** .

In genere, è necessario inviare il messaggio di **\_ \_ flag ChooseFont di WM** da una procedura di hook di [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

