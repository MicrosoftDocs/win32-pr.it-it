---
title: Informazioni sui cursori
description: In questo argomento vengono illustrati i cursori standard.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- risorse, cursori
- cursori, informazioni
- cursori, standard
- cursori standard
- Funzione SetSystemCursor (funzione)
- cursori, personalizzati
- cursori personalizzati
- cursori, aree sensibili
- cursori, creazione
- creazione di cursori
- cursori, posizione
- cursori, aspetto
- eliminazione definitiva di cursori
- duplicazione di cursori
- cursore classe
- limitazione di cursori
- cursori, distruzione
- cursori, duplicazione
- cursori, classe
- cursori, limitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d0b91ba4670d2510413240efd742b2e0ba69b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046699"
---
# <a name="about-cursors"></a>Informazioni sui cursori

Windows fornisce un set di cursori standard disponibili per qualsiasi applicazione da utilizzare in qualsiasi momento. I file di intestazione dell'SDK contengono gli identificatori per i cursori standard: gli identificatori iniziano con il prefisso **IDC \_** .

A ogni cursore standard è associata un'immagine predefinita. L'utente o un'applicazione può sostituire l'immagine predefinita associata a qualsiasi cursore standard in qualsiasi momento. Un'applicazione sostituisce un'immagine predefinita tramite la funzione [**funzione SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) . Nella figura seguente vengono illustrati diversi cursori standard di Windows Vista:

![cursori standard, tra cui la mano, il segno più a quattro frecce, la freccia con il punto interrogativo, il cerchio, la penna](images/cursorsstandard.png)

Un'applicazione può utilizzare la funzione [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) per recuperare l'immagine corrente per un cursore e può creare il cursore utilizzando la funzione [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) . Per creare l'immagine predefinita per un cursore standard, specificare il flag **di \_ compatibilità** con nella chiamata a **DrawIconEx**. Se non si specifica il flag **di \_ compatibilità** con, **DrawIconEx** disegna il cursore standard usando l'immagine specificata dall'utente.

I cursori personalizzati sono progettati per l'uso in un'applicazione specifica e possono essere qualsiasi progetto definito dallo sviluppatore. Nella figura seguente vengono illustrati diversi cursori personalizzati.

![cursori personalizzati, tra cui Hand, banana, Drum, orologio a mano, metronomo](images/cursorscustom.png)

I cursori possono essere di tipo monocromatico o colore e statici o animati. Il tipo di cursore utilizzato in un determinato computer dipende dalla visualizzazione del sistema. Gli schermi precedenti, ad esempio VGA, non supportano il colore o i cursori animati. Nuovi display, i cui driver di visualizzazione usano il motore di bitmap indipendente dal dispositivo (DIB), li supportano.

I cursori e le icone sono simili e possono essere usati in modo interscambiabile in molte situazioni. L'unica differenza tra di esse è che un'immagine specificata come cursore deve essere nel formato che la visualizzazione può supportare. Un cursore, ad esempio, deve essere monocromatico per una visualizzazione VGA.

In questa panoramica vengono fornite informazioni sui seguenti argomenti:

