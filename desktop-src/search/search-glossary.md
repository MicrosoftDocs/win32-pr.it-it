---
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Windows Glossario della ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efe8bbe07badc7575cc3aba83100814d601bc5c8ebca24961b198950b2e5e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844651"
---
# <a name="windows-search-glossary"></a>Windows Glossario della ricerca

## <a name=""></a>\#

**File con estensione osd**

OpenSearch File descrittore.

**File con estensione osdx**

File XML OpenSearch descrizione dettagliata che descrive le connessioni server disponibili e i formati dei risultati per un'origine dati specifica basata sul Web. Viene usato per interagire con la shell Windows shell. Vedere anche: OpenSearch descrittore.

## <a name="a"></a>A

**Sintassi di query avanzata (AQS)**

La sintassi di query predefinita usata da Windows ricerca per eseguire query sull'indice e per perfezionare e restringere i parametri di ricerca. AQS è destinato principalmente all'utente e può essere usato dagli utenti per compilare query AQS, ma può essere usato anche a livello di codice. Vedere anche: Sintassi di query naturali (NQS).

**AQS**

Vedere la definizione per: Advanced Query Syntax (AQS).

**Associazione**

Mapping di un'estensione di file (ad esempio, .mp3) o di un protocollo (ad esempio http) a un identificatore programmatico (ProgID). Questo mapping viene archiviato nel Registro di sistema come impostazione per utente con fallback per computer. Le applicazioni che fanno parte del sistema Programmi predefiniti impostano il mapping di associazione per l'estensione o il protocollo del nome file in modo che punti alle chiavi ProgID di cui sono proprietari.

**matrice di associazioni**

Elenco ordinato di percorsi del Registro di sistema usati per archiviare informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, ad esempio l'icona e il nome visualizzato del tipo. Ad esempio, un file .jpg ha la matrice di associazioni seguente in un sistema Windows predefinito: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\.jpg", "HKCR \\ SystemFileAssociations \\ image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

**Atom**

Xml Schema usato per i feed Web e la distribuzione del contenuto, sviluppato come alternativa a Really Simple Syndication (RSS). Il formato di diffusione Atom è stato pubblicato come standard proposto da IETF in RFC 4287.

## <a name="b"></a>B

**bind**

Per caricare o associare il codice ai dati. Ad esempio, un gestore può essere associato a un'origine dati shell.

**Associazione**

Richiesta in una query di ricerca per una colonna in un set di righe restituito. L'associazione specifica una proprietà da includere nei risultati della ricerca.

**bookmark**

Indicatore che identifica in modo univoco una riga all'interno di un set di righe.

## <a name="c"></a>C

**nome canonico**

Nome univoco di una risorsa. Canonical significa "in base alle regole". Vedere anche: nome canonico del verbo.

**nome canonico del verbo**

Nome indipendente dalla lingua che può essere utilizzato a livello di codice per fare riferimento a un verbo, indipendentemente dalla stringa localizzata nell'interfaccia utente. Vedere anche: nome canonico, verbo.

**catalog**

Unità di livello superiore dell'organizzazione in Windows ricerca. Un catalogo rappresenta un set di documenti indicizzati su cui è possibile eseguire query. Un catalogo è costituito da una tabella delle proprietà con il testo o il valore e la posizione corrispondente archiviata nelle colonne della tabella. Ogni riga della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni colonna della tabella corrisponde a una proprietà . Vedere anche: index, Windows servizio di ricerca.

**category**

Raggruppamento gerarchico di righe. Ad esempio, un risultato della query che contiene le colonne autore e titolo può essere categorizzato in base all'autore. In questo esempio ogni gruppo di righe che contiene lo stesso valore per author costituisce una categoria.

**Capitolo**

Raccolta di righe all'interno di un set di righe. Vedere anche: catalogo, categoria.

**column**

Contenitore per un singolo tipo di informazioni in una riga. Le colonne vengono mappate ai nomi delle proprietà e specificano quali proprietà vengono usate per gli elementi dell'albero dei comandi della query di ricerca. Vedere anche: category.

**albero dei comandi**

Combinazione di restrizioni, categorie e ordinamenti specificati per la query di ricerca. Vedere anche: category.

**container**

Tipo di elemento della shell che può contenere altri elementi. Gli elementi in un contenitore vengono esposti allo spazio dei nomi Shell usando un'origine dati shell. Ad esempio, cartelle, unità, server di rete e file compressi con .zip di file. Vedere anche: Origine dati shell, cartella, elemento della shell.

