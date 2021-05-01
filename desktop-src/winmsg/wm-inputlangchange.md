---
description: Inviato alla finestra interessata in primo piano dopo la modifica della lingua di input di un'applicazione. È necessario apportare impostazioni specifiche dell'applicazione e passare il messaggio alla funzione DefWindowProc, che passa il messaggio a tutte le finestre figlio di primo livello.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: WM_INPUTLANGCHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332406"
---
# <a name="wm_inputlangchange-message"></a>Messaggio WM \_ INPUTLANGCHANGE

Inviato alla finestra interessata in primo piano dopo la modifica della lingua di input di un'applicazione. È necessario apportare impostazioni specifiche dell'applicazione e passare il messaggio alla funzione [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) che passa il messaggio a tutte le finestre figlio di primo livello. Queste finestre figlio possono passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per fare in modo che passi il messaggio alle finestre figlio e così via.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam*

</dt> <dd>
  
Tipo: **WPARAM**

Tabella [codici delle](../Intl/code-pages.md) nuove impostazioni locali.

</dd> <dt>

*lParam*

</dt> <dd>
 
Tipo: **LPARAM**

Identificatore delle impostazioni locali di input **HKL.** Per altre informazioni, vedere [Lingue, impostazioni locali e layout di tastiera.](../inputdev/about-keyboard-input.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire un valore diverso da zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

È possibile recuperare il nome [delle impostazioni locali della](../Intl/locale-names.md) tastiera tramite la funzione [LCIDToLocaleName.](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) Con il nome delle impostazioni locali è possibile usare [le funzioni delle impostazioni locali moderne:](/windows/win32/intl/calling-the--locale-name--functions)

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |

## <a name="see-also"></a>Vedi anche

**Riferimento**

- [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [**WM \_ INPUTLANGCHANGEREQUEST**](wm-inputlangchangerequest.md)

**Informazioni concettuali**

- [Windows](windows.md) 
