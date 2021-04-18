---
description: Ogni documento in un'applicazione con interfaccia a documenti multipli (MDI) viene visualizzato in una finestra figlio separata all'interno dell'area client della finestra principale dell'applicazione.
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: Informazioni sull'interfaccia a più documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0397127d7ec343ebdb7696c2dd7d57204a5d5ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319097"
---
# <a name="about-the-multiple-document-interface"></a>Informazioni sull'interfaccia a più documenti

Ogni documento in un'applicazione con interfaccia a documenti multipli (MDI) viene visualizzato in una finestra figlio separata all'interno dell'area client della finestra principale dell'applicazione. Le applicazioni MDI tipiche includono applicazioni di elaborazione di testi che consentono all'utente di usare più documenti di testo e applicazioni di fogli di calcolo che consentono all'utente di usare più grafici e fogli di calcolo. Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Frame, client e finestre figlio](#frame-client-and-child-windows)
-   [Creazione finestra figlio](#child-window-creation)
-   [Attivazione della finestra figlio](#child-window-activation)
-   [Menu di più documenti](#multiple-document-menus)
-   [Più acceleratori di documenti](#multiple-document-accelerators)
-   [Dimensioni e disposizione della finestra figlio](#child-window-size-and-arrangement)
-   [Finestre del titolo dell'icona](#icon-title-windows)
-   [Dati della finestra figlio](#child-window-data)
    -   [Struttura finestra](#window-structure)
    -   [Proprietà finestra](#window-properties)

## <a name="frame-client-and-child-windows"></a>Frame, client e finestre figlio

Un'applicazione MDI dispone di tre tipi di finestre: una finestra cornice, una finestra client MDI, oltre a un numero di finestre figlio. La *finestra cornice* è simile alla finestra principale dell'applicazione: dispone di un bordo di ridimensionamento, una barra del titolo, un menu finestra, un pulsante Riduci a icona e un pulsante Ingrandisci. L'applicazione deve registrare una classe di finestra per la finestra cornice e fornire una routine della finestra per supportarla.

Un'applicazione MDI non Visualizza l'output nell'area client della finestra cornice. Viene invece visualizzata la finestra client MDI. Una *finestra client MDI* è un tipo speciale di finestra figlio appartenente alla classe della finestra pre-registrata **MdiClient**. La finestra del client è un elemento figlio della finestra cornice; funge da background per le finestre figlio. Fornisce inoltre il supporto per la creazione e la modifica delle finestre figlio. Ad esempio, un'applicazione MDI può creare, attivare o ingrandire le finestre figlio inviando messaggi alla finestra del client MDI.

Quando l'utente apre o crea un documento, la finestra del client crea una finestra figlio per il documento. La finestra client è la finestra padre di tutte le finestre figlio MDI nell'applicazione. Ogni finestra figlio ha un bordo di ridimensionamento, una barra del titolo, un menu finestra, un pulsante Riduci a icona e un pulsante Ingrandisci. Poiché una finestra figlio viene ritagliata, viene limitata alla finestra client e non può essere visualizzata all'esterno.

Un'applicazione MDI può supportare più di un tipo di documento. Ad esempio, un'applicazione di foglio di calcolo tipica consente all'utente di usare sia i grafici che i fogli di calcolo. Per ogni tipo di documento supportato, un'applicazione MDI deve registrare una classe della finestra figlio e fornire una routine della finestra per supportare le finestre che appartengono a tale classe. Per ulteriori informazioni sulle classi della finestra, vedere [classi di finestra](window-classes.md). Per ulteriori informazioni sulle routine della finestra, vedere [routine della finestra](window-procedures.md).

Di seguito è riportata una tipica applicazione MDI. Il nome è MultiPad.

![finestra cornice dell'applicazione MDI MultiPad e finestra client](images/csmdi-01.png)

## <a name="child-window-creation"></a>Creazione finestra figlio

Per creare una finestra figlio, un'applicazione MDI chiama la funzione [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) o invia il messaggio [**WM \_ MDICREATE**](wm-mdicreate.md) alla finestra client MDI. Un modo più efficiente per creare una finestra figlio MDI consiste nel chiamare la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , specificando lo stile esteso **WS \_ ex \_ MDIChild** .

Per eliminare definitivamente una finestra figlio, un'applicazione MDI Invia un messaggio [**\_ MDIDESTROY WM**](wm-mdidestroy.md) alla finestra del client MDI.

## <a name="child-window-activation"></a>Attivazione della finestra figlio

Qualsiasi numero di finestre figlio può essere visualizzato nella finestra del client in qualsiasi momento, ma solo uno può essere attivo. La finestra figlio attiva è posizionata davanti a tutte le altre finestre figlio e il bordo è evidenziato.

L'utente può attivare una finestra figlio inattiva facendo clic su di essa. Un'applicazione MDI attiva una finestra figlio inviando un messaggio [**WM \_ MDIACTIVATE**](wm-mdiactivate.md) alla finestra del client MDI. Quando la finestra client elabora questo messaggio, invia un messaggio **WM \_ MDIACTIVATE** alla routine della finestra figlio da attivare e alla routine della finestra della finestra figlio da disattivare.

Per impedire l'attivazione di una finestra figlio, gestire il messaggio [**WM \_ NCACTIVATE**](wm-ncactivate.md) alla finestra figlio restituendo **false**.

Il sistema tiene traccia della posizione di ogni finestra figlio nello stack di finestre sovrapposte. Questo stack è noto come [ordine Z](window-features.md). L'utente può attivare la finestra figlio successiva nella z order facendo clic su **Avanti** dal menu finestra della finestra attiva. Un'applicazione attiva la finestra figlio successiva o precedente nel z order inviando un messaggio [**WM \_ MDINEXT**](wm-mdinext.md) alla finestra client.

Per recuperare l'handle per la finestra figlio attiva, l'applicazione MDI Invia un [**messaggio \_ MDIGETACTIVE WM**](wm-mdigetactive.md) alla finestra client.

## <a name="multiple-document-menus"></a>Menu di più documenti

La finestra cornice di un'applicazione MDI deve includere una barra dei menu con un menu finestra. Il menu finestra deve includere elementi che dispongono le finestre figlio nella finestra del client o che chiudono tutte le finestre figlio. Il menu finestra di una tipica applicazione MDI potrebbe includere gli elementi indicati nella tabella seguente.



| Voce di menu         | Scopo                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Tile**          | Dispone le finestre figlio in un formato di sezione in modo che ognuna venga visualizzata completamente nella finestra del client.                       |
| **Cascata**       | Dispone le finestre figlio in un formato Cascade. Le finestre figlio si sovrappongono l'una all'altra, ma la barra del titolo di ogni è visibile. |
| **Disponi icone** | Dispone le icone delle finestre figlio ridotte a icona lungo la parte inferiore della finestra del client.                                     |
| **Chiudi tutto**     | Chiude tutte le finestre figlio.                                                                                                |



 

Ogni volta che viene creata una finestra figlio, il sistema aggiunge automaticamente una nuova voce di menu al menu finestra. Il testo della voce di menu corrisponde al testo sulla barra dei menu della nuova finestra figlio. Facendo clic sulla voce di menu, l'utente può attivare la finestra figlio corrispondente. Quando una finestra figlio viene distrutta, il sistema rimuove automaticamente la voce di menu corrispondente dal menu finestra.

Il sistema può aggiungere fino a dieci voci di menu al menu finestra. Quando viene creata la decima finestra figlio, il sistema aggiunge l' **altro** elemento di Windows al menu finestra. Quando si fa clic su questa voce, viene visualizzata la finestra di dialogo **Seleziona finestra** . La finestra di dialogo contiene una casella di riepilogo con i titoli di tutte le finestre figlio MDI attualmente disponibili. L'utente può attivare una finestra figlio facendo clic sul titolo nella casella di riepilogo.

Se l'applicazione MDI supporta diversi tipi di finestre figlio, adattare la barra dei menu in modo da riflettere le operazioni associate alla finestra attiva. A tale scopo, specificare risorse di menu separate per ogni tipo di finestra figlio supportata dall'applicazione. Quando viene attivato un nuovo tipo di finestra figlio, l'applicazione deve inviare un messaggio [**WM \_ MDISETMENU**](wm-mdisetmenu.md) alla finestra del client, passando all'handle il menu corrispondente.

Quando non esiste alcuna finestra figlio, la barra dei menu deve contenere solo elementi utilizzati per creare o aprire un documento.

Quando l'utente si sposta attraverso i menu di un'applicazione MDI usando i tasti di cursore, le chiavi si comportano in modo diverso rispetto a quando l'utente si sposta nei menu di un'applicazione tipica. In un'applicazione MDI, il controllo passa dal menu della finestra dell'applicazione al menu finestra della finestra figlio attiva e quindi al primo elemento sulla barra dei menu.

## <a name="multiple-document-accelerators"></a>Più acceleratori di documenti

Per ricevere ed elaborare i tasti di scelta rapida per le finestre figlio, un'applicazione MDI deve includere la funzione [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) nel ciclo di messaggi. Il ciclo deve chiamare **TranslateMDISysAccel** prima di chiamare la funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) o [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .

I tasti di scelta rapida del menu finestra per una finestra figlio MDI sono diversi da quelli per una finestra figlio non MDI. In una finestra figlio MDI la combinazione di tasti ALT +-(meno) apre il menu finestra, la combinazione di tasti CTRL + F4 chiude la finestra figlio attiva e la combinazione di tasti CTRL + F6 attiva la finestra figlio successiva.

## <a name="child-window-size-and-arrangement"></a>Dimensioni e disposizione della finestra figlio

Un'applicazione MDI controlla le dimensioni e la posizione delle finestre figlio inviando messaggi alla finestra del client MDI. Per ingrandire la finestra figlio attiva, l'applicazione invia il messaggio [**\_ MDIMAXIMIZE WM**](wm-mdimaximize.md) alla finestra client. Quando una finestra figlio viene ingrandita, la relativa area client riempie completamente la finestra del client MDI. Inoltre, il sistema nasconde automaticamente la barra del titolo della finestra figlio e aggiunge l'icona del menu della finestra figlio e il pulsante Ripristina alla barra dei menu dell'applicazione MDI. L'applicazione può ripristinare le dimensioni e la posizione originali (premassimizzate) inviando la finestra client di un messaggio [**WM \_ MDIRESTORE**](wm-mdirestore.md) .

Un'applicazione MDI può disporre le finestre figlio in formato Cascade o Tile. Quando le finestre figlio vengono propagate a catena, le finestre vengono visualizzate in uno stack. La finestra nella parte inferiore dello stack occupa l'angolo superiore sinistro dello schermo e le finestre rimanenti vengono sfalsate verticalmente e orizzontalmente, in modo che il bordo sinistro e la barra del titolo di ogni finestra figlio siano visibili. Per disporre le finestre figlio nel formato Cascade, un'applicazione MDI invia il messaggio [**WM \_ MDICASCADE**](wm-mdicascade.md) . In genere, l'applicazione invia questo messaggio quando l'utente fa clic su **Cascade** nel menu finestra.

Quando le finestre figlio sono affiancate, il sistema Visualizza ogni finestra figlio nella sua interezza, sovrapposta a nessuna delle finestre. Tutte le finestre vengono dimensionate in base alle esigenze per adattarsi alla finestra del client. Per disporre le finestre figlio nel formato tessera, un'applicazione MDI Invia un [**messaggio \_ MDITILE WM**](wm-mditile.md) alla finestra client. In genere, l'applicazione invia questo messaggio quando l'utente fa clic sul **riquadro** nel menu finestra.

Un'applicazione MDI deve fornire un'icona diversa per ogni tipo di finestra figlio supportata. L'applicazione specifica un'icona quando si registra la classe della finestra figlio. Il sistema visualizza automaticamente l'icona di una finestra figlio nella parte inferiore della finestra del client quando la finestra figlio è ridotta a icona. Un'applicazione MDI indica al sistema di disporre le icone della finestra figlio inviando un messaggio [**\_ MDIICONARRANGE WM**](wm-mdiiconarrange.md) alla finestra client. In genere, l'applicazione invia questo messaggio quando l'utente fa clic su **Disponi icone** nel menu finestra.

## <a name="icon-title-windows"></a>Finestre del titolo dell'icona

Poiché le finestre figlio MDI possono essere ridotte a icona, un'applicazione MDI deve evitare di manipolare le finestre del titolo delle icone come se fossero finestre figlio MDI normali. Le finestre del titolo dell'icona vengono visualizzate quando l'applicazione enumera le finestre figlio della finestra del client MDI. Le finestre del titolo dell'icona sono diverse dalle altre finestre figlio, tuttavia, in quanto sono di proprietà di una finestra figlio MDI.

Per determinare se una finestra figlio è una finestra del titolo dell'icona, usare la funzione [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) con l' \_ indice del proprietario GW. Le finestre non di titolo restituiscono **null**. Si noti che questo test non è sufficiente per le finestre di primo livello, perché i menu e le finestre di dialogo sono di proprietà di Windows.

## <a name="child-window-data"></a>Dati della finestra figlio

Poiché il numero di finestre figlio varia a seconda del numero di documenti aperti dall'utente, un'applicazione MDI deve essere in grado di associare i dati, ad esempio il nome del file corrente, a ogni finestra figlio. A questo scopo è possibile procedere in due modi:

-   Archiviare i dati della finestra figlio nella struttura della finestra.
-   Utilizzare le proprietà della finestra.

### <a name="window-structure"></a>Struttura finestra

Quando un'applicazione MDI registra una classe della finestra, può riservare ulteriore spazio nella struttura della finestra per i dati dell'applicazione specifici per questa particolare classe di finestre. Per archiviare e recuperare i dati in questo spazio aggiuntivo, l'applicazione usa le funzioni [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Per mantenere una grande quantità di dati per una finestra figlio, un'applicazione può allocare memoria per una struttura di dati e quindi archiviare l'handle nella memoria contenente la struttura nello spazio aggiuntivo associato alla finestra figlio.

### <a name="window-properties"></a>Proprietà finestra

Un'applicazione MDI può inoltre archiviare dati per documento utilizzando le proprietà della finestra. I *dati per documento* sono dati specifici del tipo di documento contenuto in una particolare finestra figlio. Le proprietà sono diverse dallo spazio aggiuntivo nella struttura della finestra perché non è necessario allocare spazio aggiuntivo durante la registrazione della classe di finestra. Una finestra può avere un numero qualsiasi di proprietà. Inoltre, quando vengono usati gli offset per accedere allo spazio aggiuntivo nelle strutture della finestra, le proprietà vengono definite in base ai nomi delle stringhe. Per ulteriori informazioni sulle proprietà della finestra, vedere [proprietà della finestra](window-properties.md).

 

 