**content**

Testo e proprietà associati a un elemento della shell o a un'origine di contenuto che può essere indicizzata.

**origine del contenuto**

Elemento accessibile dall'indicizzatore. Le origini di contenuto sono indirizzabili da un URL e vengono fornite all'indicizzatore da un gestore di protocollo. Ad esempio: file system file e cartelle, elementi e cartelle di Microsoft Outlook, record di database ed elementi archiviati SharePoint Microsoft. Un'origine contenuto può essere esposta come elementi della shell implementando un'origine dati shell. Vedere anche: content, shell item.

**content view (visualizzazione contenuto)**

Visualizzazione in Windows Explorer (disponibile in Windows 7 e versioni successive) che visualizza il contenuto più pertinente per ogni elemento dell'elenco in base all'estensione del nome file o all'associazione kind. La visualizzazione contenuto usa una logica di ridimensionamento che elimina le proprietà quando le dimensioni della finestra diminuiscono per garantire che le proprietà più critiche siano ancora leggibili. Vedere anche: modello di layout, tipo, associazione di tipo.

**modalità di visualizzazione del contenuto**

Vedere la definizione per: visualizzazione contenuto.

**menu di scelta rapida**

Questo termine viene talvolta usato per indicare il menu di scelta rapida. Vedere la definizione per: menu di scelta rapida.

**gestore del menu di scelta rapida**

Questo termine viene talvolta usato per indicare il gestore del menu di scelta rapida. Vedere la definizione per: gestore del menu di scelta rapida.

**ricerca per indicizzazione**

Per eseguire l'iterazione su un ambito di ricerca per indicizzazione, identificando le origini di contenuto che richiedono l'indicizzazione o la nuova indicizzazione.

**ambito della ricerca per indicizzazione**

