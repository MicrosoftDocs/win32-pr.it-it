---
title: Modalità a contrasto elevato
description: Modalità a contrasto elevato
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8c53d3e92bb97dd9e2f5fa34bad9f901920cc7
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730743"
---
# <a name="high-contrast-mode"></a>Modalità a contrasto elevato

## <a name="platforms"></a>Piattaforme

 **Client** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>Descrizione

Nei sistemi operativi Windows precedenti, la modalità a contrasto elevato è stata limitata ai temi eseguiti con i temi classici, che non sono stati creati visivamente. In Windows 8 e Windows Server 2012, la modalità classica è stata rimossa e sostituita con temi a contrasto elevato con stile visivo. Uno dei vantaggi principali di questa modifica è la rimozione di un percorso di codice separato per le app in esecuzione in modalità classica.

Gli sviluppatori devono comunque essere informati in che modo la modalità a contrasto elevato può influire sull'app e su come sviluppare un'app che sia effettivamente indipendente dallo stile. Questo è importante perché, sebbene l'uso errato o il presupposto dei colori del tema possa causare un comportamento corretto delle app in uno stile di visualizzazione, ad esempio Aero, le stesse app rispondono in modo non corretto con un contrasto elevato. Ad esempio, in Aero il testo è sempre nero e il colore di evidenziazione è un blu chiaro. In nero a contrasto elevato, tuttavia, il colore di evidenziazione è nero. Se si presuppone che il testo sia nero, come nel caso di molte app in-box precedenti a Windows 8 e si usa l'impostazione predefinita del sistema per l'evidenziazione, l'utente visualizzerà il testo nero su uno sfondo nero. In queste situazioni è necessario comprendere correttamente come usare i temi e le metriche di sistema in modo che l'app appaia corretta tra gli stili.

## <a name="manifestations"></a>Manifestazioni

-   Il tema non è abilitato nell'area client delle app che non contengono un tag di Windows 8 <supportedOS> nel manifesto dell'applicazione. Pertanto, le app devono eseguire il rendering dell'area client usando il percorso del codice necessario per il rendering in modalità a contrasto elevato del tema classico.
-   I temi non sono abilitati nelle aree client e non client delle app nei temi a contrasto elevato. Non è inoltre abilitato nelle app che non contengono un tag di Windows 8 <supportedOS> nel manifesto dell'applicazione e che si basano sull'area non client di una finestra usando l'API DwnIsCompositionEnabled (). L'intera app esegue il rendering nella modalità a contrasto elevato del tema classico.
-   Le app che aggiungono il supporto per Windows 8 nel manifesto, ma non usano gli stili di visualizzazione per il rendering, ovvero codificano colori o immagini nelle app, potrebbero non essere visualizzate correttamente nei temi a contrasto elevato. Il testo potrebbe essere difficile da leggere oppure le immagini potrebbero non essere visualizzate come in modalità a contrasto elevato.

## <a name="mitigation"></a>Strategia di riduzione del rischio

I colori del testo nei temi a contrasto elevato sono stati creati per essere conformi alle linee guida per l'accessibilità di Microsoft. Viene mantenuto un rapporto a contrasto elevato 14:1 tra primo piano e sfondo. Se i colori abilitati per impostazione predefinita non sono adatti a un determinato utente finale, possono essere facilmente personalizzati tramite le impostazioni del pannello di controllo per il colore della finestra nei temi a contrasto elevato.

Questi componenti dell'interfaccia utente sono personalizzabili nei temi a contrasto elevato:

-   Colore di sfondo della finestra
-   Colore del testo
-   Colore collegamenti ipertestuali
-   Testo disabilitato
-   Colori di sfondo e primo piano del testo selezionato
-   Colore di primo piano e sfondo del titolo della finestra attiva
-   Colore di primo piano e sfondo del titolo della finestra inattiva
-   Colori di primo piano e sfondo del pulsante

## <a name="solution"></a>Soluzione

Se si riscontrano comportamenti imprevisti nelle app con temi a contrasto elevato, una di queste soluzioni può essere utile:

-   **Manifesto di un'app per Windows 8:**

    Le app che non contengono il <supportedOS> tag di Windows 8 nel manifesto dell'applicazione avranno il rendering delle aree client senza un tema. Le app incluse devono contenere tutte questa voce nel manifesto dell'applicazione. Aggiungere il valore GUID 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38 per Windows 8.

