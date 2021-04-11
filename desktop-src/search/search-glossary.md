---
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Glossario di Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac0620f4c85c43aac6d41300e16e3e5a8dd037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128499"
---
# <a name="windows-search-glossary"></a>Glossario di Windows Search

## <a name=""></a>\#

**file con estensione OSD**

File descrittore OpenSearch.

**file con estensione osdx**

Un file XML di descrizione OpenSearch che descrive le connessioni server disponibili e i formati dei risultati per una specifica origine dati basata sul Web. Viene usato per interagire con la shell di Windows. Vedere anche: descrittore OpenSearch.

## <a name="a"></a>A

**Sintassi di query avanzate (AQS)**

Sintassi di query predefinita utilizzata da Windows Search per eseguire una query sull'indice e per perfezionare e restringere i parametri di ricerca. AQS è destinato principalmente all'utente e può essere usato dagli utenti per compilare query AQS, ma può anche essere usato a livello di codice. Vedere anche: sintassi di query naturali (NQS).

**AQS**

Vedere la definizione di: sintassi di query avanzata (AQS).

**associazione**

Mapping di un'estensione di file (ad esempio,. mp3) o di un protocollo (ad esempio, http) a un identificatore a livello di codice (ProgID). Questo mapping viene archiviato nel registro di sistema come impostazione per utente con fallback per computer. Le applicazioni che fanno parte del sistema di programmi predefiniti impostano il mapping di associazione per l'estensione o il protocollo del nome di file in modo che punti alle chiavi ProgID di loro proprietà.

**array di associazioni**

Elenco ordinato di percorsi del registro di sistema utilizzati per archiviare informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, come l'icona e il nome visualizzato del tipo. Ad esempio, un file con estensione jpg presenta la seguente matrice di associazioni in un sistema Windows predefinito: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "HKCR \\ SystemFileAssociations \\ image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

**Atom**

Un XML Schema usato per i feed Web e la distribuzione del contenuto, sviluppato come alternativa a un RSS (Really Simple Syndication). Il formato di diffusione Atom è stato pubblicato come standard IETF proposto in RFC 4287.

## <a name="b"></a>B

**bind**

Per caricare o associare il codice ai dati. Ad esempio, un gestore può essere associato a un'origine dati della shell.

**binding**

Richiesta in una query di ricerca per una colonna in un set di righe restituito. L'associazione specifica una proprietà da includere nei risultati della ricerca.

**bookmark**

Indicatore che identifica in modo univoco una riga all'interno di un set di righe.

## <a name="c"></a>C

**nome canonico**

Nome univoco di una risorsa. "Canonical" indica "secondo le regole". Vedere anche: nome del verbo canonico.

**nome del verbo canonico**

Nome indipendente dalla lingua che può essere utilizzato a livello di codice per fare riferimento a un verbo, indipendentemente dalla stringa localizzata nell'interfaccia utente. Vedere anche: nome canonico, verbo.

**catalog**

Unità di livello superiore dell'organizzazione in Windows Search. Un catalogo rappresenta un set di documenti indicizzati su cui è possibile eseguire query. Un catalogo è costituito da una tabella Properties con il testo o il valore e il percorso corrispondente archiviati nelle colonne della tabella. Ogni riga della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni colonna della tabella corrisponde a una proprietà. Vedere anche: index, servizio Windows Search.

**category**

Raggruppamento gerarchico di righe. Ad esempio, il risultato di una query contenente colonne autore e titolo può essere categorizzato in base all'autore. In questo esempio, ogni gruppo di righe che contiene lo stesso valore per l'autore costituisce una categoria.

**capitolo**

Raccolta di righe all'interno di un set di righe. Vedere anche: Catalog, Category.

**column**

Contenitore per un singolo tipo di informazioni in una riga. Le colonne eseguono il mapping ai nomi di proprietà e specificano quali proprietà vengono usate per gli elementi della struttura ad albero dei comandi della query di ricerca. Vedere anche: Category.

**albero dei comandi**

Una combinazione di restrizioni, categorie e ordinamenti specificati per la query di ricerca. Vedere anche: Category.

**container**

Tipo di elemento della shell che può contenere altri elementi. Gli elementi in un contenitore vengono esposti allo spazio dei nomi della shell utilizzando un'origine dati della shell. Gli esempi includono cartelle, unità, server di rete e file compressi con estensione zip. Vedere anche: origine dati della shell, cartella, elemento della shell.

**content**

Testo e proprietà associati a un elemento della shell o a un'origine di contenuto che può essere indicizzata.

