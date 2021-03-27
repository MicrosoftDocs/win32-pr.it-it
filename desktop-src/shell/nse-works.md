---
description: Esplora risorse fornisce una rappresentazione grafica dello spazio dei nomi della shell combinato con strumenti che consentono agli utenti di interagire con gli oggetti della shell.
ms.assetid: cc387338-15fa-4350-b039-61a0f1c5030a
title: Informazioni sulle estensioni dello spazio dei nomi della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0150092a25708c1f079160a9d106a7b8205e231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979975"
---
# <a name="understanding-shell-namespace-extensions"></a>Informazioni sulle estensioni dello spazio dei nomi della shell

Esplora risorse fornisce una rappresentazione grafica dello spazio dei nomi della shell combinato con strumenti che consentono agli utenti di interagire con gli oggetti della shell. Con un'estensione dello spazio dei nomi, è possibile usare qualsiasi corpo di dati e fare in modo che Esplora risorse lo presenti all'utente come cartella virtuale. Quando un utente accede a questa cartella, i dati vengono presentati come una gerarchia strutturata con struttura ad albero di cartelle e file, in modo analogo al resto dello spazio dei nomi della shell. Gli utenti e le applicazioni sono in grado di interagire con il contenuto di questa cartella virtuale in modo analogo a qualsiasi altro oggetto spazio dei nomi. In questo documento viene illustrato come creare un'estensione dello spazio dei nomi.