-   **Uso degli stili di visualizzazione con le interfacce utente disegnate dal proprietario:**

    I controlli creati dal proprietario devono seguire le istruzioni in [MSDN](/windows/desktop/Controls/using-visual-styles) per il rendering corretto di parti e Stati del controllo, incluso il testo. Gli sviluppatori non devono basarsi sul testo o sul colore di sfondo specificato in un contesto di dispositivo per poter usare metodi non UxTheme per il rendering. Nel caso in cui non esistano parti del tema per il controllo in questione, usare GetThemeSysColor con la [metrica appropriata](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e creare il testo usando i metodi GDI standard. Se nessuna delle chiamate a UxTheme è appropriata, usare il metodo GetSysColor per ottenere la metrica appropriata.

-   **Selezione del colore del testo:**

    Non usare un colore del testo hardcoded, anche se si presuppone che si tratti di un aspetto corretto in tutti gli scenari comuni. I temi di spedizione vengono creati in modo da supportare la visibilità elevata con le metriche associate. Ad esempio, il colore \_ HIGHLIGHTTEXT è progettato per essere usato con \_ l'evidenziazione dei colori come sfondo e il colore \_ WINDOWTEXT deve essere usato con \_ la finestra dei colori come sfondo. Se sono presenti eccezioni a queste associazioni, è possibile utilizzarle nelle parti del tema e nelle definizioni di stato stesse e non nel codice. Quando si progettano interfacce utente a contrasto elevato, è fondamentale che l'interfaccia utente sia agnostica rispetto al tema a contrasto elevato attualmente applicato, in quanto gli utenti a contrasto elevato possono personalizzare i loro colori.

-   **Risposta all' \_ evento ThemeChange di WM:**

    Se l'app memorizza nella cache i colori recuperati dal tema o applica i colori in modo non standard, aggiungere un gestore di messaggi per WM \_ THEMECHANGE che ricalcola i valori dei colori archiviati e ridisegna l'interfaccia utente.

-   **Scrittura di un'app WWA a contrasto elevato:**

    Le app Web non hanno accesso alle API di UxTheme, ma devono comunque essere scritte con le metriche di sistema correnti come base per l'interfaccia utente. Ci sono alcune risorse che gli sviluppatori WWA possono sfruttare per garantire un'app conforme a contrasto elevato:

    -   La [specifica del colore CSS W3C](https://www.w3.org/TR/css3-color/) specifica la sintassi per l'uso delle metriche di sistema anziché dei colori specifici
    -   È in corso l'aggiunta del supporto per le query di supporto a contrasto elevato a Internet Explorer 10
    -   WWAs può sfruttare il metodo IAccessibilityCapabilities:: Get \_ HighContrast () per verificare lo stato del contrasto elevato

    Le app di Windows Store non hanno molti degli stessi problemi con le parti del tema presenti nelle applicazioni Windows classiche, ma è comunque necessario garantire una conformità a contrasto elevato. Per impostazione predefinita, Internet Explorer ignora alcuni stili definiti dall'utente e li sostituisce con valori conformi a contrasto elevato. Ad esempio, le proprietà CSS background-image, background e Color vengono ignorate.

    Se non si desidera che Internet Explorer ignori le proprietà impostate ed è stato verificato che l'interfaccia utente sia conforme a contrasto elevato, è possibile impostare la nuova proprietà CSS M3 – MS-High-Contrast: off su un elemento padre.

-   **Scrittura di un'app di Windows Store a contrasto elevato:**

    L'app di Windows Store deve usare la classe [SystemColors](/dotnet/api/system.windows.systemcolors) per determinare la colorazione corretta degli elementi dell'interfaccia utente, tenendo presente che alcuni colori della metrica di sistema sono progettati per essere usati insieme, ad esempio SystemColors. WindowColor e SystemColors. WindowTextColor. Ciò facilita un'esperienza di contrasto elevato superiore.

-   **Rilevamento corretto del contrasto elevato nelle versioni precedenti di Windows:**

    Le app in esecuzione in versioni precedenti di Windows non hanno accesso ai nuovi temi a contrasto elevato anche se il manifesto specifica la compatibilità con la versione di Windows in questione. Di conseguenza, potrebbe essere necessario inserire percorsi di codice aggiuntivi per gestire il rendering nell'ambiente classico utilizzato nelle versioni precedenti di Windows. La presenza di un contrasto elevato in questo caso deve essere controllata chiamando la funzione [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il \_ flag GETHIGHCONTRAST di spi. Questo è l'unico modo supportato per verificare la presenza di un contrasto elevato.

## <a name="tests"></a>Test

Durante il test di un'app, assicurarsi che il rendering venga eseguito correttamente in tutti i temi inclusi in Windows 8: Aero, Basic, Contrasto elevato 1, Contrasto elevato 2, Contrasto elevato nero e Contrasto elevato bianco. Verificare che il testo sia chiaramente visibile e facile da leggere nei temi a contrasto elevato.

## <a name="resources"></a>Risorse

-   [Classi, parti e Stati di stile Aero](../controls/aero-style-classes-parts-and-states.md) (il nuovo tema di base e i temi a contrasto elevato usano anche questi Stati)
-   [Parti e stati comuni a tutti gli stili di visualizzazione](../controls/parts-and-states.md)
-   [Uso di stili di visualizzazione con controlli personalizzati e Owner-Drawn](../controls/using-visual-styles.md)
-   [GetSysColor (funzione)](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [Modulo colori CSS W3C livello 3](https://www.w3.org/TR/css3-color/)
-   [Classe SystemColors](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [SystemParametersInfo (funzione)](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Accessibilità Microsoft](https://www.microsoft.com/enable/)

 

 