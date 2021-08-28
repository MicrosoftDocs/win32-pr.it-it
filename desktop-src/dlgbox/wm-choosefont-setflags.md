---
title: WM_CHOOSEFONT_SETFLAGS messaggio (Commdlg.h)
description: Un'applicazione invia il \_ messaggio WM CHOOSEFONT SETFLAGS a una finestra di dialogo Tipo di carattere per impostare le opzioni di \_ visualizzazione per la finestra di dialogo.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- WM_CHOOSEFONT_SETFLAGS finestre di dialogo del messaggio
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
ms.openlocfilehash: 0d77290dfb3668e24d3586cf6d742b524e05fb07979de7c8d45f39998aca9708
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726081"
---
# <a name="wm_choosefont_setflags-message"></a>Messaggio \_ WM CHOOSEFONT \_ SETFLAGS

Un'applicazione invia il **\_ messaggio WM CHOOSEFONT \_ SETFLAGS** **a** una finestra di dialogo Tipo di carattere per impostare le opzioni di visualizzazione per la finestra di dialogo.


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

Puntatore a una [**struttura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) che contiene nuove impostazioni nel **membro Flags.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

La [**funzione ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea una **finestra di** dialogo Tipo di carattere e usa una [**struttura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per specificare i valori iniziali per il **membro Flags.** Usare il **messaggio WM \_ CHOOSEFONT \_ SETFLAGS** per specificare valori diversi per il membro **Flags** mentre la finestra **di** dialogo Tipo di carattere è aperta.

In genere, è consigliabile inviare **il \_ messaggio WM CHOOSEFONT \_ SETFLAGS** da una procedura hook [**CFHookProc.**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |



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

[Libreria di finestre di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

