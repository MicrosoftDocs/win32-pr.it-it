---
title: WM_CHOOSEFONT_SETLOGFONT messaggio (Commdlg.h)
description: Un'applicazione invia il messaggio WM CHOOSEFONT SETLOGFONT a una finestra di dialogo Tipo di \_ carattere per impostare le informazioni sul tipo di carattere logico \_ corrente.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- WM_CHOOSEFONT_SETLOGFONT finestre di dialogo del messaggio
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
ms.openlocfilehash: 1d35c6f54679389b411417e5539382fd322c0873e6dba87fc90efb93b8be7ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503424"
---
# <a name="wm_choosefont_setlogfont-message"></a>Messaggio \_ WM CHOOSEFONT \_ SETLOGFONT

Un'applicazione invia il **messaggio \_ WM CHOOSEFONT \_ SETLOGFONT** a una finestra di dialogo **Tipo** di carattere per impostare le informazioni sul tipo di carattere logico corrente.


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

Puntatore a una [**struttura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che contiene informazioni sul tipo di carattere logico corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Quando si chiama la funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per creare una finestra di dialogo **Tipo** di carattere, è possibile usare il membro **lpLogFont** della struttura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per specificare una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) contenente i valori iniziali per la finestra di dialogo. Usare il **messaggio WM \_ CHOOSEFONT \_ SETLOGFONT** per specificare una **struttura LOGFONT** con valori diversi mentre **la** finestra di dialogo Tipo di carattere è aperta.

In genere, si invia il messaggio **WM \_ CHOOSEFONT \_ SETLOGFONT** da una procedura hook [**CFHookProc.**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) La routine hook può anche inviare i [**messaggi WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) e [**WM \_ CHOOSEFONT \_ SETFLAGS.**](wm-choosefont-setflags.md)

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

[**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comune](common-dialog-box-library.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

