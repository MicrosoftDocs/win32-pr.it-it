---
description: Trasmette a ogni finestra dopo un evento di modifica del tema. Esempi di eventi di modifica del tema sono l'attivazione di un tema, la disattivazione di un tema o una transizione da un tema a un altro.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: Messaggio WM_THEMECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751199"
---
# <a name="wm_themechanged-message"></a>\_Messaggio THEMECHANGED WM

Trasmette a ogni finestra dopo un evento di modifica del tema. Esempi di eventi di modifica del tema sono l'attivazione di un tema, la disattivazione di un tema o una transizione da un tema a un altro.


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro è riservato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro è riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Questo messaggio viene pubblicato dal sistema operativo. Le applicazioni in genere non inviano questo messaggio.

 

I temi sono specifiche per l'aspetto dei controlli, in modo che l'elemento visivo di un controllo venga trattato separatamente dalla relativa funzionalità.

Per rilasciare un handle del tema esistente, chiamare [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata). Per acquisire un nuovo handle del tema, usare [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).

Dopo la trasmissione **WM \_ THEMECHANGED** , gli eventuali handle di tema esistenti non sono validi. Una finestra sensibile al tema deve rilasciare e riaprire i relativi handle di tema preesistenti quando riceve il messaggio **\_ THEMECHANGED WM** . Se la funzione [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) restituisce **null**, la finestra deve disegnare senza tema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[**IsThemeActive**](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
