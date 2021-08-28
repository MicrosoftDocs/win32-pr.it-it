---
title: Informazioni sui problemi di ridimensionamento dello schermo
description: Windows Vista e versioni successive del sistema operativo consentono agli utenti di modificare l'impostazione punti per pollice (dpi) in modo che la maggior parte degli elementi dell'interfaccia utente sullo schermo appaia più grande.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- client, ridimensionamento Automazione interfaccia utente schermo
- client, ridimensionamento dello schermo
- client, ridimensionamento
- Automazione interfaccia utente,ridimensionamento dello schermo
- Automazione interfaccia utente, ridimensionamento
- ridimensionamento dello schermo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dcdc8d586b4320e4da04dfdd7e0264f36074cc59fa53f42333ec5a6c3dd135
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614291"
---
# <a name="understanding-screen-scaling-issues"></a>Informazioni sui problemi di ridimensionamento dello schermo

Windows Vista e versioni successive del sistema operativo consentono agli utenti di modificare l'impostazione punti per pollice (dpi) in modo che la maggior parte degli elementi dell'interfaccia utente sullo schermo appaia più grande. Nelle versioni precedenti di Windows, il ridimensionamento doveva essere implementato dalle applicazioni. In Windows Vista e versioni successive, il Gestione finestre desktop (DWM) esegue il ridimensionamento predefinito per tutte le applicazioni che non gestiscono il ridimensionamento. Microsoft Automazione interfaccia utente applicazioni client devono prendere in considerazione questa funzionalità.

In questo argomento sono incluse le sezioni seguenti:

-   [Ridimensionamento in Windows Vista e versioni successive](#scaling-in-windows-vista-and-later)
-   [Ridimensionamento nei client di automazione interfaccia utente](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>Ridimensionamento in Windows Vista e versioni successive

L'impostazione dpi predefinita è 96, ovvero 96 pixel occupano una larghezza o un'altezza di un pollice nozionale. La misura esatta di un pollice dipende dalle dimensioni e dalla risoluzione fisica del monitor. Ad esempio, su un monitor con una larghezza di 12 pollici e una risoluzione orizzontale di 1280 pixel, una riga orizzontale di 96 pixel si estende per circa 9/10 di un pollice.

La modifica dell'impostazione dpi non corrisponde alla modifica della risoluzione dello schermo. Con il ridimensionamento dpi, il numero di pixel fisici sullo schermo rimane invariato. Tuttavia, il ridimensionamento viene applicato alle dimensioni e alla posizione degli elementi dell'interfaccia utente. Questo ridimensionamento può essere eseguito automaticamente dal DWM per il desktop e per le applicazioni che non chiedono esplicitamente di non essere ridimensionate.

In effetti, quando l'utente imposta il fattore di scala su 120 dpi, un pollice verticale o orizzontale sullo schermo diventa più grande del 25%. Tutte le dimensioni vengono ridimensionate di conseguenza. L'offset di una finestra dell'applicazione dal bordo superiore e dal bordo sinistro dello schermo aumenta del 25%. Se il ridimensionamento dell'applicazione è abilitato e l'applicazione non è in grado di riconoscere dpi, le dimensioni della finestra aumentano nella stessa proporzione, insieme agli offset e alle dimensioni di tutti gli elementi dell'interfaccia utente in essa contenuti.

> [!Note]  
> Per impostazione predefinita, DWM non esegue il ridimensionamento per le applicazioni che non supportano dpi quando l'utente imposta il valore dpi su 120, ma esegue il ridimensionamento quando il valore dpi è impostato su un valore personalizzato pari a 144 o superiore. È tuttavia possibile ignorare questo comportamento predefinito.

 

Il ridimensionamento dello schermo crea nuove sfide per le applicazioni che dipendono dalle coordinate dello schermo. Lo schermo contiene ora due sistemi di coordinate: fisico e logico. Le coordinate fisiche di un punto sono l'offset effettivo in pixel dall'angolo superiore sinistro del punto di origine. Le coordinate logiche sono gli offset così come si presenterebbero se i pixel fossero ridimensionati.

Si supponga di progettare una finestra di dialogo con un pulsante in corrispondenza delle coordinate (100, 48). Quando questa finestra di dialogo viene visualizzata con il valore predefinito di 96 dpi, il pulsante si trova in corrispondenza delle coordinate fisiche (100, 48). A 120 dpi, si trova in corrispondenza delle coordinate fisiche (125, 60). Ma le coordinate logiche sono le stesse in qualsiasi impostazione dpi: (100, 48).

Le coordinate logiche sono importanti perché rendono coerente il comportamento del sistema operativo e delle applicazioni, indipendentemente dall'impostazione dpi. Ad esempio, in genere, [**la funzione GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) restituisce le coordinate logiche. Se si sposta il cursore su un elemento di una finestra di dialogo, vengono restituite le stesse coordinate, indipendentemente dall'impostazione dpi. Se si disegna un controllo in corrispondenza di (100, 100), questo viene disegnato in base a tali coordinate logiche e occuperà la stessa posizione relativa in qualsiasi impostazione dpi.

## <a name="scaling-in-ui-automation-clients"></a>Ridimensionamento nei client di automazione interfaccia utente

L Automazione interfaccia utente API non usa coordinate logiche. I metodi e le proprietà seguenti restituiscono coordinate fisiche o accettano le coordinate fisiche come parametri.

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement::GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment::BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

Per impostazione predefinita, Automazione interfaccia utente applicazioni in esecuzione in un ambiente non impostato su 96 dpi non o ottengono risultati corretti da questi metodi e proprietà. Ad esempio, poiché la posizione del cursore si trova in coordinate logiche, il client non può passare queste coordinate a [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) per ottenere l'elemento che si trova sotto il cursore. Inoltre, l'applicazione non sarà in grado di posizionare correttamente le finestre al di fuori dell'area client.

La soluzione è in due parti.

Prima di tutto, rendere l'applicazione client in grado di riconoscere dpi. A tale scopo, chiamare la [**funzione SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) all'avvio. Questa funzione rende l'intero processo in grado di riconoscere dpi, ovvero tutte le finestre che appartengono al processo non vengono ridimensionate.

In secondo momento, per ottenere le coordinate del cursore, [**chiamare la funzione GetPhysicalCursorPos.**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos)

 

 