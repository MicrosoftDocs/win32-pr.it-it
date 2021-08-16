---
title: WM_GETDPISCALEDSIZE messaggio (Winuser.h)
description: Questo messaggio indica al sistema operativo che la finestra verrà ridimensionata in dimensioni diverse da quelle predefinite.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE messaggio High DPI
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3386a0f38187e375f9dae0e390a413a1e64565f15d39e1e9f1e436c9238bea99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759292"
---
# <a name="wm_getdpiscaledsize-message"></a>Messaggio \_ WM GETDPISCALEDSIZE

Questo messaggio indica al sistema operativo che la finestra verrà ridimensionata in dimensioni diverse da quelle predefinite.

Questo messaggio viene inviato alle finestre di primo livello con [DPI \_ AWARENESS \_ CONTEXT](dpi-awareness-context.md) di Per Monitor v2 prima dell'invio di un messaggio [**WM \_ DPICHANGED**](wm-dpichanged.md) e consente alla finestra di calcolare le dimensioni desiderate per la modifica DPI in sospeso. Poiché il ridimensionamento DPI lineare è il comportamento predefinito, questo è utile solo negli scenari in cui la finestra vuole ridimensionare in modo non lineare. Se l'applicazione risponde a questo messaggio, le dimensioni risultanti saranno il rettangolo candidato inviato a **WM \_ DPICHANGED.**

Usare questo messaggio per modificare le dimensioni del rettale fornito con [**WM \_ DPICHANGED.**](wm-dpichanged.md)


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

WPARAM contiene un valore DPI. Le dimensioni della finestra ridimensionata che verrebbero impostate dall'applicazione devono essere calcolate come se la finestra passasse a questo valore DPI.

</dd> <dt>

*lParam* 
</dt> <dd>

LPARAM è un puntatore in/out a uno struct SIZE. Il valore In in LPARAM è la dimensione in sospeso della finestra dopo uno spostamento avviato dall'utente o una \_ \_ chiamata a [**SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) Se la finestra viene ridimensionata, queste dimensioni non corrispondono necessariamente alle dimensioni correnti della finestra al momento della ricezione del messaggio.

Il valore Out in LPARAM deve essere scritto dall'applicazione per specificare le dimensioni della finestra ridimensionate desiderate corrispondenti al valore \_ \_ DPI specificato in WPARAM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un valore BOOL. La restituzione di TRUE indica che è stata calcolata una nuova dimensione. La restituzione di FALSE indica che il messaggio non verrà gestito e il ridimensionamento DPI lineare predefinito verrà applicato alla finestra.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato solo alle finestre di primo livello che hanno un contesto di riconoscimento DPI di Per Monitor v2.

Questo evento è necessario per facilitare il ridimensionamento non lineare e garantisce che la posizione delle finestre rimanga costante in relazione al cursore e quando si sposta avanti e indietro tra i monitor.

Non esiste alcuna gestione predefinita specifica di questo messaggio in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Come per tutti i messaggi non gestiti in modo esplicito, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) restituirà zero per questo messaggio. Come indicato in precedenza, questo valore restituito indica al sistema di usare il comportamento lineare predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                            |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



 

