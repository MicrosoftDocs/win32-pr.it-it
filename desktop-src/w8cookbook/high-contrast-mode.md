---
title: Modalità a contrasto elevato
description: Modalità a contrasto elevato
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a288447dda8d3a76278ad695459d2c15598b328
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883901"
---
# <a name="high-contrast-mode"></a>Modalità a contrasto elevato

## <a name="platforms"></a>Piattaforme

 **Client** - Windows 8  
**Server** - Windows Server 2012  



## <a name="description"></a>Descrizione

Nei sistemi Windows precedenti, la modalità a contrasto elevato era limitata ai temi in esecuzione nei temi classici, che non avevano uno stile visivo. In Windows 8 e Windows Server 2012 la modalità classica è stata rimossa e sostituita con temi a contrasto elevato con stile visivo. Uno dei vantaggi principali di questa modifica è la rimozione di un percorso di codice separato per le app in esecuzione in modalità classica.

Gli sviluppatori devono comunque essere educati sul modo in cui la modalità a contrasto elevato può influire sulla propria app e su come sviluppare un'app realmente indipendente dagli stili. Questo è importante perché, anche se l'uso non corretto o il presupposto dei colori del tema può causare un comportamento corretto delle app in uno stile di visualizzazione come Aero, queste stesse app rispondono in modo non corretto a contrasto elevato. Ad esempio, in Aero il testo è sempre nero e il colore di evidenziazione è blu chiaro. Nel nero a contrasto elevato, tuttavia, il colore di evidenziazione è nero. Se si presuppone il testo nero, come è stato fatto in molte app predefinite prima di Windows 8 e si usa l'impostazione predefinita del sistema per l'evidenziazione, l'utente visualizza il testo nero su uno sfondo nero. In queste situazioni è necessario comprendere come usare correttamente i temi e le metriche di sistema in modo che l'app sia corretta in tutti gli stili.

## <a name="manifestations"></a>Manifestazioni

-   Il testo non è abilitato nell'area client delle app che non contengono un tag Windows 8 &lt; &gt; supportedOS nel manifesto dell'app. Pertanto, le app devono eseguire il rendering dell'area client usando il percorso del codice necessario per il rendering in modalità a contrasto elevato del tema classico.
-   Il tema non è abilitato nelle aree non client e client delle app con temi a contrasto elevato. Non è inoltre abilitato nelle app che non contengono un tag Windows 8 supportedOS nel manifesto dell'app e che disegnano nell'area non client di una finestra usando &lt; &gt; l'API DwnIsCompositionEnabled(). Il rendering dell'intera app viene eseguito in modalità a contrasto elevato del tema classico.
-   Le app che aggiungono il supporto per Windows 8 nel manifesto, ma non usano gli stili di visualizzazione per il rendering, ad esempio codificano i colori o le immagini nelle app, potrebbero non essere visualizzate correttamente nei temi a contrasto elevato. Il testo potrebbe essere difficile da leggere o le immagini potrebbero non essere visualizzate come dovrebbero in modalità a contrasto elevato.

## <a name="mitigation"></a>Strategia di riduzione del rischio

I colori del testo nei temi a contrasto elevato sono stati creati per essere conformi alle linee guida per l'accessibilità Microsoft. Viene mantenuto un rapporto di contrasto elevato di 14:1 tra primo piano e sfondo. Se i colori abilitati per impostazione predefinita non sono adatti a un particolare utente finale, possono essere facilmente personalizzati tramite le impostazioni del pannello di controllo per "Colore finestra" in questi temi a contrasto elevato.

Questi componenti dell'interfaccia utente sono personalizzabili nei temi a contrasto elevato:

-   Colore di sfondo della finestra
-   Colore del testo
-   Colore dei collegamenti ipertestuali
-   Testo disabilitato
-   Colori primo piano e sfondo del testo selezionato
-   Colori di primo piano e sfondo del titolo della finestra attiva
-   Colori di primo piano e sfondo del titolo della finestra inattiva
-   Colori primo piano e sfondo dei pulsanti

## <a name="solution"></a>Soluzione

Se si verifica un comportamento imprevisto nelle app con temi a contrasto elevato, una di queste soluzioni potrebbe essere utile:

-   **Manifesting an app for Windows 8:**

    Per le app che non contengono Windows 8 tag supportedOS nel manifesto dell'app verrà eseguito il rendering delle aree &lt; &gt; client senza un tema. Le app predefinite devono contenere tutte questa voce nel manifesto dell'app. Aggiungere il valore GUID 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38 per Windows 8.

-   **Uso degli stili di visualizzazione con le informazioni utente disegnate dal proprietario:**

    I controlli disegnati dal proprietario devono seguire le istruzioni in [MSDN per](/windows/desktop/Controls/using-visual-styles) il rendering corretto di parti e stati del controllo, incluso il testo. Gli sviluppatori non devono basarsi sul testo o sul colore di sfondo specificato in un contesto di dispositivo per usare metodi non UxTheme per il rendering. Nel caso in cui non sia presente alcuna parte del tema per il [](/windows/desktop/api/winuser/nf-winuser-getsyscolor) controllo in questione, usare GetThemeSysColor con la metrica appropriata e disegnare il testo usando i metodi GDI standard. Se nessuna delle chiamate UxTheme è appropriata, usare il metodo GetSysColor per ottenere la metrica appropriata.

