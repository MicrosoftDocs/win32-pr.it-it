---
title: Active Accessibility e Windows ridimensionamento dello schermo di Vista
description: Windows Vista consente agli utenti di modificare l'impostazione punti per pollice (dpi) in modo che la maggior parte degli elementi dell'interfaccia utente sullo schermo appaia più grande.
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acf9c1ff6755507541c08b34e183dd751e0941fc646a1f691e4488884e572c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327061"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Active Accessibility e Windows ridimensionamento dello schermo di Vista

Windows Vista consente agli utenti di modificare l'impostazione punti per pollice (dpi) in modo che la maggior parte degli elementi dell'interfaccia utente sullo schermo appaia più grande. Anche se questa funzionalità è stata a lungo disponibile in Microsoft Windows, nelle versioni precedenti il ridimensionamento doveva essere implementato dalle applicazioni. In Windows Vista, il Gestione finestre desktop esegue il ridimensionamento predefinito per tutte le applicazioni che non gestiscono il ridimensionamento. Microsoft Active Accessibility applicazioni client devono prendere in considerazione questa funzionalità.

## <a name="scaling-in-windows-vista"></a>Ridimensionamento in Windows Vista

L'impostazione dpi predefinita è 96, ovvero 96 pixel occupano una larghezza o un'altezza di un pollice nozionale. La misura esatta di un pollice dipende dalle dimensioni e dalla risoluzione fisica del monitor. Ad esempio, su un monitor con una larghezza di 12 pollici e una risoluzione orizzontale di 1280 pixel, una riga orizzontale di 96 pixel si estende per circa 9/10 di un pollice.

La modifica dell'impostazione dpi non corrisponde alla modifica della risoluzione dello schermo. Con il ridimensionamento dpi, il numero di pixel fisici sullo schermo rimane invariato. Tuttavia, il ridimensionamento viene applicato alle dimensioni e alla posizione degli elementi dell'interfaccia utente. È possibile eseguire il ridimensionamento automaticamente con Gestione finestre desktop per il desktop e per le applicazioni che non richiedono tale funzionalità in modo esplicito.

In effetti, quando l'utente imposta il fattore di scala su 120 dpi, un pollice verticale o orizzontale sullo schermo diventa più grande del 25%. Tutte le dimensioni vengono ridimensionate di conseguenza. L'offset di una finestra dai bordi superiore e sinistro dello schermo aumenta del 25%. Le dimensioni della finestra aumentano nella stessa proporzione, insieme agli offset e alle dimensioni di tutti gli elementi dell'interfaccia utente in essa contenuti.

Per impostazione predefinita, DWM non esegue il ridimensionamento per le applicazioni che non supportano dpi quando l'utente imposta il valore dpi su 120, ma lo esegue quando il valore dpi è impostato su un valore personalizzato pari a 144 o superiore. È tuttavia possibile ignorare questo comportamento predefinito.

Il ridimensionamento dello schermo crea nuove sfide per le applicazioni che dipendono dalle coordinate dello schermo. Lo schermo contiene ora due sistemi di coordinate: fisico e logico. Le coordinate fisiche di un punto sono l'offset effettivo in pixel dalla parte superiore sinistra dell'origine. Le coordinate logiche sono gli offset così come si presenterebbero se i pixel fossero ridimensionati.

Si supponga di progettare una finestra di dialogo con un pulsante in corrispondenza delle coordinate (100, 48). Quando questa finestra di dialogo viene visualizzata con il valore predefinito di 96 dpi, il pulsante si trova in corrispondenza delle coordinate fisiche (100, 48). A 120 dpi, si trova in corrispondenza delle coordinate fisiche (125, 60). Ma le coordinate logiche sono le stesse in qualsiasi impostazione dpi: (100, 48).

Le coordinate logiche sono importanti perché rendono coerente il comportamento del sistema operativo e delle applicazioni indipendentemente dall'impostazione dpi. Ad esempio, **System.Windows. Forms.Cursor.Position** restituisce in genere le coordinate logiche. Se si sposta il cursore su un elemento di una finestra di dialogo, vengono restituite le stesse coordinate indipendentemente dall'impostazione dpi. Se si disegna un controllo in corrispondenza di (100, 100), questo viene disegnato in base a tali coordinate logiche e occuperà la stessa posizione relativa in qualsiasi impostazione dpi.

## <a name="scaling-in-active-accessibility-clients"></a>Ridimensionamento in Active Accessibility client

Microsoft Active Accessibility non usa coordinate logiche. I metodi e le funzioni seguenti restituiscono coordinate fisiche o le accettano come parametri.

-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

Per impostazione predefinita, Microsoft Active Accessibility'applicazione client in esecuzione in un ambiente diverso da 96 dpi non sarà in grado di ottenere risultati corretti da queste chiamate. Ad esempio, poiché la posizione del cursore si trova in coordinate logiche, il client non può semplicemente passare queste coordinate a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) per ottenere l'elemento che si trova sotto il cursore.

Inoltre, un'applicazione che crea una finestra all'esterno della relativa area client, ad esempio un'applicazione di accessibilità che evidenzia gli elementi dell'interfaccia utente con stato attivo, non creerà la finestra nella posizione corretta dello schermo, perché la finestra verrà posizionata in corrispondenza delle coordinate logiche, non delle coordinate fisiche restituite da [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).

La soluzione è in due parti:

-   Rendere l'applicazione client "in grado di riconoscere dpi". A tale scopo, chiamare la [**funzione SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) all'avvio. Questa funzione rende l'intero processo in grado di riconoscere dpi, ovvero tutte le finestre che appartengono al processo non vengono ridimensionate.
-   Usare funzioni che sono in grado di riconoscere dpi. Ad esempio, per ottenere le coordinate del cursore, chiamare [**la funzione GetPhysicalCursorPos.**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) Non usare [**GetCursorPos**](/windows/win32/api/winuser/nf-winuser-getcursorpos); Il comportamento nelle applicazioni con riconoscere dpi non è definito.

Se l'applicazione esegue la comunicazione tra processi diretta con applicazioni non in grado di riconoscere dpi, è possibile eseguire la conversione tra coordinate logiche e fisiche usando le funzioni [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) e [**LogicalToPhysicalPoint.**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint)

 

 