**origine contenuto**

Elemento a cui è possibile accedere dall'indicizzatore. Le origini di contenuto sono indirizzabili da un URL e vengono fornite all'indicizzatore da un gestore di protocollo. Gli esempi includono: file system file e cartelle, elementi e cartelle di Microsoft Outlook, record del database e elementi archiviati di Microsoft SharePoint. Un'origine di contenuto può essere esposta come elementi della shell implementando un'origine dati della shell. Vedere anche: contenuto, elemento della shell.

**content view (visualizzazione contenuto)**

Visualizzazione in Esplora risorse (disponibile in Windows 7 e versioni successive) che Visualizza il contenuto più rilevante per ogni elemento nell'elenco in base all'estensione del nome file o all'associazione di tipo. La visualizzazione contenuto usa una logica di ridimensionamento che elimina le proprietà quando le dimensioni della finestra diminuiscono per garantire che le proprietà più importanti abbiano ancora spazio per essere leggibili in modo chiaro. Vedere anche: modello di layout, tipo, associazione di tipo.

**modalità di visualizzazione contenuto**

Vedere la definizione di: visualizzazione contenuto.

**menu di scelta rapida**

Questo termine viene talvolta usato per indicare il menu di scelta rapida. Vedere definizione per: menu di scelta rapida.

**gestore menu di scelta rapida**

Questo termine viene talvolta usato per indicare il gestore dei menu di scelta rapida. Vedere definizione per: gestore del menu di scelta rapida.

**ricerca per indicizzazione**

Per eseguire l'iterazione su un ambito di ricerca per indicizzazione, identificando le origini contenuto che richiedono indicizzazione o reindicizzazione.

**ambito di ricerca per indicizzazione**

Raccolta di archivi dati (identificabili da URL) che rappresenta il contenuto indicizzato e indicizzato dall'indicizzatore.

**cursor**

Nel contesto dell'indice locale, un cursore è un indicatore per l'utilizzo di una riga o di un piccolo blocco di righe alla volta in un set di dati restituito in un set di risultati. Dopo aver posizionato il cursore su una riga, è possibile eseguire operazioni su tale riga o su un blocco di righe a partire da tale posizione.

## <a name="d"></a>D

**Gestione dati, esplorazione e data mining**

Vedere la definizione di: database Mining Extensions (DMX).

**gestore dell'oggetto dati**

Gestore che fornisce altri formati degli Appunti per l'oggetto dati (IDataObject) di un elemento. Gli oggetti dati vengono usati negli scenari di trascinamento della selezione e di copia e incolla.

**origine dati**

Questo termine viene talvolta usato per indicare l'origine dati dell'archivio dati o della shell. Vedere la definizione per: archivio dati, origine dati Shell.

**archivio dati**

Repository di dati. Un archivio dati può essere esposto al modello di programmazione della shell come contenitore usando un'origine dati della shell. Gli elementi in un archivio dati possono essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo.

**DMX (database Mining Extensions)**

Linguaggio di query utilizzato per creare e modificare data mining. I modelli amministrativi per Windows 7, Windows Search e Windows Explorer sono file con estensione ADMX e si basano sulla tecnologia DMX. È possibile personalizzare i modelli seguenti tramite Criteri di gruppo: search. admx, Explorer. admx e WindowsExplorer. admx.

**DMX**

Vedere la definizione per: database Mining Extensions.

**document**

Elemento della shell che contiene testo e per il quale è possibile implementare l'interfaccia IFilter.

**gestore di trascinamento**

Gestore che consente a un particolare tipo di elemento di supportare gli scenari di trascinamento della selezione e di copia e incolla.

**destinazione di rilascio**

Oggetto dati trascinato e rilasciato su un file. Vedere anche: gestore dati, Drop Handler.

**verbo dinamico**

Verbo che dipende dallo stato di un elemento della shell o del sistema; l'aspetto dell'elemento è basato sullo stato e richiede che il codice in esecuzione determini se l'elemento deve essere visualizzato. Vedere anche: gestore del menu di scelta rapida, verbo statico, verbo.

## <a name="e"></a>E

**Comando Explorer**

Oggetto che può essere visualizzato come pulsante nella parte superiore della finestra di Esplora risorse che fornisce la funzionalità per gli elementi e i contenitori in tale finestra. Un'origine dati della shell fornisce gli oggetti comando di Esplora risorse per un elemento contenitore specifico. I comandi vengono talvolta usati come verbi.

