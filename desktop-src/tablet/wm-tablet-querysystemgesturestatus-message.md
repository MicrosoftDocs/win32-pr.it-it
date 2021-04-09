---
description: Inviato quando il sistema richiede a una finestra i movimenti di sistema che si desidera ricevere.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Messaggio WM_TABLET_QUERYSYSTEMGESTURESTATUS (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879129"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a>\_ \_ Messaggio QUERYSYSTEMGESTURESTATUS di WM Tablet

Inviato quando il sistema richiede a una finestra i movimenti di sistema che si desidera ricevere.


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore punto che rappresenta le coordinate dello schermo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Grazie alla gestione di questo messaggio, è possibile disabilitare dinamicamente i gesti rapidi per le aree di una finestra.

> [!Note]  
> Il *lParam* può essere convertito in coordinate x e y mediante le `GET_X_LPARAM` `GET_Y_LPARAM` macro e.

 

Per impostazione predefinita, la finestra riceverà tutti gli eventi di movimento del sistema. È possibile scegliere quali eventi si desidera vengano ricevuti dalla finestra e quali eventi si desidera disabilitare rispondendo al messaggio **WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS** in **WndProc**. Il messaggio **WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS** è definito in tpcshrd. h. I valori per abilitare e disabilitare i movimenti del Tablet System di sistema sono definiti anche in tpcshrd. h, come indicato di seguito:

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> La disabilitazione di pressione propagata consente di migliorare la velocità di risposta per i clic del mouse perché questa funzionalità crea un tempo di attesa per distinguere tra le due operazioni.

 

Prestare attenzione durante la gestione del messaggio **WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS** . **WM \_ Il TABLET \_ QUERYSYSTEMGESTURESTATUS** viene passato utilizzando la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . Se si chiamano metodi su un'interfaccia COM, tale oggetto deve trovarsi all'interno dello stesso processo. In caso contrario, COM genera un'eccezione.

## <a name="examples"></a>Esempio

L'esempio seguente illustra come disabilitare i gesti rapidi per un'area usando WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS.


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



Nell'esempio seguente viene illustrato come disabilitare diverse funzionalità di gesti rapidi per un'intera finestra.


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
