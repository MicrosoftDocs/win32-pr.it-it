---
description: Un'applicazione invia il messaggio WM WININICHANGE a tutte le finestre di primo livello dopo aver apportato una modifica \_ WIN.INI file. La funzione SystemParametersInfo invia questo messaggio dopo che un'applicazione usa la funzione per modificare un'impostazione in WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: WM_WININICHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cfdfeff65c1580f0bd8373fdc5ef1eec409233a9624934ea67ba835ddf805e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810461"
---
# <a name="wm_wininichange-message"></a>Messaggio \_ WM WININICHANGE

Un'applicazione invia **il messaggio WM \_ WININICHANGE** a tutte le finestre di primo livello dopo aver apportato una modifica al file WIN.INI file. La [**funzione SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) invia questo messaggio dopo che un'applicazione usa la funzione per modificare un'impostazione in WIN.INI.

> [!Note]  
> Il **messaggio WM \_ WININICHANGE** viene fornito solo per garantire la compatibilità con le versioni precedenti del sistema. Le applicazioni devono usare il [**messaggio WM \_ SETTINGCHANGE.**](wm-settingchange.md)

 

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa contenente il nome del parametro di sistema modificato. Ad esempio, questa stringa può essere il nome di una chiave del Registro di sistema o il nome di una sezione nel file Win.ini file. Questo parametro non è particolarmente utile per determinare quale parametro di sistema è stato modificato. Ad esempio, quando la stringa è un nome del Registro di sistema, indica in genere solo il nodo foglia nel Registro di sistema, non l'intero percorso. Inoltre, alcune applicazioni inviano questo messaggio con *lParam* impostato su **NULL.** In generale, quando si riceve questo messaggio, è necessario controllare e ricaricare le impostazioni dei parametri di sistema usate dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se si elabora questo messaggio, restituire zero.

## <a name="remarks"></a>Commenti

Per inviare **il messaggio WM \_ WININICHANGE** a tutte le finestre di primo livello, usare la [**funzione SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con il parametro *hWnd* impostato su **HWND \_ BROADCAST**.

Le chiamate alle funzioni che WIN.INI possono essere mappate al Registro di sistema. Questo mapping si verifica quando WIN.INI e la sezione da modificare vengono specificate nel Registro di sistema nella chiave seguente:

**HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ IniFileMapping**

La modifica nel percorso di archiviazione non ha alcun effetto sul comportamento di questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
