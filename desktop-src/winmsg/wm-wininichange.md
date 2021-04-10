---
description: Un'applicazione invia il \_ messaggio WM WININICHANGE a tutte le finestre di primo livello dopo avere apportato una modifica al file di WIN.INI. La funzione SystemParametersInfo Invia questo messaggio dopo che un'applicazione usa la funzione per modificare un'impostazione in WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Messaggio WM_WININICHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966645"
---
# <a name="wm_wininichange-message"></a>\_Messaggio WININICHANGE WM

Un'applicazione invia il messaggio **WM \_ WININICHANGE** a tutte le finestre di primo livello dopo avere apportato una modifica al file di WIN.INI. La funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) Invia questo messaggio dopo che un'applicazione usa la funzione per modificare un'impostazione in WIN.INI.

> [!Note]  
> Il messaggio **WM \_ WININICHANGE** viene fornito solo per la compatibilità con le versioni precedenti del sistema. Le applicazioni devono usare il messaggio [**WM \_ SETTINGCHANGE**](wm-settingchange.md) .

 

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Puntatore a una stringa contenente il nome del parametro di sistema che è stato modificato. Questa stringa, ad esempio, può essere il nome di una chiave del registro di sistema o il nome di una sezione nel file di Win.ini. Questo parametro non è particolarmente utile per determinare quale parametro di sistema è stato modificato. Ad esempio, quando la stringa è un nome del registro di sistema, in genere indica solo il nodo foglia nel registro di sistema, non l'intero percorso. Inoltre, alcune applicazioni inviano questo messaggio con *lParam* impostato su **null**. In generale, quando si riceve questo messaggio, è necessario controllare e ricaricare le impostazioni dei parametri di sistema utilizzate dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se si elabora questo messaggio, restituire zero.

## <a name="remarks"></a>Commenti

Per inviare il **messaggio \_ WM WININICHANGE** a tutte le finestre di primo livello, utilizzare la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con il parametro *HWND* impostato su **HWND \_ broadcast**.

In alternativa, è possibile eseguire il mapping delle chiamate a funzioni che cambiano WIN.INI al registro di sistema. Questo mapping si verifica quando WIN.INI e la sezione da modificare vengono specificati nel registro di sistema con la seguente chiave:

**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**

La modifica nel percorso di archiviazione non ha alcun effetto sul comportamento di questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