## <a name="f"></a>F

**ricerca federata**

Modello di estendibilità che consente la ricerca di archivi dati e la rappresentazione dei risultati come elementi della shell in Esplora risorse. Vedere anche: provider di ricerca federato, connettore di ricerca, descrittore OpenSearch, standard OpenSearch.

**connettore ricerca federata**

Vedere la definizione per: connettore di ricerca.

**provider di ricerca federato**

Un servizio Web, implementato da un archivio dati, che supporta i protocolli utilizzati da Windows 7 in modo che Windows 7 e versioni successive possano eseguire ricerche nell'archivio dati in modalità remota. Vedere anche: descrittore OpenSearch, standard OpenSearch.

**associazione file**

Vedere definizione per: associazione tipo di file.

**formato file**

Formato per i dati archiviati in un file con una specifica di formato documentata. Gli esempi includono OLE DocFile, OPC, XML, ZIP e altre specifiche del formato di file noto. Gli autori dei tipi di file usano in genere un formato di file esistente come base di un nuovo tipo di file. Un formato di file può essere semplicemente una definizione di cui non viene creata un'istanza come tipo di file.

**gestore formato file**

Questo termine è un sinonimo del gestore dei tipi di file. Vedere definizione per: gestore tipo di file.

**estensione del nome file**

Vedere la definizione per: estensione del nome file.

**estensione del nome file**

L'indicatore principale di un tipo di file per file system elementi è la parte del nome file che segue il punto finale. L'estensione del nome file non può contenere spazi o caratteri non ASCII e si applica solo ai file (non alle cartelle). Le estensioni di file vengono confrontate utilizzando una funzione di confronto che non è sensibile a case o impostazioni locali. Vedere anche: formato di file, tipo di file.

**tipo di file**

Un particolare valore di estensione del nome di file, ad esempio ". htm" o ". jpg", che definisce una classe di file che sono dello stesso tipo e hanno un set comune di associazioni. Vedere anche: tipo, associazione del tipo di file.

**associazione di tipi di file**

Per un'estensione di file particolare, gli elementi di matrice di associazione che definiscono dove possono essere registrati i gestori e altri attributi. Vedere anche: array di associazioni, tipo di file.

**personalizzazione del tipo di file**

Un'associazione che consente a Shell di personalizzare il modo in cui la shell considera un tipo di file. Le personalizzazioni dei tipi di file includono: specificando l'applicazione utilizzata per aprire il file quando si fa doppio clic su di esso, aggiungendo comandi al menu di scelta rapida per un tipo di file, specificando un'icona personalizzata, specificando un tipo di contenuto MIME da associare a un tipo di file, specificando un tipo percepito e specificando una o più applicazioni associate dal tipo di file con Vedere anche: PerceivedType.

**gestore tipo di file**

Gestore registrato per un tipo di file. Vedere anche: handler.

**filter**

Implementazione dell'interfaccia IFilter. Apre i file di un tipo di file specifico e filtra le proprietà e i blocchi di testo per l'indicizzatore. I filtri sono associati ai tipi di file, come indicato dalle estensioni dei nomi di file, dai tipi MIME o dagli identificatori di classe (CLSID). Sebbene un filtro sia in grado di gestire più tipi di file, ogni tipo di file funziona con un solo filtro.

**cartella**

Vedere la definizione per: container.

## <a name="h"></a>H

**gestore**

Oggetto COM che fornisce la funzionalità per un elemento della shell. La maggior parte delle origini dati della Shell offre un sistema estensibile per l'associazione di gestori agli elementi. Ad esempio, la cartella file system usa il sistema di associazione per cercare i gestori per un tipo di file specifico. Vedere anche: associazione di file, tipo di file, personalizzazione del tipo di file.

## <a name="i"></a>I

**gestore icone**

Gestore che fornisce le informazioni necessarie per generare e memorizzare nella cache un'icona per un elemento. L'archivio dati file system supporta il caricamento di un gestore di icone per un elemento in base al tipo di file, consentendo a tale gestore di fornire un'icona utilizzata per tutte le istanze del tipo di file.

**index**

n. Catalogo che archivia il contenuto e le proprietà degli elementi della Shell per consentire ricerche rapide. Vedere anche: Catalog, indicizzatore, indicizzazione, indice invertito. v. Per accedere alle origini contenuto, filtrare le origini per il contenuto e le proprietà e inserire i valori estratti nell'indice (per il testo) e nell'archivio delle proprietà di ricerca di Windows (per le proprietà). Vedere anche: origine del contenuto, indice, indicizzatore, indice invertito.

