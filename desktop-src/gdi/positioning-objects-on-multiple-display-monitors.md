---
description: Una finestra o un menu che si trova in più monitor causa un'interruzione visiva per un visualizzatore. Per ridurre al minimo questo problema, il sistema visualizza i menu e le finestre nuove e ingrandite su un unico monitor. La tabella seguente illustra come viene scelto il monitoraggio.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Posizionamento di oggetti su più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6581fbed64b6a8ac83e29410e9758c6dea7b2d145958c57fa187abf34985c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602731"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Posizionamento di oggetti su più monitor di visualizzazione

Una finestra o un menu che si trova in più monitor causa un'interruzione visiva per un visualizzatore. Per ridurre al minimo questo problema, il sistema visualizza i menu e le finestre nuove e ingrandite su un unico monitor. La tabella seguente illustra come viene scelto il monitoraggio.



| Oggetto         | Località                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Finestra         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(Ex) visualizza una finestra sul monitor che contiene la parte più grande della finestra. Ingrandisce il monitor che contiene la parte più grande della finestra prima che fosse ridotta a icona.<br/> La combinazione di tasti ALT+TAB visualizza una finestra sul monitor con la finestra attualmente attiva.<br/>                                                                                                                                          |
| finestra di proprietà   | sullo stesso monitor del proprietario.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Sottomenu        | Viene visualizzato nel monitoraggio che contiene la parte più grande della voce di menu corrispondente.                                                                                                                                                                                                                                                                                                                                                                                                          |
| menu di scelta rapida   | Viene visualizzato nel monitor in cui si è verificato il clic con il pulsante destro del mouse.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| elenco a discesa | Viene visualizzato sul monitor che contiene il rettangolo della casella combinata.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| finestra di dialogo     | Viene visualizzato nel monitoraggio della finestra proprietaria. Se è definito con lo stile DS \_ CENTERMOUSE, viene visualizzato sul monitor con il mouse.<br/> Se non dispone di alcun proprietario e la finestra attiva e la finestra di dialogo si trova nella stessa applicazione, la finestra di dialogo viene visualizzata sul monitor della finestra attualmente attiva.<br/> Se la finestra di dialogo non ha alcun proprietario e la finestra attiva non si trova nella stessa applicazione della finestra di dialogo, la finestra di dialogo viene visualizzata nel monitor principale.<br/> |
| finestra di messaggio    | Viene visualizzato nel monitoraggio della finestra proprietaria.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Se una finestra si trova tra due monitor e uno dei monitor viene riposizionato, il sistema posiziona la finestra sul monitor che contiene la parte più grande della finestra originale.

Un'applicazione dovrà anche in genere posizionare gli oggetti . Ad esempio, potrebbe essere necessario creare una finestra sullo stesso monitor di un'altra finestra.

**Per posizionare un oggetto in un sistema a più monitor**

1.  Determinare il monitoraggio appropriato.
2.  Ottenere le coordinate per il monitoraggio.
3.  Posizionare l'oggetto usando le coordinate.

In genere, si posiziona un oggetto sul monitor primario o su un monitor che dispone già di un oggetto. Per identificare il monitoraggio per un punto, un rettangolo o una finestra specificata, usare [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint), [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)e [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow).

Per ottenere le coordinate per il monitoraggio, usare [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), che fornisce sia l'area di lavoro che l'intero rettangolo del monitoraggio. Si noti che SM CXSCREEN e SM CYSCREEN fanno sempre riferimento al monitoraggio primario, non necessariamente al \_ \_ monitoraggio che visualizza l'applicazione. Evitare anche SM xxVIRTUALSCREEN perché in questo modo la finestra viene centrata sullo \_ schermo virtuale, non su un monitor.

Per centrare le finestre di dialogo nell'area di lavoro di una finestra, usare lo stile DS \_ CENTER. Per centrare la finestra di dialogo in una finestra dell'applicazione, [**usare GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect). Windows limita automaticamente menu e finestre di dialogo a un monitoraggio. Tuttavia, può verificarsi un problema per i menu personalizzati, le caselle a discesa personalizzate, i riquadri degli strumenti personalizzati e la posizione dell'applicazione salvata.

Per un esempio di posizionamento corretto degli oggetti, vedere [Posizionamento di oggetti in una configurazione a più display](positioning-objects-on-a-multiple-display-setup.md).

L'uso di SM CXSCREEN e SM CYSCREEN per determinare la posizione di una barra degli strumenti del desktop dell'applicazione (denominata anche appbar ) limita la barra delle app \_ \_ al monitoraggio primario.  Per consentire a una barra delle app di essere su qualsiasi bordo di qualsiasi monitoraggio, usare le metriche di sistema appropriate per calcolare i bordi dei monitoraggi. Usare anche le macro **GET \_ X \_ LPARAM** e **GET Y \_ \_ LPARAM** per estrarre le coordinate, altrimenti il segno delle coordinate potrebbe non essere corretto. Queste macro sono incluse in Windowsx.h.

Le dimensioni di una finestra a schermo intero devono cambiare quando si sposta tra monitor con risoluzioni diverse. A tale scopo, l'applicazione deve controllare la finestra in cui si trova usando [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) o [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) e quindi usare [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) per ottenere le dimensioni del monitoraggio. In alternativa, è possibile usare **HMONITOR** dalla funzione **DirectX DirectDrawEnumerateEx.** Usare quindi [**SetWindowPos per**](/windows/win32/api/winuser/nf-winuser-setwindowpos) posizionare e ridimensionare la finestra per coprire il monitoraggio.

Una finestra ingrandita non copre una barra delle applicazioni con la proprietà "Sempre in alto". Tuttavia, una finestra a schermo intero copre la barra delle applicazioni, ad esempio in Microsoft PowerPoint presentazioni e giochi.

Per salvare e ripristinare in un secondo momento la posizione di una finestra quando un'applicazione viene chiusa, usare le [**funzioni GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) e [**SetWindowPlacement.**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) Tuttavia, verificare che la posizione sia ancora valida prima di usarla perché il monitoraggio potrebbe essere stato spostato o rimosso dal sistema. L'applicazione visualizza la finestra sul monitoraggio primario se **il monitor HMONITOR** di una finestra non è valido.

Il sistema tenta di avviare un'applicazione nel monitoraggio che contiene il collegamento. Un modo per posizionare un'applicazione è quindi disporre il collegamento su un monitor desiderato.

Se si usa [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx,**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) specificare *un hWnd* in modo che il sistema aperi le nuove finestre sullo stesso monitoraggio dell'applicazione chiamante.

Si noti che i valori per la [**struttura MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) sono leggermente modificati per un sistema con più monitor.

 

 
