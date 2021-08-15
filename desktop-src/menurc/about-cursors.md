---
title: Informazioni sui cursori
description: In questo argomento vengono illustrati i cursori standard.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- risorse, cursori
- cursori, informazioni
- cursori, standard
- cursori standard
- Funzione SetSystemCursor
- cursori, personalizzati
- cursori personalizzati
- cursori, aree sensibili
- cursori, creazione
- creazione di cursori
- cursori, posizione
- cursori, aspetto
- eliminazione di cursori
- duplicazione di cursori
- cursore di classe
- limitazione dei cursori
- cursori, eliminazione
- cursori, duplicazione
- cursors,class
- cursori, limitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8d987eb12857779ac85d34cb7e4ff7f3f5ce59ed8a750764c433c88abbccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735405"
---
# <a name="about-cursors"></a>Informazioni sui cursori

Windows fornisce un set di cursori standard che possono essere utilizzati da qualsiasi applicazione in qualsiasi momento. I file di intestazione DELL'SDK contengono identificatori per i cursori standard. Gli identificatori iniziano con il **prefisso IDC. \_**

A ogni cursore standard è associata un'immagine predefinita. L'utente o un'applicazione può sostituire l'immagine predefinita associata a qualsiasi cursore standard in qualsiasi momento. Un'applicazione sostituisce un'immagine predefinita usando la [**funzione SetSystemCursor.**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) L'immagine seguente mostra diversi cursori standard di Windows Vista:

![cursori standard, tra cui mano, segno più quattro frecce, freccia con punto interrogativo, cerchio, penna](images/cursorsstandard.png)

Un'applicazione può usare [**la funzione GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) per recuperare l'immagine corrente per un cursore e può disegnare il cursore usando la [**funzione DrawIconEx.**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) Per disegnare l'immagine predefinita per un cursore standard, specificare il flag **DI \_ COMPAT** nella chiamata a **DrawIconEx.** Se non si specifica il flag **DI \_ COMPAT,** **DrawIconEx** disegna il cursore standard usando l'immagine specificata dall'utente.

I cursori personalizzati sono progettati per l'uso in un'applicazione specifica e possono essere qualsiasi progettazione definita dallo sviluppatore. Nella figura seguente vengono illustrati diversi cursori personalizzati.

![cursori personalizzati, tra cui mano, banane, pane, controllo a portata di mano, metronome](images/cursorscustom.png)

I cursori possono essere monocromatici o a colori e statici o animati. Il tipo di cursore utilizzato in un computer specifico dipende dalla visualizzazione del sistema. I vecchi schermi, ad esempio VGA, non supportano i cursori a colori o animati. I nuovi display, i cui driver di visualizzazione usano il motore DIB (Device Independent Bitmap), li supportano.

I cursori e le icone sono simili e possono essere usati in modo intercambiabile in molte situazioni. L'unica differenza è che un'immagine specificata come cursore deve essere nel formato supportato dalla visualizzazione. Ad esempio, un cursore deve essere monocromatico per una visualizzazione VGA.

In questa panoramica vengono fornite informazioni sugli argomenti seguenti:

