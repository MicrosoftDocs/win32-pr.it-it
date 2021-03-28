---
description: Una finestra o un menu che si trova in più di un monitoraggio causa un'interferenza visiva per un visualizzatore. Per ridurre al minimo questo problema, il sistema Visualizza i menu e le finestre nuove e ingrandite su un solo monitor. Nella tabella seguente viene illustrato come viene scelto il monitoraggio.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Posizionamento di oggetti su più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77149291737482fa0f3e7fe19ee4f350ee6521d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978391"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Posizionamento di oggetti su più monitor di visualizzazione

Una finestra o un menu che si trova in più di un monitoraggio causa un'interferenza visiva per un visualizzatore. Per ridurre al minimo questo problema, il sistema Visualizza i menu e le finestre nuove e ingrandite su un solo monitor. Nella tabella seguente viene illustrato come viene scelto il monitoraggio.



| Oggetto         | Location                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Finestra         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(ad esempio) Visualizza una finestra sul monitoraggio che contiene la parte più grande della finestra. Ingrandisce il monitoraggio che contiene la parte più grande della finestra prima che sia ridotta a icona.<br/> La combinazione di tasti ALT + TAB Visualizza una finestra sul monitor con la finestra attualmente attiva.<br/>                                                                                                                                          |
| finestra di proprietà   | sullo stesso monitor del proprietario.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| sottomenu        | Viene visualizzato sul monitor che contiene la parte più grande della voce di menu corrispondente.                                                                                                                                                                                                                                                                                                                                                                                                          |
| menu di scelta rapida   | Viene visualizzato sul monitor in cui si è verificato il clic destro.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| elenco a discesa | Viene visualizzato sul monitor che contiene il rettangolo della casella combinata.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| finestra di dialogo     | Viene visualizzato sul monitor della finestra a cui appartiene. Se è definito con lo \_ stile DS CENTERMOUSE, viene visualizzato sul monitor con il mouse.<br/> Se non è presente alcun proprietario e la finestra attiva e la finestra di dialogo si trovano nella stessa applicazione, la finestra di dialogo viene visualizzata sul monitor della finestra attualmente attiva.<br/> Se nella finestra di dialogo non è presente alcun proprietario e la finestra attiva non si trova nella stessa applicazione della finestra di dialogo, la finestra di dialogo verrà visualizzata sul monitor primario.<br/> |
| MessageBox    | Viene visualizzato sul monitor della finestra a cui appartiene.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Se una finestra occupa due monitoraggi e uno dei monitoraggi viene riposizionato, il sistema posiziona la finestra sul monitor che contiene la parte più grande della finestra originale.

Un'applicazione deve in genere anche posizionare gli oggetti. Ad esempio, potrebbe essere necessario creare una finestra sullo stesso monitor di un'altra finestra.

**Per posizionare un oggetto in un sistema a più monitor**

1.  Determinare il monitoraggio appropriato.
2.  Ottenere le coordinate del monitoraggio.
3.  Posizionare l'oggetto usando le coordinate.

In genere, un oggetto viene posizionato sul monitor primario o su un monitoraggio su cui è già presente un oggetto. Per identificare il monitoraggio per un punto, un rettangolo o una finestra specifica, usare [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint), [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)e [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow).

Per ottenere le coordinate per il monitoraggio, utilizzare [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), che fornisce sia l'area di lavoro che l'intero rettangolo di monitoraggio. Si noti che SM \_ CXSCREEN e SM \_ CYSCREEN si riferiscono sempre al monitoraggio principale, non necessariamente al monitoraggio che Visualizza l'applicazione. Evitare inoltre xxVIRTUALSCREEN SM \_ perché questo centra la finestra sullo schermo virtuale, non su un monitor.

Per centrare le finestre di dialogo nell'area di lavoro di una finestra, utilizzare lo \_ stile DS Center. Per centrare la finestra di dialogo in una finestra dell'applicazione, usare [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect). Windows limita automaticamente i menu e le finestre di dialogo a un monitoraggio. Tuttavia, è possibile che si verifichi un problema per i menu personalizzati, le caselle di riepilogo a discesa personalizzate, le tavolozze degli strumenti personalizzate e la posizione dell'applicazione salvata.

Per un esempio di come posizionare correttamente gli oggetti, vedere [posizionamento di oggetti in una configurazione con più visualizzazioni](positioning-objects-on-a-multiple-display-setup.md).

Se si usa SM \_ CXSCREEN e SM \_ CYSCREEN per determinare la posizione di una barra degli strumenti del desktop dell'applicazione (denominata anche *AppBar*), il AppBar viene limitato al monitor primario. Per consentire a un AppBar di trovarsi su qualsiasi bordo di qualsiasi monitoraggio, usare le metriche di sistema appropriate per calcolare i bordi dei monitoraggi. Usare inoltre le macro **get \_ X \_ lParam** e **get \_ Y \_ lParam** per estrarre le coordinate. in caso contrario, il segno delle coordinate potrebbe non essere corretto. Queste macro sono incluse in WINDOWSX. h.

È necessario modificare la dimensione di una finestra a schermo intero mentre si sposta tra i monitoraggi con risoluzioni diverse. A tale scopo, l'applicazione deve verificare la finestra in cui si trova, usando [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) o [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) e quindi usare [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) per ottenere le dimensioni del monitoraggio. In alternativa, è possibile usare **HMONITOR** dalla funzione DirectX **DirectDrawEnumerateEx** . Usare quindi [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) per posizionare e ridimensionare la finestra per coprire il monitoraggio.

Una finestra ingrandita non copre una barra delle applicazioni con la proprietà "always on top". Tuttavia, una finestra a schermo intero copre la barra delle applicazioni, ad esempio in Microsoft PowerPoint Slide shows and Games.

Per salvare e successivamente ripristinare la posizione di una finestra alla chiusura di un'applicazione, usare le funzioni [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) e [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) . Verificare tuttavia che la posizione sia ancora valida prima di utilizzarla perché il monitoraggio potrebbe essere stato spostato o rimosso dal sistema. L'applicazione Visualizza la finestra sul monitor principale se il **HMONITOR** di una finestra non è valido.

Il sistema tenta di avviare un'applicazione sul monitor che contiene il collegamento. Quindi, un modo per posizionare un'applicazione consiste nell'avere il collegamento su un monitor desiderato.

Se si usa [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) , fornire un *HWND* in modo che il sistema Apra tutte le nuove finestre sullo stesso monitoraggio dell'applicazione chiamante.

Si noti che i valori per la struttura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) sono leggermente modificati per un sistema con più monitoraggi.

 

 
