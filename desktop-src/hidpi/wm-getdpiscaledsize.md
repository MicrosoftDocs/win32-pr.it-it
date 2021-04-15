---
title: Messaggio WM_GETDPISCALEDSIZE (winuser. h)
description: Questo messaggio indica al sistema operativo che la finestra verrà ridimensionata in dimensioni diverse da quelle predefinite.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- Messaggio WM_GETDPISCALEDSIZE alto DPI
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
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476858"
---
# <a name="wm_getdpiscaledsize-message"></a>\_Messaggio GETDPISCALEDSIZE WM

Questo messaggio indica al sistema operativo che la finestra verrà ridimensionata in dimensioni diverse da quelle predefinite.

Questo messaggio viene inviato alle finestre di primo livello con un [ \_ \_ contesto](dpi-awareness-context.md) di compatibilità dpi di per monitor V2 prima dell'invio di un messaggio [**WM \_ DPICHANGED**](wm-dpichanged.md) e consente alla finestra di calcolare la dimensione desiderata per la modifica dpi in sospeso. Poiché il ridimensionamento DPI lineare è il comportamento predefinito, questa opzione è utile solo negli scenari in cui la finestra vuole ridimensionare in modo non lineare. Se l'applicazione risponde a questo messaggio, la dimensione risultante sarà il rettangolo candidato inviato a **WM \_ DPICHANGED**.

Utilizzare questo messaggio per modificare la dimensione del Rect fornito con [**WM \_ DPICHANGED**](wm-dpichanged.md).


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il WPARAM contiene un valore DPI. Le dimensioni della finestra ridimensionate che l'applicazione deve impostare devono essere calcolate come se la finestra fosse in grado di passare a questo DPI.

</dd> <dt>

*lParam* 
</dt> <dd>

LPARAM è un puntatore in/out a uno struct di dimensioni. Il \_ \_ valore in in lParam è la dimensione in sospeso della finestra dopo uno spostamento avviato dall'utente o una chiamata a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Se è in corso il ridimensionamento della finestra, questa dimensione non corrisponde necessariamente alla dimensione corrente della finestra al momento della ricezione del messaggio.

Il \_ \_ valore out in lParam deve essere scritto dall'applicazione per specificare le dimensioni della finestra ridimensionate desiderate corrispondenti al valore DPI fornito in wParam.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un valore BOOL. Restituisce TRUE indica che è stata calcolata una nuova dimensione. Restituisce FALSE indica che il messaggio non verrà gestito e il ridimensionamento DPI lineare predefinito verrà applicato alla finestra.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato solo a finestre di primo livello con un contesto di compatibilità DPI di per monitor V2.

Questo evento è necessario per facilitare il ridimensionamento non lineare normale e garantisce che la posizione di Windows rimanga costante in relazione al cursore e quando si spostano avanti e indietro tra i monitoraggi.

Non esiste alcuna gestione predefinita specifica del messaggio in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Come per tutti i messaggi non gestiti in modo esplicito, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) restituirà zero per questo messaggio. Come indicato in precedenza, questo ritorno indica al sistema di usare il comportamento lineare predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

