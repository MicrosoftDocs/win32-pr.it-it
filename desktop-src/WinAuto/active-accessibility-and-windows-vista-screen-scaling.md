---
title: Active Accessibility e il ridimensionamento dello schermo di Windows Vista
description: Windows Vista consente agli utenti di modificare l'impostazione di punti per pollice (dpi) in modo che la maggior parte degli elementi dell'interfaccia utente sullo schermo risulti più grande.
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db8e192dc01d4c7d75f19741cdfac7b3b08d22c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473787"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Active Accessibility e il ridimensionamento dello schermo di Windows Vista

Windows Vista consente agli utenti di modificare l'impostazione di punti per pollice (dpi) in modo che la maggior parte degli elementi dell'interfaccia utente sullo schermo risulti più grande. Sebbene questa funzionalità sia stata a lungo disponibile in Microsoft Windows, nelle versioni precedenti il ridimensionamento doveva essere implementato dalle applicazioni. In Windows Vista, il Gestione finestre desktop esegue il ridimensionamento predefinito per tutte le applicazioni che non gestiscono la scalabilità. Le applicazioni client di Microsoft Active Accessibility devono tenere conto di questa funzionalità.

## <a name="scaling-in-windows-vista"></a>Ridimensionamento in Windows Vista

L'impostazione DPI predefinita è 96, il che significa che 96 pixel occupano una larghezza o un'altezza di un pollice teorico. La misura esatta di un pollice dipende dalle dimensioni e dalla risoluzione fisica del monitor. Ad esempio, su un monitor con una larghezza di 12 pollici e una risoluzione orizzontale di 1280 pixel, una riga orizzontale di 96 pixel si estende per circa 9/10 di un pollice.

La modifica dell'impostazione DPI non corrisponde alla modifica della risoluzione dello schermo. Con il ridimensionamento DPI, il numero di pixel fisici sullo schermo rimane lo stesso. Il ridimensionamento viene tuttavia applicato alle dimensioni e alla posizione degli elementi dell'interfaccia utente. È possibile eseguire il ridimensionamento automaticamente con Gestione finestre desktop per il desktop e per le applicazioni che non richiedono tale funzionalità in modo esplicito.

In effetti, quando l'utente imposta il fattore di scala su 120 dpi, un pollice verticale o orizzontale sullo schermo aumenta del 25%. Tutte le dimensioni vengono ridimensionate di conseguenza. L'offset di una finestra dai bordi superiore e sinistro dello schermo aumenta del 25%. Le dimensioni della finestra aumentano nella stessa proporzione, con gli offset e le dimensioni di tutti gli elementi dell'interfaccia utente che contiene.

Per impostazione predefinita, DWM non esegue la scalabilità per le applicazioni non compatibili con DPI quando l'utente imposta il valore dpi su 120, ma lo esegue quando il valore dpi è impostato su un valore personalizzato pari a 144 o superiore. È tuttavia possibile ignorare questo comportamento predefinito.

Il ridimensionamento dello schermo crea nuove sfide per le applicazioni che dipendono dalle coordinate dello schermo. Lo schermo contiene ora due sistemi di coordinate: fisico e logico. Le coordinate fisiche di un punto sono l'offset effettivo in pixel dalla parte superiore sinistra dell'origine. Le coordinate logiche sono gli offset così come si presenterebbero se i pixel fossero ridimensionati.

Si supponga di progettare una finestra di dialogo con un pulsante in corrispondenza delle coordinate (100, 48). Quando questa finestra di dialogo viene visualizzata sul valore predefinito 96 dpi, il pulsante si trova in corrispondenza delle coordinate fisiche (100, 48). A 120 dpi si trova in corrispondenza delle coordinate fisiche (125, 60). Tuttavia, le coordinate logiche sono le stesse in qualsiasi impostazione dpi: (100, 48).

Le coordinate logiche sono importanti, perché rendono il comportamento del sistema operativo e delle applicazioni coerenti indipendentemente dall'impostazione dpi. Ad esempio, **System. Windows. Forms. Cursor. Position** restituisce normalmente le coordinate logiche. Se si sposta il cursore su un elemento in una finestra di dialogo, le stesse coordinate vengono restituite indipendentemente dall'impostazione dpi. Se si disegna un controllo in (100, 100), questo viene disegnato su queste coordinate logiche e occupa la stessa posizione relativa in qualsiasi impostazione dpi.

## <a name="scaling-in-active-accessibility-clients"></a>Ridimensionamento nei client di Active Accessibility

Microsoft Active Accessibility non utilizza le coordinate logiche. I metodi e le funzioni seguenti restituiscono coordinate fisiche o le accettano come parametri.

-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

Per impostazione predefinita, un'applicazione client di Microsoft Active Accessibility in esecuzione in un ambiente non 96-dpi non sarà in grado di ottenere risultati corretti da queste chiamate. Ad esempio, poiché la posizione del cursore è in coordinate logiche, il client non può semplicemente passare queste coordinate a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) per ottenere l'elemento che si trova sotto il cursore.

Inoltre, un'applicazione che crea una finestra al di fuori dell'area client, ad esempio un'applicazione di accessibilità che evidenzia gli elementi dell'interfaccia utente con lo stato attivo, non creerà la finestra nella posizione dello schermo corretta, perché la finestra sarà posizionata in corrispondenza delle coordinate logiche, non delle coordinate fisiche restituite da [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).

La soluzione è in due parti:

-   Rendere l'applicazione client "compatibile con DPI". A tale scopo, chiamare la funzione [**SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) all'avvio. Questa funzione rende l'intero processo compatibile con dpi, vale a dire che tutte le finestre appartenenti al processo non vengono ridimensionate.
-   Usare funzioni compatibili con i valori dpi. Per ottenere, ad esempio, le coordinate del cursore, chiamare la funzione [**GetPhysicalCursorPos**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) . Non utilizzare [**GetCursorPos**](/windows/win32/api/winuser/nf-winuser-getcursorpos); il comportamento delle applicazioni in grado di riconoscere DPI non è definito.

Se l'applicazione esegue la comunicazione tra processi diretta con applicazioni non compatibili con dpi, è possibile che sia presente una conversione tra coordinate logiche e fisiche usando le funzioni [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) e [**LogicalToPhysicalPoint**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint) .

 

 