-   [Area sensibile](#the-hot-spot)
-   [Mouse e cursore](#the-mouse-and-the-cursor)
-   [Creazione di cursori](#cursor-creation)
-   [Posizione e aspetto del cursore](#cursor-location-and-appearance)
-   [Cursor Confinement](#cursor-confinement)
-   [Distruzione del cursore](#cursor-destruction)
-   [Duplicazione dei cursori](#cursor-duplication)
-   [Cursore della classe Window](#the-window-class-cursor)

## <a name="the-hot-spot"></a>Area sensibile

Nel cursore un pixel  denominato area sensibile contrassegna la posizione esatta dello schermo interessata da un evento del mouse, ad esempio facendo clic su un pulsante del mouse. In genere, l'area sensibile è il punto focale del cursore. Il sistema tiene traccia di questo punto e lo riconosce come posizione del cursore. Ad esempio, le aree sensibili tipiche sono il pixel alla punta di un cursore a freccia e il pixel al centro di un cursore a forma di mirino. Le immagini seguenti illustrano due cursori di un programma di disegno, in cui le aree sensibili sono associate alla punta del pennello e al mirino del pennello.

![aree sensibili su due cursori](images/cursorhotspot.png)

Quando si verifica un evento di input del mouse, il driver del mouse converte l'evento in un messaggio del mouse appropriato che include le coordinate dell'area sensibile. Il sistema invia il messaggio del mouse alla finestra che contiene l'area sensibile o alla finestra che acquisisce l'input del mouse. Per altre informazioni, vedere [Input del mouse.](/windows/desktop/inputdev/mouse-input)

## <a name="the-mouse-and-the-cursor"></a>Mouse e cursore

Il sistema riflette lo spostamento del mouse spostando di conseguenza il cursore sullo schermo. Quando il cursore si sposta su diverse parti di finestre o in finestre diverse, il sistema (o un'applicazione) modifica l'aspetto del cursore. Ad esempio, quando il cursore si incrocia su un collegamento ipertestuale, il sistema cambia il cursore da una freccia a una mano.

![cursore standard che cambia in mano quando si trova su un collegamento ipertestuale](images/cursorchangingstate.png)

Se il sistema non dispone di un mouse, il sistema visualizza e sposta il cursore solo quando l'utente sceglie determinati comandi di sistema, ad esempio quelli usati per ridimensionare o spostare una finestra. Per fornire all'utente un metodo per visualizzare e spostare il cursore quando il mouse non è disponibile, un'applicazione può usare le funzioni del cursore per simulare lo spostamento del mouse. Data questa funzionalità di simulazione, l'utente può usare i tasti di direzione per spostare il cursore.

## <a name="cursor-creation"></a>Creazione di cursori

Poiché i cursori standard sono predefiniti, non è necessario crearli. Per usare un cursore standard, un'applicazione recupera un handle di cursore usando la [**funzione LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) [**o LoadImage.**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) Un *handle di cursore* è un valore univoco del **tipo HCURSOR** che identifica un cursore standard o personalizzato.

Per creare un cursore personalizzato per un'applicazione, in genere si usa un'applicazione grafica e si include il cursore come risorsa nel file di definizione delle risorse dell'applicazione. In fase di esecuzione chiamare [**LoadCursor per**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) recuperare l'handle del cursore. Le risorse cursore contengono dati per diversi dispositivi di visualizzazione. La **funzione LoadCursor** seleziona automaticamente i dati più appropriati per il dispositivo di visualizzazione corrente. Per caricare un cursore direttamente da un oggetto . CUR o . File ANI, usare la [**funzione LoadCursorFromFile.**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)

È anche possibile creare un cursore personalizzato in fase di esecuzione usando la funzione [**CreateIconIndirect,**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) che crea un cursore basato sul contenuto di una [**struttura ICONINFO.**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) La [**funzione GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) riempie questa struttura con coordinate dell'area sensibile e informazioni relative alla maschera e al colore associati.

Le applicazioni devono implementare cursori personalizzati come risorse e usare [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) anziché creare il cursore in fase di esecuzione. L'uso delle risorse cursore consente di evitare la dipendenza del dispositivo, semplifica la localizzazione e consente alle applicazioni di condividere le progettazioni dei cursori.

La [**funzione CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) consente a un'applicazione di creare icone e cursori in base ai dati delle risorse. **CreateIconFromResourceEx** crea un cursore basato su dati di risorse binari da altri file eseguibili (.exe) o DLL. Deve essere preceduto da chiamate alla [**funzione LookupIconIdFromDirectoryEx,**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) nonché da diverse funzioni di risorsa. **LookupIconIdFromDirectoryEx** identifica i dati del cursore più appropriati per il dispositivo di visualizzazione corrente. Per altre informazioni sulle funzioni delle risorse, vedere [Risorse.](resources.md)

## <a name="cursor-location-and-appearance"></a>Posizione e aspetto del cursore

Il sistema visualizza automaticamente un cursore per il mouse e ne aggiorna la posizione sullo schermo. È possibile ottenere le coordinate correnti dello schermo del cursore e spostare il cursore in qualsiasi posizione sullo schermo usando rispettivamente le funzioni [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) e [**SetCursorPos.**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)

È anche possibile recuperare l'handle per il cursore corrente usando la [**funzione GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) ed è possibile impostare il cursore usando la [**funzione SetCursor.**](/windows/desktop/api/Winuser/nf-winuser-setcursor) Dopo aver chiamato **SetCursor**, l'aspetto del cursore non cambia fino a quando il mouse non viene spostato, il cursore non viene impostato in modo esplicito su un cursore diverso o non viene eseguito un comando di sistema.

Quando l'utente sposta il mouse, il sistema ridisegna il cursore in corrispondenza della nuova posizione. Il sistema ridisegna automaticamente la struttura del cursore associata alla finestra a cui punta il cursore.

È possibile nascondere e visualizzare nuovamente il cursore, senza modificare la progettazione del cursore, usando la [**funzione ShowCursor.**](/windows/desktop/api/Winuser/nf-winuser-showcursor) Questa funzione usa un contatore interno per determinare quando nascondere o visualizzare il cursore. Un tentativo di visualizzare il cursore incrementa il contatore. Un tentativo di nascondere il cursore decrementa il contatore. Il cursore è visibile solo se questo contatore è maggiore o uguale a zero.

La [**funzione GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) ottiene le informazioni seguenti per il cursore globale: se il cursore è nascosto o visualizzato, l'handle per il cursore e le coordinate del cursore.

## <a name="cursor-confinement"></a>Cursor Confinement

È possibile limitare il cursore a un'area rettangolare sullo schermo usando la [**funzione ClipCursor.**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) Ciò è utile quando l'utente deve rispondere a un determinato evento all'interno dell'area limitata del rettangolo. Ad esempio, è possibile usare **ClipCursor** per limitare il cursore a una finestra di dialogo modale, impedendo all'utente di interagire con altre finestre fino alla chiusura della finestra di dialogo.

La [**funzione GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) recupera le coordinate dello schermo dell'area rettangolare a cui è temporaneamente limitato il cursore. Quando è necessario limitare il cursore, è anche possibile usare questa funzione per salvare le coordinate dell'area originale in cui il cursore può essere spostato. È quindi possibile ripristinare il cursore nell'area originale quando il nuovo confine non è più necessario.

## <a name="cursor-destruction"></a>Distruzione del cursore

È possibile eliminare l'handle del cursore e liberare la memoria usata dal cursore chiamando la [**funzione DestroyCursor.**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) Tuttavia, questa funzione non ha alcun effetto su un cursore condiviso. Un cursore condiviso è valido purché il modulo da cui è stato caricato rimanga in memoria. Le funzioni seguenti ottengono un cursore condiviso:

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (se si usa il flag **LR \_ SHARED)**
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (se si usa il flag **\_ LR COPYRETURNORG** e *hImage* è un cursore condiviso)

Quando un cursore creato con la funzione [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) non è più necessario, è necessario eliminare il cursore. La [**funzione DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) elimina l'handle di cursore e libera la memoria utilizzata dal cursore. Usare questa funzione solo sui cursori creati con **CreateIconIndirect.**

## <a name="cursor-duplication"></a>Duplicazione dei cursori

La [**funzione CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor) copia un handle di cursore. In questo modo il codice dell'applicazione o della DLL può recuperare l'handle per un cursore di proprietà di un altro modulo. Quindi, se l'altro modulo viene liberato, il modulo che ha copiato il cursore può comunque usare la progettazione del cursore.

Per informazioni su come aggiungere, rimuovere o sostituire risorse cursore nei file eseguibili, vedere [Risorse.](resources.md)

## <a name="the-window-class-cursor"></a>Cursore della classe Window

Quando si registra una classe di finestra usando la [**funzione RegisterClass,**](/windows/desktop/api/winuser/nf-winuser-registerclassa) è possibile assegnarle un cursore predefinito, noto come *cursore di classe.* Dopo che l'applicazione ha registrato la classe della finestra, ogni finestra di tale classe ha il cursore di classe specificato.

Per eseguire l'override del cursore della classe, [**elaborare il messaggio WM \_ SETCURSOR.**](wm-setcursor.md) È anche possibile sostituire un cursore di classe usando la [**funzione SetClassLong.**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) Questa funzione modifica le impostazioni predefinite della finestra per tutte le finestre di una classe specificata. Per altre informazioni, vedere [Cursore di classe.](/windows/desktop/winmsg/about-window-classes)

 

 