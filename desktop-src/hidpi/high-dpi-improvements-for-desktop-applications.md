---
title: Mixed-Mode ridimensionamento DPI e API che sono in grado di riconoscere DPI
description: Mixed-Mode ridimensionamento DPI e API che sono in grado di riconoscere DPI
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5b16e4c438cfe1f0d04e61524899e213b25ea
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119726"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode ridimensionamento DPI e API che sono in grado di riconoscere DPI

## <a name="sub-process-dpi-awareness-support"></a>Sub-Process supporto per la consapevolezza DPI

[**SetThreadDpiAwarenessContext consente**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) l'uso di diverse modalità di ridimensionamento DPI all'interno di un singolo processo. Prima dell'Aggiornamento dell'anniversario di Windows 10, il riconoscimento DPI di una finestra era associato alla modalità di riconoscimento DPI a livello di processo (riconoscimento DPI non noto, riconoscimento DPI di sistema o riconoscimento DPI Per-Monitor). Ma ora, con **SetThreadDpiAwarenessContext,** le finestre di primo livello possono avere una modalità di riconoscimento DPI diversa da quella della modalità di riconoscimento DPI a livello di processo. Ciò ha effetto anche sulle finestre figlio, in quanto avranno sempre la stessa modalità di riconoscimento DPI della finestra padre.

L'uso **di SetThreadDpiAwarenessContext** consente agli sviluppatori di decidere dove concentrare le attività di sviluppo quando definiscono il comportamento specifico di DPI per le applicazioni desktop. Ad esempio, la finestra principale principale di un'applicazione può essere ridimensionata in base al monitoraggio, mentre le finestre secondarie di primo livello possono essere ridimensionate tramite il ridimensionamento delle bitmap da parte del sistema operativo.

## <a name="the-dpi-awareness-context"></a>Contesto di consapevolezza DPI

Prima della disponibilità di **SetThreadDpiAwarenessContext,** la conoscenza DPI di un processo è stata definita nel manifesto del file binario dell'applicazione o tramite una chiamata a [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) durante l'inizializzazione del processo. Con **SetThreadDpiAwarenessContext** ogni thread può avere un singolo contesto di riconoscimento DPI che può essere diverso da quello della modalità di riconoscimento DPI a livello di processo. Il contesto di riconoscimento DPI di un thread è rappresentato con il tipo [****DPI \_ AWARENESS \_ CONTEXT*** e](dpi-awareness-context.md) si comporta nei modi seguenti:

-   Un thread può modificare il contesto di riconoscimento DPI in qualsiasi momento.
-   Tutte le chiamate API eseguite dopo la modifica del contesto verranno eseguite nel contesto DPI corrispondente (e possono essere virtualizzate).
-   Quando viene creata una finestra, il riconoscimento DPI viene definito come riconoscimento DPI del thread chiamante in quel momento.
-   Quando viene chiamata la routine della finestra per una finestra, il thread passa automaticamente al contesto di riconoscimento DPI in uso al momento della creazione della finestra.

Uno scenario comune per l'uso di **SetThreadDpiAwarenessContext** è il seguente: Iniziare con un thread in esecuzione con un contesto (ad esempio **DPI \_ AWARENESS CONTEXT PER MONITOR \_ \_ \_ \_ AWARE)** passare temporaneamente a un contesto diverso (**DPI AWARENESS CONTEXT \_ \_ \_ UNAWARE),** creare una finestra e quindi tornare immediatamente allo stato precedente. La finestra creata avrà un contesto DPI di **DPI \_ AWARENESS CONTEXT \_ \_ UNAWARE,** mentre il contesto del thread chiamante verrà ripristinato in **DPI AWARENESS CONTEXT PER \_ \_ MONITOR \_ \_ \_ AWARE** con una chiamata successiva a **SetThreadDpiAwarenessContext**. In questo scenario, la finestra associata al thread chiamante verrebbe eseguita con un contesto per monitoraggio (e pertanto non verrebbe estesa in base alla bitmap dal sistema operativo) mentre la finestra appena creata non sarebbe in grado di riconoscere DPI (e pertanto verrebbe automaticamente mappata in base a un set di visualizzazione >scalabilità al 100%).

La figura 1 illustra come viene eseguito il thread del processo principale con **DPI \_ AWARENESS CONTEXT \_ PER \_ \_ MONITOR,** passa il contesto a **DPI AWARENESS CONTEXT \_ \_ \_ UNAWARE** e crea una nuova finestra. La finestra appena creata viene quindi eseguita con un contesto di riconoscimento **DPI \_ AWARENESS CONTEXT \_ \_ UNAWARE** ogni volta che viene inviato un messaggio o vengono effettuate chiamate API da tale finestra. Subito dopo la creazione della nuova finestra, il thread principale viene ripristinato nel contesto precedente di **DPI \_ AWARENESS CONTEXT PER \_ \_ \_ MONITOR**.