-   [Area sensibile](#the-hot-spot)
-   [Il mouse e il cursore](#the-mouse-and-the-cursor)
-   [Creazione di cursori](#cursor-creation)
-   [Posizione e aspetto del cursore](#cursor-location-and-appearance)
-   [Ottimizzazione del cursore](#cursor-confinement)
-   [Distruzione del cursore](#cursor-destruction)
-   [Duplicazione del cursore](#cursor-duplication)
-   [Cursore della classe della finestra](#the-window-class-cursor)

## <a name="the-hot-spot"></a>Area sensibile

Nel cursore, un pixel chiamato area sensibile *contrassegna l'* esatta posizione dello schermo interessata da un evento del mouse, ad esempio facendo clic su un pulsante del mouse. In genere, l'area sensibile è il punto focale del cursore. Il sistema rileva e riconosce questo punto come posizione del cursore. Ad esempio, le aree sensibili tipiche sono il pixel alla punta di un cursore a forma di freccia e il pixel al centro di un cursore a forma di mirino. Nelle immagini seguenti vengono illustrati due cursori di un programma di disegno, in cui le aree sensibili sono associate alla punta del pennello e il mirino della pittura può essere.

![punti sensibili su due cursori](images/cursorhotspot.png)

Quando si verifica un evento di input del mouse, il driver del mouse converte l'evento in un messaggio del mouse appropriato che include le coordinate dell'area sensibile. Il sistema invia il messaggio del mouse alla finestra che contiene l'area sensibile o alla finestra che acquisisce l'input del mouse. Per ulteriori informazioni, vedere [input del mouse](/windows/desktop/inputdev/mouse-input).

## <a name="the-mouse-and-the-cursor"></a>Il mouse e il cursore

Il sistema riflette lo spostamento del mouse spostando di conseguenza il cursore sullo schermo. Quando il cursore si sposta su diverse parti di Windows o in finestre diverse, il sistema (o un'applicazione) modifica l'aspetto del cursore. Quando, ad esempio, il cursore attraversa un collegamento ipertestuale, il cursore passa da una freccia a una mano.

![cursore standard che passa a una mano quando viene posizionato su un collegamento ipertestuale](images/cursorchangingstate.png)

Se il sistema non dispone di un mouse, il sistema Visualizza e sposta il cursore solo quando l'utente sceglie determinati comandi di sistema, ad esempio quelli utilizzati per ridimensionare o spostare una finestra. Per fornire all'utente un metodo di visualizzazione e spostamento del cursore quando il mouse non è disponibile, un'applicazione può utilizzare le funzioni del cursore per simulare il movimento del mouse. Data questa funzionalità di simulazione, l'utente può utilizzare i tasti di direzione per spostare il cursore.

## <a name="cursor-creation"></a>Creazione di cursori

Poiché i cursori standard sono predefiniti, non è necessario crearli. Per utilizzare un cursore standard, un'applicazione recupera un handle del cursore utilizzando la funzione [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) . Un *handle del cursore* è un valore univoco del tipo **hCursor** che identifica un cursore standard o personalizzato.

Per creare un cursore personalizzato per un'applicazione, si usa in genere un'applicazione grafica e si include il cursore come risorsa nel file di definizione delle risorse dell'applicazione. In fase di esecuzione, chiamare [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) per recuperare l'handle del cursore. Le risorse del cursore contengono dati per diversi dispositivi di visualizzazione. La funzione **LoadCursor** seleziona automaticamente i dati più appropriati per il dispositivo di visualizzazione corrente. Per caricare un cursore direttamente da un oggetto. CUR o. File ANI, usare la funzione [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea) .

È anche possibile creare un cursore personalizzato in fase di esecuzione usando la funzione [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , che crea un cursore in base al contenuto di una struttura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . La funzione [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) riempie questa struttura con le coordinate di area sensibile e le informazioni relative alla maschera e al colore associati.

Le applicazioni devono implementare cursori personalizzati come risorse e usare [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) anziché creare il cursore in fase di esecuzione. L'utilizzo delle risorse del cursore evita la dipendenza del dispositivo, semplifica la localizzazione e consente alle applicazioni di condividere le progettazioni dei cursori.

La funzione [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) consente a un'applicazione di creare icone e cursori in base ai dati delle risorse. **CreateIconFromResourceEx** crea un cursore basato sui dati di risorsa binari da altri file eseguibili (exe) o dll. Deve essere preceduto dalle chiamate alla funzione [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) , nonché da diverse funzioni di risorsa. **LookupIconIdFromDirectoryEx** identifica i dati di cursore più appropriati per il dispositivo di visualizzazione corrente. Per ulteriori informazioni sulle funzioni delle risorse, vedere [risorse](resources.md).

## <a name="cursor-location-and-appearance"></a>Posizione e aspetto del cursore

Il sistema visualizza automaticamente un cursore per il mouse e ne aggiorna la posizione sullo schermo. È possibile ottenere le coordinate dello schermo correnti del cursore e spostare il cursore in qualsiasi posizione sullo schermo usando rispettivamente le funzioni [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) e [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) .

È inoltre possibile recuperare l'handle per il cursore corrente utilizzando la funzione [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) ed è possibile impostare il cursore utilizzando la funzione [**secursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) . Dopo **aver chiamato il cursore,** l'aspetto del cursore non cambia fino a quando non si sposta il mouse, il cursore viene impostato in modo esplicito su un cursore diverso o viene eseguito un comando di sistema.

Quando l'utente sposta il mouse, il sistema ridisegnato il cursore nella nuova posizione. Il sistema ridisegna automaticamente la progettazione del cursore associata alla finestra a cui punta il cursore.

È possibile nascondere e visualizzare nuovamente il cursore senza modificare la progettazione del cursore utilizzando la funzione [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor) . Questa funzione utilizza un contatore interno per determinare quando nascondere o visualizzare il cursore. Un tentativo di visualizzare il cursore Incrementa il contatore; un tentativo di nascondere il cursore decrementa il contatore. Il cursore è visibile solo se il contatore è maggiore o uguale a zero.

La funzione [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) ottiene le informazioni seguenti per il cursore globale: se il cursore è nascosto o visualizzato, l'handle per il cursore e le coordinate del cursore.

## <a name="cursor-confinement"></a>Ottimizzazione del cursore

È possibile limitare il cursore a un'area rettangolare sullo schermo usando la funzione [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) . Questa operazione è utile quando l'utente deve rispondere a un determinato evento all'interno dell'area confinata del rettangolo. Ad esempio, è possibile utilizzare **ClipCursor** per limitare il cursore a una finestra di dialogo modale, evitando che l'utente interagisca con altre finestre fino alla chiusura della finestra di dialogo.

La funzione [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) recupera le coordinate dello schermo dell'area rettangolare a cui è temporaneamente limitato il cursore. Quando è necessario limitare il cursore, è possibile utilizzare questa funzione anche per salvare le coordinate dell'area originale in cui è possibile spostare il cursore. Quindi, è possibile ripristinare il cursore nell'area originale quando il nuovo periodo di ottimizzazione non è più necessario.

## <a name="cursor-destruction"></a>Distruzione del cursore

È possibile eliminare l'handle del cursore e liberare la memoria usata dal cursore chiamando la funzione [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) . Questa funzione, tuttavia, non ha alcun effetto su un cursore condiviso. Un cursore condiviso è valido fino a quando il modulo da cui è stato caricato rimane in memoria. Le funzioni seguenti ottengono un cursore condiviso:

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (se si usa il flag di **\_ condivisione LR** )
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (se si usa il flag **LR \_ COPYRETURNORG** e *hImage* è un cursore condiviso)

Quando non è più necessario un cursore creato tramite la funzione [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , è necessario eliminare il cursore. La funzione [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) Elimina il punto di manipolazione del cursore e libera la memoria usata dal cursore. Utilizzare questa funzione solo nei cursori creati con **CreateIconIndirect**.

## <a name="cursor-duplication"></a>Duplicazione del cursore

La funzione [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor) copia un handle del cursore. Ciò consente al codice dell'applicazione o della DLL di recuperare l'handle a un cursore di proprietà di un altro modulo. Quindi, se l'altro modulo viene liberato, il modulo che ha copiato il cursore può comunque utilizzare la progettazione del cursore.

Per informazioni su come aggiungere, rimuovere o sostituire le risorse del cursore nei file eseguibili, vedere [risorse](resources.md).

## <a name="the-window-class-cursor"></a>Cursore della classe della finestra

Quando si registra una classe della finestra usando la funzione [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) , è possibile assegnarle un cursore predefinito, noto come *cursore della classe*. Dopo che l'applicazione ha registrato la classe della finestra, ogni finestra della classe ha il cursore della classe specificato.

Per eseguire l'override del cursore della classe, elaborare il messaggio [**WM del \_ cursore**](wm-setcursor.md) . È inoltre possibile sostituire un cursore della classe utilizzando la funzione [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) . Questa funzione modifica le impostazioni predefinite della finestra per tutte le finestre di una classe specificata. Per ulteriori informazioni, vedere [classe Cursor](/windows/desktop/winmsg/about-window-classes).

 

 