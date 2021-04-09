---
title: Messaggio WM_DPICHANGED (WinUser. h)
description: Inviato quando viene modificato il valore dpi (punti per pollice) effettivo per una finestra.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- Messaggio WM_DPICHANGED alto DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741834"
---
# <a name="wm_dpichanged-message"></a>\_Messaggio DPICHANGED WM

Inviato quando viene modificato il valore dpi (punti per pollice) effettivo per una finestra. Il valore DPI è il fattore di scala per una finestra. Sono presenti più eventi che possono causare la modifica del valore DPI. Nell'elenco seguente sono indicate le possibili cause della modifica in DPI.

-   La finestra viene spostata in un nuovo monitor con un valore DPI diverso.
-   Viene modificato il valore DPI del monitoraggio che ospita la finestra.

Il valore DPI corrente per una finestra è sempre uguale all'ultimo valore DPI inviato da **WM \_ DPICHANGED**. Questo è il fattore di scala che la finestra deve ridimensionare per i thread che sono consapevoli delle modifiche DPI.


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del *wParam* contiene il valore dell'asse Y del nuovo dpi della finestra. Il [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del *wParam* contiene il valore dell'asse X del nuovo valore dpi della finestra. Ad esempio, 96, 120, 144 o 192. I valori dell'asse X e l'asse Y sono identici per le app di Windows.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/windows/desktop/api/windef/ns-windef-rect) che fornisce le dimensioni suggerite e la posizione della finestra corrente ridimensionata per il nuovo valore dpi. Si prevede che le app riposizionano e ridimensionano le finestre in base ai suggerimenti forniti da *lParam* durante la gestione di questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Questo messaggio è pertinente solo per le applicazioni con **\_ \_ \_ \_ riconoscimento dpi del monitor** o per la **consapevolezza dpi per thread \_ \_ \_ \_ compatibili con monitoraggio** . È possibile che venga ricevuta in determinate modifiche DPI se la finestra di primo livello o il processo è in esecuzione con compatibilità **dpi** o **compatibile con DPI di sistema**, ma in tali situazioni può essere tranquillamente ignorato. Per ulteriori informazioni sui diversi tipi di riconoscimento, vedere [**processo \_ dpi \_ Awareness**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) e [**dpi \_ Awareness**](/windows/desktop/api/windef/ne-windef-dpi_awareness). Le versioni precedenti di Windows richiedevano il riconoscimento DPI per essere associato al livello di un'applicazione. Queste app usano **la \_ \_ consapevolezza dpi del processo**. Attualmente, la consapevolezza DPI è associata a thread e singole finestre anziché all'intera applicazione. Queste app usano **la \_ consapevolezza dpi**.

È sufficiente usare l'asse X o il valore dell'asse Y durante il ridimensionamento dell'applicazione perché sono uguali.

Per gestire correttamente questo messaggio, sarà necessario ridimensionare e riposizionare la finestra in base ai suggerimenti forniti da *lParam* e usando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Se non si esegue questa operazione, la finestra aumenterà o verrà ridotta rispetto a tutti gli altri elementi del nuovo monitor. Se, ad esempio, un utente utilizza più monitoraggi e trascina la finestra da un monitor 96 DPI a un monitor 192 DPI, la finestra apparirà la metà delle dimensioni rispetto ad altri elementi del monitor 192 DPI.

Il valore di base di DPI è definito **come \_ \_ \_ DPI dello schermo predefinito dell'utente** , che è impostato su 96. Per determinare il fattore di scalabilità per un monitoraggio, impostare il valore DPI e dividere in base a **\_ \_ \_ DPI dello schermo predefinito dell'utente**. Nella tabella seguente vengono forniti alcuni valori DPI di esempio e i fattori di scala associati.



| Valore DPI | Percentuale di ridimensionamento |
|-----------|--------------------|
| 96        | 100%               |
| 120       | 125%               |
| 144       | 150%               |
| 192       | 200%               |



 

Nell'esempio seguente viene fornito un gestore delle modifiche DPI di esempio.


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



Il codice seguente consente di ridimensionare in modo lineare un valore da 100% (96 DPI) a un valore DPI arbitrario definito da *g \_ dpi*.


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



Un modo alternativo per ridimensionare un valore consiste nel convertire il valore DPI in un fattore di scala e usarlo.


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_riconoscimento dpi**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**\_riconoscimento dpi \_ processo**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

