---
title: Ridimensionamento di Mixed-Mode DPI e API compatibili con DPI
description: .
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9f8a8f72b199aaba195002134855155925b30d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956364"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Ridimensionamento di Mixed-Mode DPI e API compatibili con DPI

## <a name="sub-process-dpi-awareness-support"></a>Supporto per la consapevolezza di Sub-Process DPI

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) consente l'uso di diverse modalità di ridimensionamento DPI all'interno di un singolo processo. Prima dell'aggiornamento dell'anniversario di Windows 10, una conoscenza DPI della finestra è stata associata alla modalità di riconoscimento DPI a livello di processo (DPI ignaro, compatibile con DPI di sistema o Per-Monitor DPI in grado di riconoscere). A questo punto, con **SetThreadDpiAwarenessContext**, le finestre di primo livello possono avere una modalità di riconoscimento dpi diversa da quella della modalità di riconoscimento dpi a livello di processo. Questa operazione ha effetto anche sulle finestre figlio, perché avranno sempre la stessa modalità di riconoscimento DPI della finestra padre.

L'uso di **SetThreadDpiAwarenessContext** consente agli sviluppatori di decidere dove desiderano concentrare le proprie attività di sviluppo durante la definizione del comportamento specifico di dpi per le applicazioni desktop. Ad esempio, la finestra principale di un'applicazione può essere ridimensionata in base al monitor, mentre le finestre di primo livello secondarie possono essere ridimensionate tramite il ridimensionamento delle bitmap da parte del sistema operativo.

## <a name="the-dpi-awareness-context"></a>Contesto di riconoscimento DPI

Prima della disponibilità di **SetThreadDpiAwarenessContext** , il riconoscimento dpi di un processo è stato definito nel manifesto del file binario dell'applicazione o tramite una chiamata a [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) durante l'inizializzazione del processo. Con **SetThreadDpiAwarenessContext**, ogni thread può avere un contesto di consapevolezza dpi singolo che può essere diverso da quello della modalità di riconoscimento dpi a livello di processo. Il contesto di riconoscimento DPI di un thread viene rappresentato con il tipo * * * [* dpi \_ Awareness \_ context * *](dpi-awareness-context.md) * * e si comporta nei modi seguenti:

-   Un thread può avere un contesto di riconoscimento DPI modificato in qualsiasi momento.
-   Qualsiasi chiamata API eseguita dopo la modifica del contesto verrà eseguita nel contesto DPI corrispondente (e potrebbe essere virtualizzata).
-   Quando viene creata una finestra, la relativa consapevolezza DPI viene definita come riconoscimento DPI del thread chiamante in quel momento.
-   Quando viene chiamata la routine della finestra per una finestra, il thread viene automaticamente impostato sul contesto di riconoscimento DPI in uso al momento della creazione della finestra.

Uno scenario comune per l'uso di **SetThreadDpiAwarenessContext** è il seguente: iniziare con un thread in esecuzione con un contesto (ad esempio, il **contesto di riconoscimento dpi per \_ \_ \_ ogni \_ monitoraggio \_**) passa temporaneamente a un contesto diverso (**\_ \_ contesto \_** di compatibilità dpi non noto), crea una finestra e quindi passa immediatamente il contesto del thread allo stato precedente. La finestra creata avrà un contesto DPI del **contesto di \_ consapevolezza \_ \_ dpi** non compatibile, mentre il contesto del thread chiamante verrà ripristinato in **base al contesto di riconoscimento dpi per \_ \_ \_ ogni \_ monitoraggio \_** , con una chiamata successiva a **SetThreadDpiAwarenessContext**. In questo scenario, la finestra associata al thread chiamante viene eseguita con un contesto per monitor (e pertanto non deve essere allungata a bitmap dal sistema operativo), mentre la finestra appena creata non è compatibile con DPI (e di conseguenza la bitmap viene allungata automaticamente in un set di visualizzazione a >100% di ridimensionamento).

Nella figura 1 viene illustrato il modo in cui viene eseguito il thread di processo principale con il contesto di compatibilità **dpi \_ \_ \_ per ogni \_ monitoraggio**, il contesto viene attivato dal contesto di **\_ consapevolezza \_ \_ dpi** e viene creata una nuova finestra. La finestra appena creata viene quindi eseguita con un contesto di consapevolezza DPI **del \_ contesto di consapevolezza dpi \_ \_** non riconoscente ogni volta che un messaggio viene inviato all'it o viene effettuata una chiamata API. Subito dopo la creazione della nuova finestra, il thread principale viene ripristinato nel contesto precedente del **\_ contesto di riconoscimento dpi \_ \_ per ogni \_ monitoraggio**.