![Diagramma che mostra la consapevolezza dpi per monitoraggio in azione](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Nuove API correlate a DPI

Oltre al supporto per diverse modalità di riconoscimento DPI all'interno di un singolo processo offerte da **SetThreadDpiAwarenessContext,** è stata aggiunta la funzionalità DPI specifica seguente per le applicazioni desktop:<dl> <dd>[EnableNonClientDpiScaling****](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> La **modalità di riconoscimento DPI per** monitor V2 abilita automaticamente questa funzionalità e la chiamata di **EnableNonClientDpiScaling** non è quindi necessaria nelle applicazioni che la usano.

 

La **chiamata di EnableNonClientDpiScaling** dall'interno del gestore **WM \_ NCCREATE** di una finestra comporta il ridimensionamento automatico dell'area non client di una finestra di primo livello per DPI. Se la finestra di primo livello è in grado di riconoscere DPI per ogni monitoraggio (indipendentemente dal fatto che il processo stesso sia in grado di riconoscere DPI per monitor o perché la finestra è stata creata all'interno di un thread con supporto DPI per ogni monitoraggio), la barra della didascalia, le barre di scorrimento, i menu e le barre dei menu di queste finestre verranno ridimensionate in base al valore DPI ogni volta che cambia il valore DPI della finestra.
</dt> <dt>

Si noti che le aree non client di una finestra figlio, ad esempio le barre di scorrimento non client di un controllo di modifica figlio, non verranno ridimensionate automaticamente quando viene usata questa API.
</dt> <dt>

> [!Note]  
> **EnableNonClientDpiScaling** deve essere chiamato dal gestore **\_ WM NCCREATE.**

</dt> </dl> </dd> <dd> <b> API *ForDpi </b>

-   Diverse API usate di frequente, ad esempio [**GetSystemMetrics,**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) non hanno alcun contesto di HWND e pertanto non hanno modo di dedurre la corretta consapevolezza DPI per i valori restituiti. La chiamata di queste API da un thread in esecuzione in un contesto o in una modalità di riconoscimento DPI diversa può restituire valori non ridimensionati per il contesto del thread chiamante. [****GetSystemMetricForDpi****,](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi) [***SystemParametersInfoForDpi***](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)e [***AdjustWindowRectExForDpi****](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) eseguiranno la stessa funzionalità delle controparti DPI non consapevoli, ma accettano un valore DPI come argomento e dedurranno la consapevolezza dpi dal contesto del thread corrente.
-   **GetSystemMetricForDpi** e **SystemParametersInfoForDpi** restituiranno i valori delle metriche di sistema con scala DPI e i valori dei parametri di sistema in base a questa equazione:

    
    GetSystemMetrics(...) @ dpi == GetSystemMetricsForDpi(..., dpi)

    

     

    Pertanto, la chiamata a **GetSystemMetrics** (o **SystemParametersInfoForDpi)** durante l'esecuzione in un dispositivo con un determinato valore DPI di sistema restituirà lo stesso valore delle varianti che sono in grado di riconoscere DPI (**GetSystemMetricsForDpi** e **SystemParametersInfoForDpi**) dato lo stesso valore DPI dell'input.

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) accetta un oggetto HWND e calcola le dimensioni richieste di un rettangolo della finestra in modo sensibile a DPI.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow</b> restituirà l'interfaccia DPI associata all'HWND fornito. La risposta dipende dalla modalità di riconoscimento DPI di HWND:

| Modalità di riconoscimento DPI di HWND | Valore restituito                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ignari                    | 96                                                                                                                                                                                                            |
| Sistema                     | DPI di sistema                                                                                                                                                                                                |
| Per-Monitor                | Valore DPI di visualizzazione in cui si trova principalmente la finestra di primo livello associata <br/> Se viene specificata una finestra figlio, verrà restituito il valore DPI della finestra padre di primo livello corrispondente.<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

Chiamare **GetDpiForSystem è** più efficiente rispetto a chiamare [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) e [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) per ottenere il valore DPI di sistema.
</dt> <dt>

Qualsiasi componente che potrebbe essere in esecuzione in un'applicazione che usa il riconoscimento DPI del processo secondario non deve presupporre che il valore DPI di sistema sia statico durante il ciclo di vita del processo. Ad esempio, se un thread in esecuzione nel contesto di riconoscimento **DPI \_ AWARENESS CONTEXT \_ \_ UNAWARE** esegue una query sul valore DPI di sistema, la risposta sarà 96. Tuttavia, se lo stesso thread passa al contesto di riconoscimento **DPI \_ AWARENESS CONTEXT \_ \_ SYSTEM** ed esegue nuovamente una query sul valore DPI di sistema, la risposta potrebbe essere diversa. Per evitare l'uso di un valore DPI di sistema memorizzato nella cache (e possibilmente non obsoleto), usare **GetDpiForSystem** per recuperare il valore DPI di sistema relativo alla modalità di riconoscimento DPI del thread chiamante. 
</dt> </dl> </dd> </dl>