**indicizzatore**

Applicazione che esegue l'indicizzazione o coordina l'indicizzazione. Vedere anche: indice, indicizzazione, indice invertito.

**gestore infotip**

Gestore che fornisce il testo popup quando l'utente posiziona il puntatore del mouse su un oggetto dell'interfaccia utente.

**indice invertito**

Struttura permanente che contiene il contenuto Estratto da file da ricerca di Windows. Il testo è organizzato in un indice che esegue il mapping da una parola di una proprietà a un elenco di documenti e posizioni all'interno di un documento che contiene la parola. Di conseguenza, un indice invertito è l'inverso del processo di estrazione del testo e delle proprietà dal documento e di inserimento nell'indicizzatore. Vedere anche: index, indexer, indicizzazione.

**item**

Vedere la definizione di: elemento della shell.

**classe Item**

Vedere definizione per: tipo di file.

## <a name="k"></a>K

**Tipologia**

Proprietà che fornisce un nome descrittivo per l'utente e può essere associata a un elenco di proprietà e a un modello di layout. Il tipo è stato introdotto in Windows Vista per esprimere una nozione di tipo file più intuitiva per l'utente finale ed è stata definita come una proprietà di stringa multivalore (valori stringa canonici), pertanto è possibile avere un valore Kind "audio; video" o "link; Document". Alcuni nomi descrittivi dei tipi sono già associati a proprietà e modelli di layout. Ad esempio, gli elementi associati a kind. Picture e gli elementi associati a Kind.Document visualizzano proprietà diverse anche quando si trovano nella stessa visualizzazione. Ogni tipo di elemento può essere associato a uno dei quattro modelli di layout univoci che definiscono il numero di proprietà visualizzate per ogni elemento e il relativo layout. Vedere anche: associazione di tipo, visualizzazione contenuto, modello di layout.

**Associazione di tipo**

Proprietà nel sistema di proprietà, denominata System. Kind, che determina quali modelli di UX vengono visualizzati per un file. Questa proprietà fornisce anche un nome descrittivo per il tipo dell'elemento ed è collegato all'estensione del nome di file. Vedere anche: Kind.

## <a name="l"></a>L

**modello layout**

Uno dei diversi accordi per la visualizzazione delle proprietà. In Windows 7 e versioni successive, quando si registra un nuovo tipo di file, è possibile usare la visualizzazione contenuto per registrare un elenco di proprietà e un modello di layout personalizzati per il tipo di file. È possibile scegliere tra quattro diversi modelli di layout: Alpha (per i risultati della ricerca di documenti contenenti frammenti di codice), beta (per i risultati della ricerca tramite posta elettronica con frammenti di codice), gamma (simile ad Alpha ma con layout a due righe anziché quattro) e Delta (per visualizzare molte proprietà più brevi, ad esempio con musica e immagini). Vedere anche: visualizzazione del contenuto, tipo, associazione di tipo.

## <a name="m"></a>M

**gestore di metadati**

Questo termine viene talvolta usato per indicare il gestore della proprietà. Vedere la definizione di: gestore della proprietà.

## <a name="n"></a>N

**estensione dello spazio dei nomi**

Vedere la definizione di: origine dati della shell.

**percorso dello spazio dei nomi**

Processo helper che attraversa lo spazio dei nomi di un contenitore o di un set di contenitori, individuando ogni elemento e possibilmente eseguendo un'operazione con ognuno di essi. L'interfaccia INamespaceWalk può essere utilizzata per esaminare qualsiasi parte dello spazio dei nomi di Esplora risorse o per individuare gli elementi a cui fa riferimento un oggetto dati o una vista. I verbi del contenitore (ad esempio "Play" nei contenitori degli artisti) descrivono lo spazio dei nomi e individuano gli elementi.

**query in linguaggio naturale**

Vedere la definizione di: Natural Query Syntax (NQS).

**Sintassi di query naturali (NQS)**

Una sintassi di query più rilassata rispetto a AQS e sembra più simile alla lingua umana. NQS può essere usato da Windows Search per eseguire una query sull'indice se è selezionato NQS anziché il valore predefinito AQS. Vedere anche: sintassi di query avanzata (AQS).

**parole non significative**

Parola che viene ignorata da ricerca di Windows quando è presente nelle restrizioni specificate per la query di ricerca, perché presenta un valore discriminatorio minimo. Gli esempi includono "and" e "."

**NQS**