Raccolta di archivi dati (identificabili dall'URL) che rappresenta il contenuto sottoposto a ricerca per indicizzazione e indici dall'indicizzatore.

**cursor**

Nel contesto dell'indice locale, un cursore è un indicatore per l'utilizzo di una riga o di un piccolo blocco di righe alla volta in un set di dati restituito in un set di risultati. Dopo aver posizionato il cursore su una riga, è possibile eseguire operazioni su tale riga o su un blocco di righe a partire da tale posizione.

## <a name="d"></a>D

**Gestione dati, esplorazione e data mining**

Vedere la definizione per: DMX (Database Mining Extensions).

**gestore dell'oggetto dati**

Gestore che fornisce formati di Appunti aggiuntivi per l'oggetto dati (IDataObject) di un elemento. Gli oggetti dati vengono usati negli scenari di trascinamento della selezione e copia/incolla.

**origine dati**

Questo termine viene talvolta usato per indicare l'archivio dati o l'origine dati shell. Vedere la definizione per: archivio dati, origine dati shell.

**archivio dati**

Un repository di dati. Un archivio dati può essere esposto al modello di programmazione shell come contenitore usando un'origine dati shell. Gli elementi in un archivio dati possono essere indicizzati dal Windows di ricerca usando un gestore di protocollo.

**DMX (Database Mining Extensions)**

Linguaggio di query usato per creare e modificare data mining. I modelli amministrativi per Windows 7, Windows Search e Windows Explorer sono file con estensione admx e si basano sulla tecnologia DMX. I modelli seguenti possono essere personalizzati tramite Criteri di gruppo: Search.admx, Explorer.admx e WindowsExplorer.admx.

**DMX**

Vedere la definizione per: Estensioni di data mining di database.

**document**

Elemento della shell che contiene testo e per il quale è possibile implementazione dell'interfaccia IFilter.

**drop handler**

Gestore che consente a un particolare tipo di elemento di supportare scenari di trascinamento della selezione e copia/incolla.

**drop target**

Oggetto dati trascinato e rilasciato in un file. Vedere anche: gestore dati, gestore di rilascio.

**verbo dinamico**

Verbo che dipende dallo stato di un elemento della shell o del sistema; L'aspetto dell'elemento è basato sullo stato e richiede che il codice in esecuzione determinerà se l'elemento deve essere visualizzato. Vedere anche: gestore del menu di scelta rapida, verbo statico, verbo.

## <a name="e"></a>E

**Comando Explorer**

Oggetto che può essere presentato come pulsante nella parte superiore della finestra di Windows Explorer che fornisce funzionalità per gli elementi e i contenitori in tale finestra. Un'origine dati shell fornisce gli oggetti Windows comando di Esplora oggetti per un particolare elemento del contenitore. I comandi vengono talvolta usati come verbi.

## <a name="f"></a>F

**ricerca federata**

Modello di estendibilità che consente la ricerca di archivi dati e la rappresentazione dei risultati come elementi della shell in Windows Explorer. Vedere anche: provider di ricerca federato, connettore di ricerca, OpenSearch descrittore, OpenSearch standard.

**connettore di ricerca federata**

Vedere la definizione per: cercare il connettore.

**provider di ricerca federato**

Servizio Web, implementato da un archivio dati, che supporta i protocolli usati da Windows 7 in modo che Windows 7 e versioni successive possano eseguire ricerche in tale archivio dati in modalità remota. Vedere anche: OpenSearch descrittore, OpenSearch standard.

**associazione di file**

Vedere la definizione per: associazione del tipo di file.

**formato di file**

Formato per i dati archiviati in un file con una specifica di formato documentata. Ad esempio, OLE DocFile, OPC, XML, ZIP e altre specifiche di formato di file note. Gli autori di tipi di file usano in genere un formato di file esistente come base per un nuovo tipo di file. Un formato di file può essere semplicemente una definizione di cui non viene creata un'istanza come tipo di file.

**gestore del formato di file**

Questo termine è un sinonimo del gestore dei tipi di file. Vedere la definizione per: gestore dei tipi di file.

**estensione di file**

Vedere la definizione per: estensione di file.

**estensione di file**

L'indicatore principale di un tipo di file file system elementi, è la parte del nome del file che segue il punto finale. L'estensione del nome file non può contenere spazi o caratteri non ASCII e si applica solo ai file (non alle cartelle). Le estensioni di file vengono confrontate usando una funzione di confronto che non fa distinzione tra maiuscole e minuscole o impostazioni locali. Vedere anche: formato di file, tipo di file.

**tipo di file**

Valore dell'estensione del nome file specifico, ad esempio ".htm" o ".jpg", che definisce una classe di file dello stesso tipo e con un set comune di associazioni. Vedere anche: Tipo, associazione del tipo di file.

**associazione di tipi di file**

Per una particolare estensione di file, gli elementi della matrice di associazione che definiscono dove è possibile registrare gestori e altri attributi. Vedere anche: matrice di associazione, tipo di file.

**personalizzazione del tipo di file**

Associazione che consente a Shell di personalizzare il modo in cui Shell tratta un tipo di file. Le personalizzazioni dei tipi di file includono: specifica dell'applicazione usata per aprire il file quando si fa doppio clic, aggiunta di comandi al menu di scelta rapida per un tipo di file, specifica di un'icona personalizzata, specifica di un tipo di contenuto MIME da associare a un tipo di file, specifica di un tipo percepito e specifica di una o più applicazioni associate dal tipo di file alla finestra di dialogo Apri con . Vedere anche: PerceivedType.

**gestore del tipo di file**

Gestore registrato per un tipo di file. Vedere anche: handler.

**filter**

Implementazione dell'interfaccia IFilter. Apre i file di un particolare tipo di file e filtra le proprietà e i blocchi di testo per l'indicizzatore. I filtri sono associati ai tipi di file, come denotato da estensioni di file, tipi MIME o identificatori di classe (CLSID). Anche se un filtro può gestire più tipi di file, ogni tipo di file funziona con un solo filtro.

**Cartella**

Vedere la definizione per: contenitore.

## <a name="h"></a>H

**Gestore**

Oggetto COM che fornisce funzionalità per un elemento della shell. La maggior parte delle origini dati shell offre un sistema estendibile per l'associazione di gestori agli elementi. Ad esempio, la file system usa il sistema di associazione per cercare i gestori per un particolare tipo di file. Vedere anche: associazione di file, tipo di file, personalizzazione del tipo di file.

## <a name="i"></a>I

**gestore dell'icona**

Gestore che fornisce le informazioni necessarie per generare e memorizzare nella cache un'icona per un elemento. L'archivio dati file system supporta il caricamento di un gestore di icone per un elemento in base al tipo di file, consentendo a tale gestore di fornire un'icona usata per tutte le istanze di tale tipo di file.

**index**

n. Catalogo che archivia il contenuto e le proprietà degli elementi della shell per consentire ricerche rapide. Vedere anche: catalogo, indicizzatore, indicizzazione, indice invertito. v. Per accedere alle origini di contenuto, filtrare le origini per il contenuto e le proprietà e inserire i valori estratti nell'indice (per il testo) e nell'archivio delle proprietà di ricerca di Windows (per le proprietà). Vedere anche: origine del contenuto, indice, indicizzatore, indice invertito.

**Indicizzatore**

Applicazione che esegue l'indicizzazione o coordina l'indicizzazione. Vedere anche: indice, indicizzazione, indice invertito.

**Gestore della descrizione comandi**

Gestore che fornisce testo popup quando l'utente passa il puntatore del mouse su un oggetto dell'interfaccia utente.

**indice invertito**

Struttura persistente che contiene il contenuto estratto dai file Windows ricerca. Il testo è organizzato in un indice che esegue il mapping da una parola in una proprietà a un elenco di documenti e posizioni all'interno di un documento che contiene tale parola. Di conseguenza, un indice invertito è l'inverso del processo di estrazione del testo e delle proprietà dal documento e inserimento nell'indicizzatore. Vedere anche: indice, indicizzatore, indicizzazione.

**item**

Vedere la definizione per: Elemento della shell.

**Classe item**

Vedere la definizione per: tipo di file.

## <a name="k"></a>K

**Tipologia**

Proprietà che fornisce un nome kind descrittivo e può essere associata a un elenco di proprietà e a un modello di layout. Kind è stato introdotto in Windows Vista per esprimere una nozione più semplice da parte dell'utente finale del tipo di file ed è stato definito come una proprietà stringa multivalore (valori stringa canonici), pertanto è possibile avere un valore "audio;video" o "link;document" Kind. Alcuni nomi di tipo descrittivi sono già associati a proprietà e modelli di layout. Ad esempio, gli elementi associati a Kind.Picture e gli elementi associati Kind.Docvisualizzano proprietà diverse anche quando sono nella stessa visualizzazione. Ogni tipo di elemento può essere associato a uno dei quattro modelli di layout univoci che definiscono il numero di proprietà visualizzate per ogni elemento e il relativo layout. Vedere anche: Associazione del tipo, visualizzazione contenuto, modello di layout.

**Associazione di tipo**

Proprietà nel sistema di proprietà, denominata System.Kind, che determina quali modelli dell'esperienza utente vengono visualizzati per un file. Questa proprietà fornisce anche un nome descrittivo per il tipo di elemento ed è collegata all'estensione del nome file. Vedere anche: Kind.

## <a name="l"></a>L

**modello di layout**

Una delle diverse modalità di visualizzazione delle proprietà. In Windows 7 e versioni successive, quando si registra un nuovo tipo di file, è possibile usare la visualizzazione contenuto per registrare un elenco di proprietà personalizzate e un modello di layout per il tipo di file. È possibile scegliere tra quattro modelli di layout diversi: Alfa (per i risultati della ricerca di documenti che contengono frammenti di codice), Beta (per i risultati della ricerca tramite posta elettronica con frammenti di codice), Gamma (simile a Alpha ma con un layout a due righe anziché quattro) e Delta (per visualizzare molte proprietà più brevi, ad esempio con musica e immagini). Vedere anche: visualizzazione contenuto, tipo, associazione di tipo.

## <a name="m"></a>M

**gestore di metadati**

Questo termine viene talvolta usato per indicare il gestore delle proprietà. Vedere la definizione per: gestore delle proprietà.

## <a name="n"></a>N

**estensione dello spazio dei nomi**

Vedere la definizione per: Origine dati della shell.

**procedura per lo spazio dei nomi**

Processo helper che attraversa lo spazio dei nomi di un contenitore o di un set di contenitori, individuando ogni elemento ed eventualmente eseguendo un'operazione con ognuno di essi. L'interfaccia INamespaceWalk può essere usata per percorso in qualsiasi parte dello spazio dei nomi di Windows Explorer o per individuare gli elementi a cui fa riferimento un oggetto dati o una vista. I verbi del contenitore ,ad esempio "play" nei contenitori di Artists, esplorano lo spazio dei nomi e individuano gli elementi.

**query in linguaggio naturale**

Vedere la definizione per: Natural Query Syntax (NQS).

**Sintassi di query naturali (NQS)**

Sintassi di query più disincisa rispetto ad AQS e più simile al linguaggio umano. NQS può essere usato Windows ricerca per eseguire query sull'indice se È selezionato NQS anziché il valore predefinito, AQS. Vedere anche: Advanced Query Syntax (AQS).

**parola non acustica**

Parola ignorata da Windows ricerca quando è presente nelle restrizioni specificate per la query di ricerca, perché ha un valore discriminante minimo. Gli esempi includono "and" e "the".

**NQS**

Vedere la definizione per: Natural Query Syntax (NQS).

## <a name="o"></a>O

**Object Linking and Embedding Database (OLE DB)**

Set standard di interfacce che fornisce accesso eterogeneo a diverse origini di informazioni disponibili ovunque, ad esempio file system, cartelle di posta elettronica e database.

**OLE DB**

Vedere la definizione per: Object Linking and Embedding Database.

**OpenSearch descrittore**

File XML che descrive le connessioni server disponibili e i formati dei risultati per un'origine dati specifica basata sul Web. Questo file contiene uno o più modelli di URL e usa un'estensione di file osdx quando interagisce con Windows Shell. Una OpenSearch viene talvolta definita connettore di ricerca, anche se è solo la parte relativa alla descrizione di un connettore. Vedere anche: Connettore di ricerca.

**OpenSearch standard**

Raccolta di formati e protocolli semplici usati per condividere i risultati della ricerca. Per altre informazioni, vedere il sito Web OpenSearch ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**PerceivedType**

Ampia categoria di tipi di formato di file. PerceivedType è stato introdotto in Windows XP e supporta un set limitato di tipi di file noti (ad esempio, i tipi di file Image, Text, Audio e Compressed). Anche i tipi di file, in genere tipi di file pubblici, possono avere un tipo percepito. Ad esempio, anche i tipi di file di immagine .bmp, .png, .jpg e .gif sono del tipo percepito, immagine. A livello di programmazione, PerceivedType è espresso come integer. Poiché è presente codice che usa Kind e PerceivedType, i proprietari del formato di file devono registrare entrambi. Ad esempio, "riproduci tutto" dipende da PerceivedType. Vedere anche: tipo di file.

**gestore dell'anteprima**

Gestore che produce rapidamente una visualizzazione semplificata e di sola lettura dell'elemento shell da visualizzare nel riquadro di anteprima Windows Explorer.

**Previewer**

Questo termine viene talvolta usato per indicare il gestore di anteprima. Vedere la definizione per: gestore di anteprima.

**gestore delle proprietà**

Gestore che converte i dati archiviati in un file in uno schema strutturato riconosciuto da e accessibile da Windows Explorer, Windows Search e altre applicazioni. Questi sistemi possono quindi interagire con il gestore delle proprietà per scrivere e leggere le proprietà da e verso il file. I dati tradotti includono la visualizzazione dettagli, le descrizioni comandi, il riquadro dei dettagli, le pagine delle proprietà e così via. Ogni gestore di proprietà è associato a un particolare tipo di file, identificato dall'estensione del nome file. Vedere anche: sistema di proprietà.

**gestore della finestra delle proprietà**

Gestore utilizzato per creare finestre delle proprietà personalizzate con immagini e controlli dell'interfaccia utente che consentono l'interazione personalizzata con un tipo di file.

**sistema di proprietà**

Sistema estendibile di lettura/scrittura di definizioni di dati che usa proprietà implementate come coppie nome-valore. Vedere anche: gestore della proprietà, elemento della shell.

**valore della proprietà**

Valore associato a un nome di proprietà per un elemento della shell. Ad esempio, "Author", "Size" e "Date Taken" sono proprietà. I valori delle proprietà sono espressi come struttura PROPVARIANT.

**gestore di protocollo**

Gestore che accede alle origini di contenuto e fornisce un oggetto IUrlAccessor per un protocollo e un URL specificati. I gestori di protocollo Windows funzionalità di ricerca e possono fornire notifiche di modifica agli indicizzatori. Per indicizzare tipi specifici di archivi dati sono necessari gestori di protocollo diversi. Per offrire un'esperienza utente ragionevole, è necessario fornire anche un'origine dati shell per l'archivio dati oltre a implementare il gestore di protocollo. Il gestore di protocollo espone gli elementi nell'archivio dati all'indicizzatore, mentre l'origine dati shell espone gli elementi nell'archivio dati alla shell.

## <a name="r"></a>R

**Restrizione**

Condizione che un file deve soddisfare per essere inclusa nei risultati della ricerca restituiti Windows ricerca.

**row**

Colonne contenenti i valori delle proprietà che descrivono un singolo risultato del set di oggetti corrispondenti alle restrizioni specificate in una query di ricerca.

**Righe**

Set di righe restituite nei risultati della ricerca.

## <a name="s"></a>S

**connettore di ricerca**

File XML che contiene informazioni su un archivio dati. I connettori di ricerca vengono distribuiti per la ricerca federata.

**consumer di ricerca**

Componente o applicazione che esegue una query sull'indice.

**Federazione della ricerca**

Vedere la definizione per: provider di ricerca federata.

**provider di ricerca**

Componente o applicazione che fornisce i dati per Windows ricerca.

**ambito di ricerca**

Questo termine viene talvolta usato per indicare l'ambito della ricerca per indicizzazione. Vedere la definizione per: ambito della ricerca per indicizzazione.

**Origine dati shell**

Componente utilizzato per estendere lo spazio dei nomi Shell ed esporre gli elementi in un archivio dati. In passato, l'origine dati Shell è stata definita estensione dello spazio dei nomi Shell. Vedere anche: contenitore, gestore, elemento shell.

**Estensione della shell**

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere la definizione per: gestore del tipo di file.

**Gestore dell'estensione della shell**

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere la definizione per: gestore del tipo di file.

**Gestore della shell**

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere la definizione per: gestore del tipo di file.

**Elemento della shell**

Una singola parte di contenuto. Alcuni elementi della shell sono origini di contenuto e altri no. Una cartella è un'origine di contenuto, ad esempio, ma .jpg file non lo è. I gestori dei tipi di file espongono gli elementi della shell. In alcuni contesti "item" viene usato per distinguere i contenitori dai non contenitori. Vedere anche: contenitore, origine contenuto, gestore del tipo di file.

**Estensione dello spazio dei nomi della shell**

Questo termine viene talvolta usato per indicare l'origine dati shell. Vedere la definizione per: Origine dati della shell.

**menu di scelta rapida**

Interfaccia utente utilizzata per presentare una raccolta di verbi associati a un elemento dell'interfaccia utente, ad esempio un file o una cartella.

**Gestore del menu di scelta rapida**

Gestore che aggiunge verbi per uno o più elementi. Questi verbi vengono in genere visualizzati in un menu di scelta rapida. Vedere anche: menu di scelta rapida.

**verbo statico**

Verbo che si applica a un elemento shell senza dover controllare lo stato corrente di un elemento o di un sistema. Un verbo statico è basato su una registrazione statica degli elementi associati di un elemento e non cambia.

## <a name="t"></a>T

**Gestore dell'anteprima**

Gestore che fornisce un'immagine statica per rappresentare un elemento shell.

**provider di anteprime**

Questo termine viene talvolta usato per indicare il gestore delle anteprime. Vedere la definizione per: gestore di anteprime.

## <a name="u"></a>U

**Modello di URL**

Stringa di connessione basata su URL utilizzata per eseguire query su un server Web per ottenere i risultati della ricerca. Il modello è simile a un URL, ma contiene diversi valori segnaposto (ad esempio {searchTerms}) che il client deve sostituire con i dati sui risultati che vuole recuperare. La definizione dei modelli di URL è fondamentale per implementare la ricerca federata e OpenSearch standard.

**nome descrittivo del tipo**

Vedere la definizione per: Kind.

## <a name="v"></a>V

**Verbo**

Singola azione che può essere chiamata da un elemento shell. Ad esempio, aprire e stampare. I verbi vengono talvolta definiti comandi o attività. Vedere anche: verbo dinamico, gestore del menu di scelta rapida, verbo statico.

**Gestore di verbi**

Questo termine viene talvolta usato per indicare il gestore del menu di scelta rapida. Vedere la definizione per: gestore del menu di scelta rapida.

## <a name="w"></a>W

**Camminare**

Vedere la definizione per: guida allo spazio dei nomi.

**Windows Search**

Vedere la definizione per: Windows servizio di ricerca.

**Windows Cercare nell'archivio delle proprietà**

Cache dei valori delle proprietà usati nell'implementazione del Windows servizio di ricerca. È possibile eseguire query su questi valori di proprietà a livello di codice usando il provider Windows ricerca OLE DB dati. L Windows di proprietà Di ricerca raccoglie e archivia le proprietà generate dai gestori di filtri o dai gestori delle proprietà quando un elemento, ad esempio un documento di Word, viene indicizzato. Questo archivio viene eliminato e ricompilato quando l'indice viene ricompilato.

**Windows servizio di ricerca**

Fa riferimento Windows Ricerca 3.0 e successive. Questo servizio analizza un set di documenti, estrae informazioni utili e quindi organizza le informazioni estratte in modo che le proprietà di tali documenti possano essere restituite in modo efficiente in risposta alle query. Vedere anche: catalogo.
