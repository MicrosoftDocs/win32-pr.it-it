---
description: Messaggio inviato a tutte le finestre di primo livello quando la funzione SystemParametersInfo modifica un'impostazione a livello di sistema o quando le impostazioni dei criteri sono state modificate.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: WM_SETTINGCHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302f156da905263ed7f3d1d331d4dbb25af5b3e81d9df6136281c7dbc7b3914c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710041"
---
# <a name="wm_settingchange-message"></a>Messaggio \_ WM SETTINGCHANGE

Messaggio inviato a tutte le finestre di primo livello quando la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) modifica un'impostazione a livello di sistema o quando le impostazioni dei criteri sono state modificate.

Le applicazioni devono **inviare WM \_ SETTINGCHANGE** a tutte le finestre di primo livello quando apportano modifiche ai parametri di sistema. Questo messaggio non può essere inviato direttamente a una finestra. Per inviare **il messaggio WM \_ SETTINGCHANGE** a tutte le finestre di primo livello, usare la [**funzione SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con il parametro *hwnd* impostato su **HWND \_ BROADCAST.**

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Quando il sistema invia questo messaggio come risultato di una chiamata [**SystemParametersInfo,**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) il *parametro wParam* è il valore del parametro *uiAction* passato alla **funzione SystemParametersInfo.** Per un elenco di valori, vedere **SystemParametersInfo.**

Quando il sistema invia questo messaggio in seguito a una modifica nelle impostazioni dei criteri, questo parametro indica il tipo di criterio applicato. Questo valore è 1 se sono stati applicati criteri computer o zero se sono stati applicati criteri utente.

Quando il sistema invia questo messaggio in seguito a una modifica delle impostazioni locali, questo parametro è zero.

Quando un'applicazione invia questo messaggio, questo parametro deve essere **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Quando il sistema invia questo messaggio in seguito a una chiamata a [**SystemParametersInfo,**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) *lParam* è un puntatore a una stringa che indica l'area contenente il parametro di sistema modificato. Questo parametro in genere non indica quale parametro di sistema specifico è stato modificato. Si noti che alcune applicazioni inviano questo messaggio con *lParam* impostato su **NULL.** In generale, quando si riceve questo messaggio, è necessario controllare e ricaricare le impostazioni dei parametri di sistema usate dall'applicazione.

Questa stringa può essere il nome di una chiave del Registro di sistema o il nome di una sezione nel file Win.ini. Quando la stringa è un nome del Registro di sistema, in genere indica solo il nodo foglia nel Registro di sistema, non il percorso completo.

Quando il sistema invia questo messaggio in seguito a una modifica nelle impostazioni dei criteri, questo parametro punta alla stringa "Policy".

Quando il sistema invia questo messaggio in seguito a una modifica delle impostazioni locali, questo parametro punta alla stringa "intl".

Per modificare le variabili di ambiente per il sistema o l'utente, trasmettere questo messaggio con *lParam* impostato sulla stringa "Environment".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se si elabora questo messaggio, restituire zero.

## <a name="remarks"></a>Commenti

Il *parametro lParam* indica quale metrica di sistema è stata modificata, ad esempio "ConvertibleSlateMode" se l'indicatore CONVERTIBLESLATEMODE è stato attivato o "SystemDockMode" se l'indicatore DOCKED è stato attivato o disattivato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi dei criteri](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
