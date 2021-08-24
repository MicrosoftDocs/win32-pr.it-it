---
title: WM_DPICHANGED messaggio (WinUser.h)
description: Inviato quando i punti per pollice (dpi) effettivi per una finestra vengono modificati.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED messaggio High DPI
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
ms.openlocfilehash: d77a7d7608e9facc1e0fc6973b19a3d9db36900fa8d550896cc3058389f367bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666381"
---
# <a name="wm_dpichanged-message"></a>Messaggio WM \_ DPICHANGED

Inviato quando i punti per pollice (dpi) effettivi per una finestra vengono modificati. Il valore DPI è il fattore di scala per una finestra. Esistono più eventi che possono causare la modifica del valore DPI. L'elenco seguente indica le possibili cause della modifica in DPI.

-   La finestra viene spostata in un nuovo monitoraggio con un valore DPI diverso.
-   Il valore DPI del monitoraggio che ospita la finestra cambia.

Il valore DPI corrente per una finestra è sempre uguale all'ultimo valore DPI inviato da **WM \_ DPICHANGED.** Questo è il fattore di scala che la finestra deve ridimensionare per i thread che sono consapevoli delle modifiche DPI.


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) *di wParam* contiene il valore dell'asse Y del nuovo dpi della finestra. La [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) di *wParam* contiene il valore dell'asse X del nuovo valore DPI della finestra. Ad esempio, 96, 120, 144 o 192. I valori dell'asse X e dell'asse Y sono identici per Windows app.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/windows/desktop/api/windef/ns-windef-rect) che fornisce una dimensione e una posizione suggerite della finestra corrente ridimensionata per il nuovo valore DPI. L'aspettativa è che le app riposizionano e ridimensionano le finestre in base ai suggerimenti forniti da *lParam* durante la gestione di questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Questo messaggio è pertinente solo per le applicazioni **\_ \_ \_ DPI \_ AWARE PROCESS PER MONITOR** o per i **thread DPI AWARENESS PER \_ MONITOR \_ \_ \_ AWARE.** Può essere ricevuto in determinate modifiche DPI se la finestra o il processo di primo livello è in esecuzione come **DPI** inconsapevole o in grado di riconoscere **DPI** di sistema, ma in tali situazioni può essere tranquillamente ignorato. Per altre informazioni sui diversi tipi di consapevolezza, vedere [**PROCESS \_ DPI \_ AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) e [**DPI \_ AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness). Le versioni precedenti Windows necessario che la consapevolezza DPI sia associata al livello di un'applicazione. Queste app usano **PROCESS \_ DPI \_ AWARENESS**. Attualmente, la consapevolezza DPI è associata a thread e singole finestre anziché all'intera applicazione. Queste app usano **DPI \_ AWARENESS**.

È necessario usare solo l'asse X o il valore dell'asse Y quando si ridimensiona l'applicazione perché sono uguali.

Per gestire correttamente questo messaggio, è necessario ridimensionare e riposizionare la finestra in base ai suggerimenti forniti da *lParam* e usando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Se non si esegue questa operazione, la finestra aumenta o si riduce rispetto a tutti gli altri elementi del nuovo monitoraggio. Ad esempio, se un utente usa più monitor e trascina la finestra da un monitor da 96 DPI a un monitor DPI da 192, la finestra apparirà metà grande rispetto ad altri elementi nel monitoraggio DPI da 192.

Il valore di base di DPI è definito come **USER \_ DEFAULT SCREEN \_ \_ DPI,** che è impostato su 96. Per determinare il fattore di scala per un monitoraggio, prendere il valore DPI e dividere per **USER \_ DEFAULT SCREEN \_ \_ DPI**. Nella tabella seguente vengono forniti alcuni valori DPI di esempio e i fattori di scala associati.



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



Il codice seguente ridimensiona in modo lineare un valore dal 100% (96 DPI) a un valore DPI arbitrario definito da *g \_ dpi*.


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
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CONSAPEVOLEZZA DPI \_**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**ELABORARE \_ LA CONSAPEVOLEZZA DPI \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

