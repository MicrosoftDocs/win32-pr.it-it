---
title: Messaggio WM_CHOOSEFONT_SETLOGFONT (COMMDLG. h)
description: Un'applicazione invia il \_ messaggio WM ChooseFont \_ SETLOGFONT a una finestra di dialogo tipo di carattere per impostare le informazioni correnti sui caratteri logici.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Finestre di dialogo WM_CHOOSEFONT_SETLOGFONT messaggio
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742583"
---
# <a name="wm_choosefont_setlogfont-message"></a>\_ \_ Messaggio SETLOGFONT di WM ChooseFont

Un'applicazione invia il messaggio **WM \_ ChooseFont \_ SETLOGFONT** a una finestra di dialogo tipo di **carattere** per impostare le informazioni correnti sui caratteri logici.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene informazioni sul tipo di carattere logico corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Quando si chiama la funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per creare una finestra di dialogo del **tipo di carattere** , è possibile usare il membro **LPLOGFONT** della struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per specificare una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) contenente i valori iniziali per la finestra di dialogo. Usare il messaggio **WM \_ ChooseFont \_ SETLOGFONT** per specificare una struttura **LOGFONT** con valori diversi mentre è aperta la finestra di dialogo tipo di **carattere** .

In genere, si invia il messaggio **WM \_ ChooseFont \_ SETLOGFONT** da una procedura di hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) . La procedura hook può anche inviare i messaggi [**WM \_ ChooseFont \_ GETLOGFONT**](wm-choosefont-getlogfont.md) e [**WM \_ ChooseFont \_**](wm-choosefont-setflags.md) .

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

[**\_GETLOGFONT ChooseFont \_ WM**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**\_flag ChooseFont \_ WM**](wm-choosefont-setflags.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

