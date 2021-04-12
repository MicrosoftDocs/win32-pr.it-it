---
description: Messaggio inviato a tutte le finestre di primo livello quando la funzione SystemParametersInfo modifica un'impostazione a livello di sistema o quando sono state modificate le impostazioni dei criteri.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Messaggio WM_SETTINGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233715"
---
# <a name="wm_settingchange-message"></a>\_Messaggio SETTINGCHANGE WM

Messaggio inviato a tutte le finestre di primo livello quando la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) modifica un'impostazione a livello di sistema o quando sono state modificate le impostazioni dei criteri.

Le applicazioni devono inviare **WM \_ SETTINGCHANGE** a tutte le finestre di primo livello quando apportano modifiche ai parametri di sistema. (Questo messaggio non può essere inviato direttamente a una finestra). Per inviare il **messaggio \_ WM SETTINGCHANGE** a tutte le finestre di primo livello, utilizzare la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con il parametro *HWND* impostato su **HWND \_ broadcast**.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Quando il sistema invia questo messaggio in seguito a una chiamata [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , il parametro *wParam* corrisponde al valore del parametro *uiAction* passato alla funzione **SystemParametersInfo** . Per un elenco di valori, vedere **SystemParametersInfo**.

Quando il sistema invia questo messaggio a seguito di una modifica nelle impostazioni dei criteri, questo parametro indica il tipo di criteri applicato. Questo valore è 1 se è stato applicato un criterio computer o zero se è stato applicato un criterio utente.

Quando il sistema invia questo messaggio a seguito di una modifica nelle impostazioni locali, questo parametro è zero.

Quando un'applicazione invia questo messaggio, questo parametro deve essere **null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Quando il sistema invia questo messaggio in seguito a una chiamata [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* è un puntatore a una stringa che indica l'area contenente il parametro di sistema che è stato modificato. Questo parametro non indica in genere quale parametro di sistema specifico è stato modificato. Si noti che alcune applicazioni inviano questo messaggio con *lParam* impostato su **null**. In generale, quando si riceve questo messaggio, è necessario controllare e ricaricare le impostazioni dei parametri di sistema utilizzate dall'applicazione.

Questa stringa può essere il nome di una chiave del registro di sistema o il nome di una sezione nel file di Win.ini. Quando la stringa è un nome del registro di sistema, in genere indica solo il nodo foglia nel registro di sistema, non il percorso completo.

Quando il sistema invia questo messaggio a seguito di una modifica nelle impostazioni dei criteri, questo parametro punta alla stringa "Policy".

Quando il sistema invia questo messaggio a seguito di una modifica nelle impostazioni locali, questo parametro punta alla stringa "Intl".

Per applicare una modifica nelle variabili di ambiente per il sistema o l'utente, trasmettere questo messaggio con *lParam* impostato sulla stringa "Environment".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se si elabora questo messaggio, restituire zero.

## <a name="remarks"></a>Commenti

Il parametro *lParam* indica quale metrica di sistema è stata modificata, ad esempio, "ConvertibleSlateMode" se l'indicatore ConvertibleSlateMode è stato attivato o "SystemDockMode" se l'indicatore ancorato è stato attivato o disattivato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi dei criteri](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