Vedere la definizione di: Natural Query Syntax (NQS).

## <a name="o"></a>O

**Collegamento di oggetti e database di incorporamento (OLE DB)**

Un set standard di interfacce che fornisce accesso eterogeneo a origini diverse di informazioni situate ovunque, ad esempio file System, cartelle di posta elettronica e database.

**OLE DB**

Vedere la definizione per: collegamento di oggetti e database di incorporamento.

**Descrittore OpenSearch**

Un file XML che descrive le connessioni server disponibili e i formati dei risultati per un'origine dati specifica basata sul Web. Questo file contiene uno o più modelli di URL e usa un'estensione del nome di file osdx quando si interagisce con la shell di Windows. Una descrizione OpenSearch viene a volte definita connettore di ricerca, anche se è solo la parte della descrizione di un connettore. Vedere anche: connettore di ricerca.

**Standard OpenSearch**

Raccolta di formati e protocolli semplici usati per la condivisione dei risultati della ricerca. Per ulteriori informazioni, vedere il sito Web OpenSearch ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**PerceivedType**

Ampia categoria di tipi di formato di file. PerceivedType è stato introdotto in Windows XP e supporta un set limitato di tipi di file noti, ad esempio immagini, testo, audio e tipi di file compressi. I tipi di file, generalmente i tipi di file pubblici, possono anche avere un tipo percepito. Ad esempio, i tipi di file di immagine. bmp,. png,. jpg e. gif sono anche di tipo percepito, image. A livello di programmazione, PerceivedType viene espresso come numero intero. Poiché è presente codice che usa Kind e PerceivedType, i proprietari del formato di file devono registrarsi entrambi. Ad esempio, "Play All" dipende da PerceivedType. Vedere anche: tipo di file.

**gestore di anteprime**

Gestore che produce rapidamente una visualizzazione semplificata e di sola lettura dell'elemento della shell da visualizzare nel riquadro di anteprima di Esplora risorse.

**Previewer**

Questo termine viene talvolta usato per indicare il gestore di anteprime. Vedere la definizione di: gestore di anteprime.

**Gestore proprietà**

Gestore che converte i dati archiviati in un file in uno schema strutturato riconosciuto da e a cui è possibile accedere da Esplora risorse, da Windows Search e da altre applicazioni. Questi sistemi possono quindi interagire con il gestore delle proprietà per scrivere e leggere le proprietà da e verso il file. I dati tradotti includono la visualizzazione dettagli, infotip, il riquadro dettagli, le pagine delle proprietà e così via. Ogni gestore di proprietà è associato a un particolare tipo di file, identificato dall'estensione del nome file. Vedere anche: sistema di proprietà.

**gestore della finestra delle proprietà**

Gestore utilizzato per creare finestre delle proprietà personalizzate con le immagini e i controlli dell'interfaccia utente che consentono l'interazione personalizzata con un tipo di file.

**sistema di proprietà**

Sistema di lettura/scrittura estendibile di definizioni di dati che utilizza proprietà implementate come coppie nome-valore. Vedere anche: gestore della proprietà, elemento della shell.

**valore proprietà**

Valore associato a un nome di proprietà per un elemento della shell. Ad esempio, "Author", "size" e "date taked" sono proprietà. I valori delle proprietà vengono espressi come una struttura PROPVARIANT.

**gestore di protocollo**

Gestore che accede a origini contenuto e fornisce un oggetto IUrlAccessor per un protocollo e un URL specificati. I gestori di protocollo estendono la funzionalità di ricerca di Windows e possono fornire notifiche delle modifiche agli indicizzatori. Per indicizzare tipi specifici di archivi dati sono necessari gestori di protocollo diversi. Per garantire un'esperienza utente ragionevole, è necessario specificare anche un'origine dati della Shell per l'archivio dati, oltre a implementare il gestore di protocollo. Il gestore di protocollo espone gli elementi nell'archivio dati all'indicizzatore, mentre l'origine dati della shell espone gli elementi nell'archivio dati alla Shell.

## <a name="r"></a>R

**restrizione**

Condizione che un file deve soddisfare per essere incluso nei risultati della ricerca restituiti da ricerca di Windows.

**row**

Colonne che contengono i valori di proprietà che descrivono un singolo risultato dal set di oggetti che corrispondono alle restrizioni specificate in una query di ricerca.

**righe**

Set di righe restituite nei risultati della ricerca.

## <a name="s"></a>S

**Cerca connettore**

Un file XML che contiene informazioni su un archivio dati. I connettori di ricerca vengono distribuiti per la ricerca federata.