-   **Selezione del colore del testo:**

    Non usare un colore di testo hardcoded, anche se si presuppone che sia molto utile in tutti gli scenari comuni. I temi di spedizione vengono creati in modo da supportare una visibilità elevata con le metriche associate. Ad esempio, COLOR HIGHLIGHTTEXT deve essere usato con COLOR HIGHLIGHT come sfondo e COLOR WINDOWTEXT deve essere usato con \_ \_ COLOR WINDOW come \_ \_ sfondo. Se sono presenti eccezioni a queste associazioni, è possibile usare tali associazioni nelle parti del tema e nelle definizioni di stato stesse e non nel codice. Quando si progettano le interfaccia utente a contrasto elevato, è fondamentale che l'interfaccia utente sia indipendente dal tema a contrasto elevato attualmente applicato, in quanto gli utenti a contrasto elevato possono personalizzare i colori.

-   **Risposta \_ all'evento ThemeChange wm:**

    Se l'app memorizza nella cache i colori recuperati dal tema o applica i colori in modo non standard, aggiungere un gestore di messaggi per WM THEMECHANGE che ricalcola i valori dei colori archiviati e ridisegna l'interfaccia \_ utente.

-   **Scrittura di un'app WWA a contrasto elevato:**

    Le app Web non hanno accesso alle API UxTheme, ma devono comunque essere scritte con le metriche di sistema correnti come base per l'interfaccia utente. Gli sviluppatori WWA possono sfruttare alcune risorse per garantire un'app conforme a contrasto elevato:

    -   La [specifica W3C CSS Color](https://www.w3.org/TR/css3-color/) specifica la sintassi per l'uso di metriche di sistema anziché colori specifici
    -   È in corso l'aggiunta del supporto per le query multimediali a contrasto elevato Internet Explorer 10
    -   I WWA possono sfruttare il metodo IAccessibilityCapabilities::get \_ HighContrast() per controllare lo stato di contrasto elevato

    Windows Le app dello Store non presentano molti degli stessi problemi con le parti del tema presenti nelle applicazioni Windows classiche, ma è comunque necessario garantire la conformità a contrasto elevato. Per impostazione predefinita, Internet Explorer alcuni stili definiti dall'utente e li sostituisce con valori conformi a contrasto elevato. Ad esempio, le proprietà CSS background-image, background e color vengono ignorate.

    Se non si vuole che Internet Explorer ignori le proprietà impostate e si sia verificato che l'interfaccia utente sia conforme a contrasto elevato, è possibile impostare la nuova proprietà CSS M3 –ms-high-contrast: off per un elemento padre.

-   **Scrittura di un'app Windows Store a contrasto elevato:**

    Windows L'app dello Store deve usare la classe [SystemColors](/dotnet/api/system.windows.systemcolors) per determinare la colorazione corretta degli elementi dell'interfaccia utente, tenendo presente che alcuni colori delle metriche di sistema sono progettati per essere usati in combinazione, ad esempio SystemColors.WindowColor e SystemColors.WindowTextColor. Ciò facilita un'esperienza di contrasto elevato superiore.

-   **Rilevamento corretto del contrasto elevato nelle versioni precedenti di Windows:**

    Le app in esecuzione nelle versioni precedenti Windows non hanno accesso ai nuovi temi a contrasto elevato, anche se il manifesto specifica la compatibilità con la versione di Windows in questione. Di conseguenza, potrebbe essere necessario inserire percorsi di codice aggiuntivi per gestire il rendering nell'ambiente classico usato nelle versioni precedenti di Windows. La presenza di contrasto elevato in questo caso deve essere controllata chiamando la funzione [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il flag SPI \_ GETHIGHCONTRAST. Questo è l'unico modo supportato per controllare la presenza di contrasto elevato.

## <a name="tests"></a>Test

Durante il test di un'app, assicurarsi che il rendering venga eseguito correttamente in tutti i temi predefiniti forniti da Windows 8: Aero, Basic, Contrasto elevato 1, Contrasto elevato 2, Contrasto elevato Black e Contrasto elevato White. Assicurarsi che il testo sia chiaramente visibile e facile da leggere nei temi a contrasto elevato.

## <a name="resources"></a>Risorse

-   [Classi, parti e](../controls/aero-style-classes-parts-and-states.md) stati in stile Aero (anche il nuovo tema di base e i temi a contrasto elevato usano questi stati)
-   [Parti e stati comuni a tutti gli stili di visualizzazione](../controls/parts-and-states.md)
-   [Uso degli stili di visualizzazione con controlli personalizzati Owner-Drawn personalizzati](../controls/using-visual-styles.md)
-   [Funzione GetSysColor](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [Modulo colori CSS W3C livello 3](https://www.w3.org/TR/css3-color/)
-   [Classe SystemColors](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [Funzione SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Accessibilità Microsoft](https://www.microsoft.com/enable/)

 

 