![diagramma che mostra la consapevolezza dpi per monitor in azione](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Nuove API correlate a DPI

Oltre al supporto per diverse modalità di riconoscimento DPI all'interno di un singolo processo offerto da **SetThreadDpiAwarenessContext** , per le applicazioni desktop sono state aggiunte le funzionalità specifiche di dpi seguenti:<dl> <dd>[EnableNonClientDpiScaling****](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> La modalità di riconoscimento dpi **per monitor V2** Abilita automaticamente questa funzionalità e la chiamata a **EnableNonClientDpiScaling** non è pertanto necessaria nelle applicazioni che la utilizzano.

 

La chiamata di **EnableNonClientDpiScaling** dall'interno di una finestra s **WM \_ NCCREATE** handler determinerà l'area non client di una finestra di primo livello che si ridimensiona automaticamente per dpi. Se la finestra di primo livello è compatibile con DPI per il monitor (indipendentemente dal fatto che il processo stesso sia compatibile con DPI per monitor o perché la finestra è stata creata all'interno di un thread compatibile con DPI per il monitoraggio), la barra del titolo, le barre di scorrimento, i menu e le barre dei menu di queste finestre vengono ridimensionati in base al valore DPI della finestra.
</dt> <dt>

Si noti che le aree non client di una finestra figlio, ad esempio le barre di scorrimento non client di un controllo di modifica figlio, non otterranno automaticamente la scalabilità DPI quando viene usata questa API.
</dt> <dt>

> [!Note]  
> **EnableNonClientDpiScaling** deve essere chiamato dal gestore **WM \_ NCCREATE** .

</dt> </dl> </dd> <dd> <b> API * ForDpi </b>

-   Diverse API usate di frequente, ad esempio [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) , non dispongono di un contesto di HWND e pertanto non hanno alcun modo per dedurre la consapevolezza dpi corretta per i valori restituiti. La chiamata di queste API da un thread in esecuzione in un contesto o in una modalità di riconoscimento DPI differente può restituire valori non ridimensionati per il contesto del thread chiamante. [* * * * GetSystemMetricForDpi * *](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)* *, * * * * [SystemParametersInfoForDpi * *](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)* * e [* * * * AdjustWindowRectExForDpi * *](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) * * eseguirà la stessa funzionalità delle rispettive controparti compatibili con DPI, ma accetterà un dpi come argomento e dedurrà la consapevolezza dpi dal contesto del thread corrente.
-   **GetSystemMetricForDpi** e **SystemParametersInfoForDpi** restituiranno valori della metrica di sistema con scalabilità dpi e valori dei parametri di sistema in base a questa equazione:

    |                                                                 |
    |-----------------------------------------------------------------|
    | GetSystemMetrics (...) @ dpi = = GetSystemMetricsForDpi (..., dpi) |

    

     

    Pertanto, la chiamata di **GetSystemMetrics** (o **SystemParametersInfoForDpi**), durante l'esecuzione in un dispositivo con un determinato valore dpi di sistema, restituirà lo stesso valore che le varianti compatibili con dpi (**GetSystemMetricsForDpi** e **SystemParametersInfoForDpi**) otterranno, dato lo stesso valore dpi come input.

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) accetta un HWND e calcola la dimensione richiesta di un rettangolo della finestra in modo sensibile ai DPI.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow</b> restituirà il valore dpi associato all'elemento HWND fornito. La risposta dipenderà dalla modalità di riconoscimento DPI di HWND:

| Modalità di riconoscimento DPI di HWND | Valore restituito                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A conoscenza                    | 96                                                                                                                                                                                                            |
| Sistema                     | DPI di sistema                                                                                                                                                                                                |
| Per-Monitor                | DPI della visualizzazione a cui si trova principalmente la finestra di primo livello associata <br/> Se viene fornita una finestra figlio, verrà restituito il valore DPI della finestra padre di livello superiore corrispondente.<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

La chiamata di **GetDpiForSystem** è più efficiente rispetto alla chiamata di [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) e [**GETDEVICECAPS**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) per ottenere il valore dpi del sistema.
</dt> <dt>

Tutti i componenti che potrebbero essere in esecuzione in un'applicazione che utilizza la consapevolezza DPI del processo secondario non devono presupporre che il valore DPI del sistema sia statico durante il ciclo di vita del processo. Se, ad esempio, un thread in esecuzione con il contesto di consapevolezza dpi non è in grado di eseguire query sul valore DPI di sistema, la risposta sarà 96. **\_ \_ \_** Tuttavia, se lo stesso thread passava al contesto di sensibilizzazione del **\_ sistema del \_ contesto \_ di riconoscimento dpi** ed esegue una query su DPI di sistema, la risposta potrebbe essere diversa. Per evitare l'utilizzo di un valore DPI di sistema (e possibilmente obsoleto) memorizzato nella cache, utilizzare **GetDpiForSystem** per recuperare il valore dpi di sistema relativo alla modalità di riconoscimento dpi del thread chiamante. 
</dt> </dl> </dd> </dl>