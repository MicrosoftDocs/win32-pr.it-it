---
description: Ogni documento in un'applicazione con interfaccia a documenti multipli (MDI) viene visualizzato in una finestra figlio separata all'interno dell'area client della finestra principale dell'applicazione.
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: Informazioni sull'interfaccia a documenti multipli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071d3bebad8e6aba48b69b66fd41f9f7933c1d9785ae38512003aaf1bd9a19e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706002"
---
# <a name="about-the-multiple-document-interface"></a>Informazioni sull'interfaccia a documenti multipli

Ogni documento in un'applicazione con interfaccia a documenti multipli (MDI) viene visualizzato in una finestra figlio separata all'interno dell'area client della finestra principale dell'applicazione. Le tipiche applicazioni MDI includono applicazioni di elaborazione delle parole che consentono all'utente di lavorare con più documenti di testo e applicazioni foglio di calcolo che consentono all'utente di usare più grafici e fogli di calcolo. Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Frame, client e figlio Windows](#frame-client-and-child-windows)
-   [Creazione di finestre figlio](#child-window-creation)
-   [Attivazione della finestra figlio](#child-window-activation)
-   [Menu a più documenti](#multiple-document-menus)
-   [Acceleratori di documenti multipli](#multiple-document-accelerators)
-   [Dimensioni e disposizione della finestra figlio](#child-window-size-and-arrangement)
-   [Icona Titolo Windows](#icon-title-windows)
-   [Dati della finestra figlio](#child-window-data)
    -   [Struttura della finestra](#window-structure)
    -   [Proprietà finestra](#window-properties)

## <a name="frame-client-and-child-windows"></a>Frame, client e figlio Windows

Un'applicazione MDI ha tre tipi di finestre: una finestra cornice, una finestra del client MDI e una serie di finestre figlio. La *finestra cornice* è simile alla finestra principale dell'applicazione: ha un bordo di ridimensionamento, una barra del titolo, un menu della finestra, un pulsante riduci a icona e un pulsante ingrandisci. L'applicazione deve registrare una classe di finestra per la finestra cornice e fornire una routine della finestra per supportarla.

Un'applicazione MDI non visualizza l'output nell'area client della finestra cornice. Viene invece visualizzata la finestra del client MDI. Una *finestra client MDI* è un tipo speciale di finestra figlio appartenente alla classe della finestra **preregistrata MDICLIENT.** La finestra client è un elemento figlio della finestra cornice. funge da sfondo per le finestre figlio. Fornisce inoltre il supporto per la creazione e la modifica di finestre figlio. Ad esempio, un'applicazione MDI può creare, attivare o ingrandire le finestre figlio inviando messaggi alla finestra del client MDI.

Quando l'utente apre o crea un documento, la finestra client crea una finestra figlio per il documento. La finestra client è la finestra padre di tutte le finestre figlio MDI nell'applicazione. Ogni finestra figlio ha un bordo di ridimensionamento, una barra del titolo, un menu della finestra, un pulsante riduci a icona e un pulsante ingrandisci. Poiché una finestra figlio viene ritagliata, è limitata alla finestra client e non può essere visualizzata all'esterno di essa.

Un'applicazione MDI può supportare più di un tipo di documento. Ad esempio, una tipica applicazione foglio di calcolo consente all'utente di usare sia grafici che fogli di calcolo. Per ogni tipo di documento supportato, un'applicazione MDI deve registrare una classe di finestra figlio e fornire una routine della finestra per supportare le finestre appartenenti a tale classe. Per altre informazioni sulle classi di finestra, vedere [Classi di finestre.](window-classes.md) Per altre informazioni sulle routine della finestra, vedere [Routine della finestra.](window-procedures.md)

Di seguito è riportata una tipica applicazione MDI. Il nome è Multipad.

![Finestra cornice dell'applicazione mdi multipad e finestra client](images/csmdi-01.png)

## <a name="child-window-creation"></a>Creazione di finestre figlio

Per creare una finestra figlio, un'applicazione MDI chiama la funzione [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) o invia il messaggio [**\_ WM MDICREATE**](wm-mdicreate.md) alla finestra del client MDI. Un modo più efficiente per creare una finestra figlio MDI è chiamare la [**funzione CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) specificando lo stile **esteso \_ WS EX \_ MDICHILD.**

Per eliminare una finestra figlio, un'applicazione MDI invia un [**messaggio \_ MDIDESTROY WM**](wm-mdidestroy.md) alla finestra del client MDI.

## <a name="child-window-activation"></a>Attivazione della finestra figlio

Nella finestra client può essere visualizzato un numero qualsiasi di finestre figlio in qualsiasi momento, ma solo una può essere attiva. La finestra figlio attiva viene posizionata davanti a tutte le altre finestre figlio e il bordo viene evidenziato.

L'utente può attivare una finestra figlio inattiva facendo clic su di essa. Un'applicazione MDI attiva una finestra figlio inviando un messaggio [**\_ MDIACTIVATE WM**](wm-mdiactivate.md) alla finestra del client MDI. Quando la finestra client elabora questo messaggio, invia un messaggio **\_ WM MDIACTIVATE** alla routine della finestra della finestra figlio da attivare e alla routine della finestra figlio in fase di disattivazione.

Per impedire l'attivazione di una finestra figlio, gestire il messaggio [**\_ WM NCACTIVATE**](wm-ncactivate.md) nella finestra figlio restituisce **FALSE.**

Il sistema tiene traccia della posizione di ogni finestra figlio nello stack di finestre sovrapposte. Questo stacking è noto come [Z-Order.](window-features.md) L'utente può attivare la finestra figlio successiva nell'ordine Z facendo clic su **Avanti** dal menu della finestra nella finestra attiva. Un'applicazione attiva la finestra figlio successiva (o precedente) nell'ordine Z inviando un messaggio [**\_ WM MDINEXT**](wm-mdinext.md) alla finestra client.

Per recuperare l'handle per la finestra figlio attiva, l'applicazione MDI invia un messaggio [**\_ WM MDIGETACTIVE**](wm-mdigetactive.md) alla finestra client.

## <a name="multiple-document-menus"></a>Menu a più documenti

La finestra cornice di un'applicazione MDI deve includere una barra dei menu con un menu di finestra. Il menu della finestra deve includere elementi che dispongono le finestre figlio all'interno della finestra del client o che chiudono tutte le finestre figlio. Il menu della finestra di una tipica applicazione MDI potrebbe includere gli elementi nella tabella seguente.



| Voce di menu         | Scopo                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Tile**          | Dispone le finestre figlio in un formato di riquadro in modo che ognuna venga visualizzata per intero nella finestra del client.                       |
| **Cascata**       | Dispone le finestre figlio in un formato a cascata. Le finestre figlio si sovrappongono tra loro, ma la barra del titolo di ognuna è visibile. |
| **Disponi icone** | Dispone le icone delle finestre figlio ridotte a icona nella parte inferiore della finestra client.                                     |
| **Chiudi tutto**     | Chiude tutte le finestre figlio.                                                                                                |



 

Ogni volta che viene creata una finestra figlio, il sistema aggiunge automaticamente una nuova voce di menu al menu della finestra. Il testo della voce di menu corrisponde al testo sulla barra dei menu della nuova finestra figlio. Facendo clic sulla voce di menu, l'utente può attivare la finestra figlio corrispondente. Quando una finestra figlio viene distrutta, il sistema rimuove automaticamente la voce di menu corrispondente dal menu della finestra.

Il sistema può aggiungere fino a dieci voci di menu al menu della finestra. Quando viene creata la decimo finestra figlio, il sistema aggiunge la voce **Windows** al menu della finestra. Facendo clic su questo elemento viene **visualizzata la finestra di** dialogo Seleziona finestra . La finestra di dialogo contiene una casella di riepilogo con i titoli di tutte le finestre figlio MDI attualmente disponibili. L'utente può attivare una finestra figlio facendo clic sul relativo titolo nella casella di riepilogo.

Se l'applicazione MDI supporta diversi tipi di finestre figlio, personalizzare la barra dei menu in modo da riflettere le operazioni associate alla finestra attiva. A tale scopo, fornire risorse di menu separate per ogni tipo di finestra figlio supportato dall'applicazione. Quando viene attivato un nuovo tipo di finestra figlio, l'applicazione deve inviare un messaggio [**\_ MDISETMENU WM**](wm-mdisetmenu.md) alla finestra client, passando l'handle al menu corrispondente.

Quando non esiste alcuna finestra figlio, la barra dei menu deve contenere solo gli elementi usati per creare o aprire un documento.

Quando l'utente si sposta tra i menu di un'applicazione MDI usando i tasti di cursore, i tasti si comportano in modo diverso rispetto a quando l'utente si sposta tra i menu di un'applicazione tipica. In un'applicazione MDI il controllo passa dal menu della finestra dell'applicazione al menu della finestra della finestra figlio attiva e quindi alla prima voce nella barra dei menu.

## <a name="multiple-document-accelerators"></a>Acceleratori di documenti multipli

Per ricevere ed elaborare i tasti di scelta rapida per le finestre figlio, un'applicazione MDI deve includere la [**funzione TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) nel ciclo di messaggi. Il ciclo deve chiamare **TranslateMDISysAccel** prima di chiamare la [**funzione TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) o [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)

I tasti di scelta rapida nel menu della finestra per una finestra figlio MDI sono diversi da quelli per una finestra figlio non MDI. In una finestra figlio MDI la combinazione di tasti ALT+ - (meno) apre il menu della finestra, la combinazione di tasti CTRL+F4 chiude la finestra figlio attiva e la combinazione di tasti CTRL+F6 attiva la finestra figlio successiva.

## <a name="child-window-size-and-arrangement"></a>Dimensioni e disposizione della finestra figlio

Un'applicazione MDI controlla le dimensioni e la posizione delle finestre figlio inviando messaggi alla finestra del client MDI. Per ingrandire la finestra figlio attiva, l'applicazione invia il [**messaggio \_ WM MDIMAXIMIZE**](wm-mdimaximize.md) alla finestra del client. Quando una finestra figlio è ingrandita, la relativa area client riempie completamente la finestra del client MDI. Inoltre, il sistema nasconde automaticamente la barra del titolo della finestra figlio e aggiunge l'icona di menu della finestra figlio e il pulsante Ripristina alla barra dei menu dell'applicazione MDI. L'applicazione può ripristinare le dimensioni e la posizione originali (massime) della finestra client inviando alla finestra client un messaggio [**\_ WM MDIRESTORE.**](wm-mdirestore.md)

Un'applicazione MDI può disporre le finestre figlio in un formato a cascata o a riquadri. Quando le finestre figlio sono sovrapposte, le finestre vengono visualizzate in uno stack. La finestra nella parte inferiore dello stack occupa l'angolo superiore sinistro dello schermo e le finestre rimanenti vengono offset verticalmente e orizzontalmente in modo che il bordo sinistro e la barra del titolo di ogni finestra figlio siano visibili. Per disporre le finestre figlio nel formato a cascata, un'applicazione MDI invia il [**messaggio \_ WM MDICASCADE.**](wm-mdicascade.md) In genere, l'applicazione invia questo messaggio quando l'utente fa clic su **Propaga** nel menu della finestra.

Quando le finestre figlio sono affiancate, il sistema visualizza ogni finestra figlio nella sua interezza, non sovrapponendo nessuna delle finestre. Tutte le finestre vengono ridimensionate, in base alle esigenze, per adattarsi alla finestra del client. Per disporre le finestre figlio nel formato riquadro, un'applicazione MDI invia un [**messaggio \_ MDITILE WM**](wm-mditile.md) alla finestra del client. In genere, l'applicazione invia questo messaggio quando l'utente fa clic su **Riquadro** nel menu della finestra.

Un'applicazione MDI deve fornire un'icona diversa per ogni tipo di finestra figlio che supporta. L'applicazione specifica un'icona durante la registrazione della classe della finestra figlio. Il sistema visualizza automaticamente l'icona di una finestra figlio nella parte inferiore della finestra client quando la finestra figlio è ridotta a icona. Un'applicazione MDI indica al sistema di disporre le icone delle finestre figlio inviando un messaggio [**\_ WM MDIICONARRANGE**](wm-mdiiconarrange.md) alla finestra client. In genere, l'applicazione invia questo messaggio quando l'utente fa clic **su Disponi** icone nel menu della finestra.

## <a name="icon-title-windows"></a>Icona Titolo Windows

Poiché le finestre figlio MDI possono essere ridotte a icona, un'applicazione MDI deve evitare di modificare le finestre del titolo delle icone come se fossero normali finestre figlio MDI. Le finestre del titolo dell'icona vengono visualizzate quando l'applicazione enumera le finestre figlio della finestra del client MDI. Le finestre del titolo dell'icona differiscono dalle altre finestre figlio, tuttavia, perché appartengono a una finestra figlio MDI.

Per determinare se una finestra figlio è una finestra del titolo dell'icona, usare [**la funzione GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) con l'indice GW \_ OWNER. Le finestre non titolo restituiscono **NULL.** Si noti che questo test non è sufficiente per le finestre di primo livello, perché i menu e le finestre di dialogo sono finestre di proprietà.

## <a name="child-window-data"></a>Dati della finestra figlio

Poiché il numero di finestre figlio varia a seconda del numero di documenti aperti dall'utente, un'applicazione MDI deve essere in grado di associare i dati (ad esempio, il nome del file corrente) a ogni finestra figlio. A questo scopo è possibile procedere in due modi:

-   Archiviare i dati della finestra figlio nella struttura della finestra.
-   Usare le proprietà della finestra.

### <a name="window-structure"></a>Struttura della finestra

Quando un'applicazione MDI registra una classe di finestra, può riservare spazio aggiuntivo nella struttura della finestra per i dati dell'applicazione specifici di questa particolare classe di finestre. Per archiviare e recuperare i dati in questo spazio aggiuntivo, l'applicazione usa le [**funzioni GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) [**e SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)

Per mantenere una grande quantità di dati per una finestra figlio, un'applicazione può allocare memoria per una struttura di dati e quindi archiviare l'handle nella memoria contenente la struttura nello spazio aggiuntivo associato alla finestra figlio.

### <a name="window-properties"></a>Proprietà finestra

Un'applicazione MDI può anche archiviare dati per documento usando le proprietà della finestra. *I dati per documento* sono dati specifici del tipo di documento contenuto in una determinata finestra figlio. Le proprietà sono diverse dallo spazio aggiuntivo nella struttura della finestra in , in cui non è necessario allocare spazio aggiuntivo durante la registrazione della classe della finestra. Una finestra può avere un numero qualsiasi di proprietà. Inoltre, quando gli offset vengono usati per accedere allo spazio aggiuntivo nelle strutture della finestra, le proprietà vengono definite dai nomi di stringa. Per altre informazioni sulle proprietà della finestra, vedere [Proprietà della finestra.](window-properties.md)

 

 
