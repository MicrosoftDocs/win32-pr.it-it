---
description: Trasmettere a ogni finestra dopo un evento di modifica del tema. Esempi di eventi di modifica del tema sono l'attivazione di un tema, la disattivazione di un tema o una transizione da un tema a un altro.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: WM_THEMECHANGED messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b070cb492fa5db94acb97cd07f3de87455189d542aaaad2a51a3e0ecc6b4268d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199910"
---
# <a name="wm_themechanged-message"></a>Messaggio \_ WM THEMECHANGED

Trasmettere a ogni finestra dopo un evento di modifica del tema. Esempi di eventi di modifica del tema sono l'attivazione di un tema, la disattivazione di un tema o una transizione da un tema a un altro.


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

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Questo messaggio viene inviato dal sistema operativo. Le applicazioni in genere non inviano questo messaggio.

 

I temi sono specifiche per l'aspetto dei controlli, in modo che l'elemento visivo di un controllo sia trattato separatamente dalla relativa funzionalità.

Per rilasciare un handle del tema esistente, [**chiamare CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata). Per acquisire un nuovo handle del tema, [**usare OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).

Dopo la **trasmissione WM \_ THEMECHANGED,** tutti gli handle del tema esistenti non sono validi. Una finestra in grado di riconoscere il tema deve rilasciare e riaprire uno degli handle di tema preesistenti quando riceve il **messaggio WM \_ THEMECHANGED.** Se la [**funzione OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) restituisce **NULL,** la finestra deve disegnare senzathemed.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



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

 

 