-   [Funzionamento di un'estensione dello spazio dei nomi](#how-a-namespace-extension-works)
-   [Oggetto visualizzazione cartella di sistema predefinito (DefView)](#the-default-system-folder-view-object-defview)
-   [Interazione di Esplora risorse con un'estensione dello spazio dei nomi](#how-windows-explorer-interacts-with-a-namespace-extension)
    -   [Visualizzazione albero](#tree-view)
    -   [Visualizzazione cartelle](#folder-view)
    -   [Barra dei menu e barre degli strumenti](#menu-bar-and-toolbars)
    -   [Barra di stato](#status-bar)

## <a name="how-a-namespace-extension-works"></a>Funzionamento di un'estensione dello spazio dei nomi

Dietro le quinte, ogni cartella visualizzata da Esplora risorse è rappresentata da un oggetto Component Object Model (COM) denominato *oggetto Folder*. Ogni volta che l'utente interagisce con una cartella o il relativo contenuto, la shell comunica con l'oggetto cartella associato tramite una delle numerose interfacce standard. L'oggetto Folder esegue quindi tutte le operazioni necessarie per rispondere all'azione dell'utente e la Shell Aggiorna la visualizzazione di Esplora risorse.

La maggior parte dei file e delle cartelle con cui gli utenti interagiscono fanno parte del file system o di una cartella virtuale di sistema, ad esempio il Cestino. In altre documentazioni è stato illustrato come è possibile personalizzare il comportamento di queste cartelle standard per soddisfare i requisiti dell'applicazione modificando il registro di sistema o implementando [gestori estensioni della shell](handlers.md). Tuttavia, l'estensione della shell in questi modi è particolarmente utile quando le informazioni possono essere facilmente confezionate sotto forma di normali file di file system o cartelle.

Esistono diverse situazioni in cui l'archiviazione dei dati come raccolta di cartelle e file di file System potrebbe essere indesiderata o addirittura impossibile. Di seguito sono riportati alcuni esempi di questo tipo di dati:

-   Raccolta di elementi che vengono inseriti più efficacemente in un unico file, ad esempio un database.
-   Raccolta di elementi archiviati in un computer remoto che non dispone di un file system Windows standard. Un esempio di questi dati è costituito dalle informazioni archiviate in un Personal Digital Assistant (PDA) o in una fotocamera digitale.
-   Raccolta di elementi che non rappresentano i dati archiviati. Un esempio di tali dati è costituito dai collegamenti alla stampante contenuti nella cartella stampanti standard.

Un modo per presentare questo tipo di dati a un utente consiste nel scrivere un'applicazione per consentire agli utenti di visualizzare e interagire con i vari elementi. Tuttavia, se i dati possono essere presentati come gerarchia di cartelle o file, gran parte delle funzionalità che è necessario implementare potrebbero essere servizi dell'interfaccia utente già forniti da Esplora risorse. Un approccio molto più efficiente potrebbe essere quello di scrivere un'estensione dello spazio dei nomi e di fare in modo che Esplora risorse diventi l'interfaccia utente grafica.

Per implementare un'estensione dello spazio dei nomi, le informazioni devono essere organizzate come spazi dei nomi strutturati ad albero. La *radice dello spazio dei nomi* viene presentata come cartella virtuale nello spazio dei nomi della shell. La cartella radice e tutte le relative sottocartelle e gli elementi di dati diventano parte dello spazio dei nomi della shell e Esplora risorse diventa l'interfaccia utente. È quindi possibile presentare le informazioni all'utente in modo familiare e facilmente accessibile con molto meno la programmazione dell'interfaccia utente rispetto a quella necessaria per un'applicazione personalizzata.

Un'estensione dello spazio dei nomi è costituita da due componenti di base:

-   Gestione dati
-   Interfaccia tra il gestore di dati e Esplora risorse

Il primo componente dell'elenco è completamente attivo. È possibile archiviare e gestire i dati in qualsiasi modo più efficace. Il secondo componente è il codice necessario per creare il pacchetto dei dati come oggetti cartella e gestire l'interazione con Esplora risorse. Esplora risorse può quindi chiamare questi oggetti per consentire agli utenti di visualizzare e interagire con i dati come se si trattasse di una raccolta di cartelle e file. Gli oggetti cartella dell'estensione dello spazio dei nomi devono interagire con Esplora risorse come se si trattasse di cartelle normali. Prima di tentare di implementare un'estensione dello spazio dei nomi, è prima necessario comprendere in che modo Esplora risorse gestisce un oggetto cartella.

## <a name="the-default-system-folder-view-object-defview"></a>Oggetto visualizzazione cartella di sistema predefinito (DefView)

La shell fornisce un'implementazione predefinita della visualizzazione cartelle, colloquialmente nota come DefView, in modo che sia possibile evitare la maggior parte delle operazioni di implementazione dell'estensione dello spazio dei nomi. Poiché alcune funzionalità di visualizzazione non possono essere realizzate tramite visualizzazioni personalizzate, è spesso consigliabile usare l'oggetto visualizzazione cartella di sistema predefinito al posto di una visualizzazione personalizzata. Per ulteriori informazioni, vedere [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview).

## <a name="how-windows-explorer-interacts-with-a-namespace-extension"></a>Interazione di Esplora risorse con un'estensione dello spazio dei nomi

Esplora risorse offre agli utenti un'interfaccia utente grafica che consente di eseguire varie attività, tra cui:

-   [Esplorazione](navigate.md) della gerarchia dello spazio dei nomi e visualizzazione del contenuto delle cartelle.
-   [Gestione](manage.md) del contenuto dello spazio dei nomi mediante lo spostamento, l'eliminazione e la copia di oggetti.
-   [Recupero](folder-info.md) di un'ampia gamma di informazioni sugli oggetti.
-   [Avvio](launch.md) delle applicazioni.

L'interfaccia utente grafica di Esplora risorse ha cinque componenti di base. Nell'illustrazione seguente vengono denominati i componenti e viene mostrato dove vengono in genere visualizzati in Esplora risorse.

![illustrazione che mostra i componenti dell'interfaccia utente di Esplora risorse ](images/nse1.png)

Quando un utente visualizza una cartella che appartiene a un'estensione dello spazio dei nomi in Esplora risorse, l'oggetto cartella presenta almeno un controllo parziale sul contenuto delle cinque aree.

### <a name="tree-view"></a>Visualizzazione ad albero

La visualizzazione albero fornisce una visualizzazione di alto livello dello spazio dei nomi. Quest'area ospita un [controllo di visualizzazione albero](../controls/tree-view-controls.md) in grado di visualizzare ogni cartella dello spazio dei nomi e la posizione della cartella nella gerarchia dello spazio dei nomi. Un utente può eseguire diverse operazioni con l'area di visualizzazione albero, tra cui:

-   Visualizzazione o nascondere il livello successivo nello spazio dei nomi.
-   Copia, trasferimento o eliminazione di cartelle.
-   Per visualizzare un menu di scelta rapida, fare clic con il pulsante destro del mouse.
-   Selezione di una cartella e visualizzazione del relativo contenuto nella visualizzazione cartelle.

La visualizzazione albero comunica con gli oggetti Folder principalmente tramite la relativa interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Ad esempio, quando un utente fa clic sul segno più (+) accanto all'icona della cartella, Esplora risorse espande la visualizzazione per visualizzare le sottocartelle della cartella. Per ottenere le informazioni necessarie per aggiornare la visualizzazione albero, la shell esegue diverse chiamate all'interfaccia **IShellFolder** dell'oggetto Folder per:

-   Richiedere gli attributi della cartella.
-   Enumerare il contenuto della cartella.
-   Richiedere nomi visualizzati per ogni sottocartella.
-   Richiedere un'icona da visualizzare accanto a ogni cartella.

Esplora risorse aggiorna quindi la visualizzazione albero per visualizzare le sottocartelle della cartella selezionata. Se nelle sottocartelle sono presenti sottocartelle, accanto all'icona della cartella viene visualizzato un carattere "+". Sono disponibili numerose attività più sofisticate che un utente può eseguire anche con la visualizzazione albero, tra cui:

-   Usare gli Appunti per tagliare o copiare una cartella e incollarla in un'altra cartella.
-   Usare il trascinamento della selezione per tagliare o copiare una cartella e rilasciarla in un'altra cartella.
-   Utilizzo di un motore di ricerca per la ricerca di elementi in una cartella o nelle relative sottocartelle.
-   Modifica delle proprietà della cartella.

Per una descrizione più dettagliata del modo in cui un'estensione dello spazio dei nomi gestisce queste azioni utente, vedere [implementazione delle interfacce di oggetti della cartella di base](nse-implement.md).

### <a name="folder-view"></a>Visualizzazione cartelle

Quando un utente seleziona una cartella, il contenuto della cartella viene visualizzato nella visualizzazione cartella. In un certo senso, la funzionalità normale della visualizzazione cartelle si sovrappone alla visualizzazione albero. Gli utenti possono spostare o copiare cartelle, modificare le proprietà delle cartelle, visualizzare il contenuto di una sottocartella, visualizzare un menu di scelta rapida per una cartella e così via. Esistono tuttavia alcune differenze distinte tra visualizzazione albero e visualizzazione cartelle:

-   Visualizzazione cartelle consente di visualizzare solo il contenuto di una singola cartella, non parte o tutta la gerarchia dello spazio dei nomi.
-   Visualizzazione cartelle consente di visualizzare gli oggetti file e gli oggetti cartella.
-   Nella visualizzazione cartelle è possibile visualizzare molte più informazioni sugli oggetti rispetto alla visualizzazione albero.
-   La visualizzazione cartelle consente alle estensioni dello spazio dei nomi di avere un controllo quasi completo sulle informazioni visualizzate e su come. È possibile modificare solo aspetti secondari della visualizzazione albero, ad esempio le icone di cartella.

A differenza della visualizzazione albero, Esplora risorse non controlla direttamente il contenuto della visualizzazione cartelle. La visualizzazione cartelle è un'area fornita da Esplora risorse per gli oggetti cartella. La visualizzazione e la gestione del contenuto di una cartella nella visualizzazione cartelle sono responsabili dell'oggetto cartella. Sebbene la maggior parte delle visualizzazioni di cartella segua un formato abbastanza standard, esistono alcune limitazioni relative a ciò che può essere visualizzato o al modo in cui. Un caso estremo è la cartella Internet, ovvero un browser con funzionalità complete.

Quando un utente seleziona una cartella che appartiene all'estensione dello spazio dei nomi, viene creata una finestra e il relativo handle viene passato a Esplora risorse. Questa finestra diventa figlio della finestra di visualizzazione cartelle. Esplora risorse fornisce le dimensioni della finestra di visualizzazione cartelle, ma non impone alcuna restrizione sul contenuto della finestra figlio. È quindi possibile usare la finestra figlio per visualizzare la visualizzazione cartelle della cartella.

Le estensioni dello spazio dei nomi utilizzano uno dei due approcci per la creazione di una visualizzazione cartelle:

-   Utilizzare la finestra figlio per ospitare un controllo [visualizzazione elenco](../controls/list-view-control-reference.md) . Questo controllo consente di visualizzare il contenuto di una cartella in modo molto simile alla [visualizzazione classica](../lwef/web-view.md)di Esplora risorse.
-   Utilizzare la finestra figlio per ospitare un [controllo WebBrowser](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752044(v=vs.85)) e utilizzare un documento DHTML (Dynamic HTML) per visualizzare il contenuto della cartella.

Entrambi gli approcci visualizzano una visualizzazione di cartelle che ha un aspetto molto simile a quello visualizzato per le cartelle di sistema. Tuttavia, se si desidera utilizzare uno schema di visualizzazione diverso, è possibile eseguire questa operazione.

### <a name="menu-bar-and-toolbars"></a>Barra dei menu e barre degli strumenti

Come la maggior parte delle applicazioni Windows, Esplora risorse fornisce all'utente una raccolta di strumenti. Una selezione completa di strumenti è disponibile tramite la barra dei menu. Gli strumenti usati più di frequente sono rappresentati anche da pulsanti o caselle di modifica su una barra degli strumenti. A differenza di molte applicazioni Windows, la barra dei menu di Esplora risorse è in realtà un [controllo Toolbar](../controls/toolbar-control-reference.md) che è stato personalizzato per comportarsi come un menu convenzionale. Sia la barra dei menu che la barra degli strumenti sono incorporati in un [controllo Rebar](../controls/rebar-control-reference.md) per consentire agli utenti di organizzare i singoli controlli per soddisfare le proprie esigenze.

Per impostazione predefinita, Esplora risorse supporta un set standard di pulsanti e voci di menu, ad esempio copia e proprietà. L'estensione dello spazio dei nomi può personalizzare la barra dei menu e le barre degli strumenti eliminando gli strumenti standard e aggiungendo strumenti personalizzati. Quando l'oggetto visualizzazione cartella viene inizializzato, Esplora risorse passa un puntatore alla relativa interfaccia [**IShellBrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) . Questa interfaccia supporta diversi metodi che è possibile chiamare per personalizzare la barra dei menu e la barra degli strumenti. Quando l'utente seleziona una delle voci di menu o dei pulsanti della barra degli strumenti personalizzati, Esplora risorse invia \_ i messaggi di comando WM per gli elementi del menu personalizzato e della barra degli strumenti alla routine della finestra della finestra figlio.

### <a name="status-bar"></a>Barra di stato

La barra di stato di Esplora risorse Visualizza informazioni sull'oggetto attualmente selezionato. L'estensione dello spazio dei nomi può utilizzare la barra di stato per visualizzare informazioni sullo stato, ad esempio una stringa di testo. È possibile personalizzare la barra di stato chiamando [**IShellBrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser).

 

 