**Cerca utente**

Componente o applicazione che esegue una query sull'indice.

**Cerca Federazione**

Vedere la definizione di: provider di ricerca federato.

**provider di ricerca**

Componente o applicazione che fornisce dati a Windows Search.

**ambito di ricerca**

Questo termine viene talvolta usato per indicare l'ambito della ricerca per indicizzazione. Vedere definizione per: ambito di ricerca per indicizzazione.

**Origine dati Shell**

Componente utilizzato per estendere lo spazio dei nomi della shell ed esporre gli elementi in un archivio dati. In passato, l'origine dati della shell era denominata estensione dello spazio dei nomi della shell. Vedere anche: contenitore, gestore, elemento della shell.

**Estensione della shell**

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere definizione per: gestore tipo di file.

**Gestore dell'estensione della shell**

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere definizione per: gestore tipo di file.

**Gestore Shell**

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere definizione per: gestore tipo di file.

**Elemento della shell**

Una singola parte di contenuto. Alcuni elementi della shell sono origini di contenuto e altri no. Una cartella è un'origine di contenuto, ad esempio, ma non è presente un file con estensione jpg. I gestori di tipi di file espongono gli elementi della shell. In alcuni contesti "Item" viene usato per distinguere i contenitori da non contenitori. Vedere anche: contenitore, origine del contenuto, gestore del tipo di file.

**Estensione dello spazio dei nomi shell**

Questo termine viene talvolta usato per indicare l'origine dati della shell. Vedere la definizione di: origine dati della shell.

**menu di scelta rapida**

Interfaccia utente utilizzata per presentare una raccolta di verbi associati a un elemento dell'interfaccia utente, ad esempio un file o una cartella.

**Gestore del menu di scelta rapida**

Gestore che aggiunge verbi per un elemento o elementi. Questi verbi vengono in genere visualizzati in un menu di scelta rapida. Vedere anche: menu di scelta rapida.

**verbo statico**

Verbo che si applica a un elemento della shell senza che sia necessario controllare lo stato corrente di un elemento o di un sistema. Un verbo statico si basa su una registrazione statica degli elementi associati di un elemento e non cambia.

## <a name="t"></a>T

**gestore anteprime**

Gestore che fornisce un'immagine statica per rappresentare un elemento della shell.

**provider di anteprime**

Questo termine viene talvolta usato per indicare il gestore di anteprime. Vedere la definizione per: gestore anteprime.

## <a name="u"></a>U

**Modello di URL**

Stringa di connessione basata su URL utilizzata per eseguire una query su un server Web per i risultati della ricerca. Il modello ha un aspetto simile a un URL, ma contiene diversi valori segnaposto (ad esempio {searchTerms}) che il client deve sostituire con i dati sui risultati che desidera recuperare. La definizione di modelli di URL è fondamentale per l'implementazione degli standard federati di ricerca e OpenSearch.

**nome descrittivo del tipo**

Vedere la definizione per: Kind.

## <a name="v"></a>V

**verb**

Singola azione che può essere chiamata da un elemento della shell. Gli esempi includono Open e Print. I verbi sono talvolta denominati comandi o attività. Vedere anche: verbo dinamico, gestore del menu di scelta rapida, verbo statico.

**gestore di verbi**

Questo termine viene talvolta usato per indicare il gestore dei menu di scelta rapida. Vedere definizione per: gestore del menu di scelta rapida.

## <a name="w"></a>W

**passeggiata**

Vedere la definizione di: percorso dello spazio dei nomi.

**Windows Search**

Vedere la definizione per: servizio Windows Search.

**Archivio delle proprietà di ricerca di Windows**

Cache dei valori delle proprietà utilizzati nell'implementazione del servizio Windows Search. Questi valori di proprietà possono essere sottoposti a query a livello di codice utilizzando il provider di OLE DB di ricerca di Windows. L'archivio delle proprietà di ricerca di Windows raccoglie e archivia le proprietà generate dai gestori di filtro o dai gestori di proprietà quando un elemento, ad esempio un documento di Word, viene indicizzato. Questo archivio viene eliminato e ricompilato quando l'indice viene ricompilato.

**Servizio Windows Search**

Si riferisce a Windows Search 3,0 e versioni successive. Questo servizio analizza un set di documenti, estrae informazioni utili e quindi organizza le informazioni estratte in modo che le proprietà di tali documenti possano essere restituite in modo efficiente in risposta alle query. Vedere anche: catalog.
