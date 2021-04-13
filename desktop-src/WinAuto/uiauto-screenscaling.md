---
title: Informazioni sui problemi di scalabilità dello schermo
description: Windows Vista e le versioni successive del sistema operativo consentono agli utenti di modificare l'impostazione dpi (punti per pollice) in modo che la maggior parte degli elementi dell'interfaccia utente sullo schermo risulti più grande.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- client, ridimensionamento dello schermo di automazione interfaccia utente
- client, ridimensionamento dello schermo
- client, ridimensionamento
- Automazione interfaccia utente, ridimensionamento dello schermo
- Automazione interfaccia utente, ridimensionamento
- ridimensionamento dello schermo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d790ee7747f258847cd23aea8bbbe8c25813fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399533"
---
# <a name="understanding-screen-scaling-issues"></a>Informazioni sui problemi di scalabilità dello schermo

Windows Vista e le versioni successive del sistema operativo consentono agli utenti di modificare l'impostazione dpi (punti per pollice) in modo che la maggior parte degli elementi dell'interfaccia utente sullo schermo risulti più grande. Nelle versioni precedenti di Windows, la scalabilità doveva essere implementata dalle applicazioni. In Windows Vista e versioni successive, il Gestione finestre desktop (DWM) esegue il ridimensionamento predefinito per tutte le applicazioni che non gestiscono la scalabilità. Le applicazioni client di automazione interfaccia utente Microsoft devono tenere conto di questa funzionalità.

In questo argomento sono incluse le sezioni seguenti:

-   [Ridimensionamento in Windows Vista e versioni successive](#scaling-in-windows-vista-and-later)
-   [Ridimensionamento nei client di automazione interfaccia utente](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>Ridimensionamento in Windows Vista e versioni successive

L'impostazione DPI predefinita è 96, il che significa che 96 pixel occupano una larghezza o un'altezza di un pollice teorico. La misura esatta di un pollice dipende dalle dimensioni e dalla risoluzione fisica del monitor. Ad esempio, su un monitor con una larghezza di 12 pollici e una risoluzione orizzontale di 1280 pixel, una riga orizzontale di 96 pixel si estende per circa 9/10 di un pollice.

La modifica dell'impostazione DPI non corrisponde alla modifica della risoluzione dello schermo. Con il ridimensionamento DPI, il numero di pixel fisici sullo schermo rimane lo stesso. Il ridimensionamento viene tuttavia applicato alle dimensioni e alla posizione degli elementi dell'interfaccia utente. Questo ridimensionamento può essere eseguito automaticamente da DWM per il desktop e per le applicazioni che non richiedono in modo esplicito la scalabilità.

In effetti, quando l'utente imposta il fattore di scala su 120 dpi, un pollice verticale o orizzontale sullo schermo aumenta del 25%. Tutte le dimensioni vengono ridimensionate di conseguenza. L'offset di una finestra dell'applicazione dal bordo superiore e il bordo sinistro dello schermo aumenta del 25%. Se il ridimensionamento dell'applicazione è abilitato e l'applicazione non è compatibile con dpi, le dimensioni della finestra aumentano nella stessa proporzione, con gli offset e le dimensioni di tutti gli elementi dell'interfaccia utente che contiene.

> [!Note]  
> Per impostazione predefinita, DWM non esegue la scalabilità per le applicazioni non compatibili con DPI quando l'utente imposta il valore dpi su 120, ma esegue il ridimensionamento quando il valore dpi è impostato su un valore personalizzato pari a 144 o superiore. È tuttavia possibile ignorare questo comportamento predefinito.

 

Il ridimensionamento dello schermo crea nuove sfide per le applicazioni che dipendono dalle coordinate dello schermo. Lo schermo contiene ora due sistemi di coordinate: fisico e logico. Le coordinate fisiche di un punto sono l'offset effettivo in pixel dalla parte superiore sinistra del punto di origine. Le coordinate logiche sono gli offset così come si presenterebbero se i pixel fossero ridimensionati.

Si supponga di progettare una finestra di dialogo con un pulsante in corrispondenza delle coordinate (100, 48). Quando questa finestra di dialogo viene visualizzata sul valore predefinito 96 dpi, il pulsante si trova in corrispondenza delle coordinate fisiche (100, 48). A 120 dpi si trova in corrispondenza delle coordinate fisiche (125, 60). Tuttavia, le coordinate logiche sono le stesse in qualsiasi impostazione dpi: (100, 48).

Le coordinate logiche sono importanti, perché rendono coerenti il comportamento del sistema operativo e delle applicazioni, indipendentemente dall'impostazione dpi. Ad esempio, la funzione [**GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) restituisce in genere le coordinate logiche. Se si sposta il cursore su un elemento in una finestra di dialogo, vengono restituite le stesse coordinate, indipendentemente dall'impostazione dpi. Se si disegna un controllo in (100, 100), questo viene disegnato su queste coordinate logiche e occupa la stessa posizione relativa in qualsiasi impostazione dpi.

## <a name="scaling-in-ui-automation-clients"></a>Ridimensionamento nei client di automazione interfaccia utente

L'API di automazione interfaccia utente non usa coordinate logiche. I metodi e le proprietà seguenti restituiscono coordinate fisiche o accettano coordinate fisiche come parametri.

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement:: GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment:: BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

Per impostazione predefinita, le applicazioni di automazione interfaccia utente in esecuzione in un ambiente che non è impostato su 96 dpi non otterranno risultati corretti da questi metodi e proprietà. Ad esempio, poiché la posizione del cursore è nelle coordinate logiche, il client non può passare queste coordinate a [**IUIAutomation:: ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) per ottenere l'elemento che si trova sotto il cursore. Inoltre, l'applicazione non sarà in grado di posizionare correttamente le finestre al di fuori dell'area client.

La soluzione è costituita da due parti.

Per prima cosa, fare in modo che l'applicazione client sia compatibile con dpi. A tale scopo, chiamare la funzione [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) all'avvio. Questa funzione rende l'intero processo compatibile con dpi, vale a dire che tutte le finestre appartenenti al processo non vengono ridimensionate.

In secondo luogo, per ottenere le coordinate del cursore, chiamare la funzione [**GetPhysicalCursorPos**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) .

 

 