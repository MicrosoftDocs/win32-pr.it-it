---
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
title: Glossario della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345396"
---
# <a name="shell-glossary"></a>Glossario della shell

## <a name="a"></a>A

<dl> <dt>

**associazione**
</dt> <dd>

Mapping di un'estensione di file (ad esempio,. mp3) o di un protocollo (ad esempio, http) a un identificatore a livello di codice (ProgID). Questo mapping viene archiviato nel registro di sistema come impostazione per utente con fallback per computer. Le applicazioni che fanno parte del sistema di programmi predefiniti impostano il mapping di associazione per l'estensione o il protocollo del nome di file in modo che punti alle chiavi ProgID di loro proprietà.

</dd> <dt>

**array di associazioni**
</dt> <dd>

Elenco ordinato di percorsi del registro di sistema utilizzati per archiviare informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, come l'icona e il nome visualizzato del tipo. Ad esempio, un file con estensione jpg presenta la seguente matrice di associazioni in un sistema Windows predefinito: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "HKCR \\ SystemFileAssociations \\ image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**bind**
</dt> <dd>

Per caricare o associare il codice ai dati. Ad esempio, un gestore può essere associato a un'origine dati della shell.

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**nome canonico**
</dt> <dd>

Nome univoco di una risorsa. "Canonical" indica "secondo le regole". Vedere anche: nome del verbo canonico.

</dd> <dt>

**nome del verbo canonico**
</dt> <dd>

Nome indipendente dalla lingua che può essere utilizzato a livello di codice per fare riferimento a un verbo, indipendentemente dalla stringa localizzata nell'interfaccia utente. Vedere anche: nome canonico, verbo.

</dd> <dt>

**container**
</dt> <dd>

Tipo di elemento della shell che può contenere altri elementi. Gli elementi in un contenitore vengono esposti allo spazio dei nomi della shell utilizzando un'origine dati della shell. Gli esempi includono cartelle, unità, server di rete e file compressi con estensione zip. Vedere anche: origine dati della shell, cartella, elemento della shell.

</dd> <dt>

**content**
</dt> <dd>

Testo e proprietà associati a un elemento della shell o a un'origine di contenuto che può essere indicizzata.

</dd> <dt>

**origine contenuto**
</dt> <dd>

Elemento a cui è possibile accedere dall'indicizzatore. Le origini di contenuto sono indirizzabili da un URL e vengono fornite all'indicizzatore da un gestore di protocollo. Gli esempi includono: file system file e cartelle, elementi e cartelle di Microsoft Outlook, record del database e elementi archiviati di Microsoft SharePoint. Un'origine di contenuto può essere esposta come elementi della shell implementando un'origine dati della shell. Vedere anche: contenuto, elemento della shell.

</dd> <dt>

**content view (visualizzazione contenuto)**
</dt> <dd>

Visualizzazione in Esplora risorse (disponibile in Windows 7 e versioni successive) che Visualizza il contenuto più rilevante per ogni elemento nell'elenco in base all'estensione del nome file o all'associazione di tipo. La visualizzazione contenuto usa una logica di ridimensionamento che elimina le proprietà quando le dimensioni della finestra diminuiscono per garantire che le proprietà più importanti abbiano ancora spazio per essere leggibili in modo chiaro. Vedere anche: modello di layout, tipo, associazione di tipo.

</dd> <dt>

**modalità di visualizzazione contenuto**
</dt> <dd>

Vedere la definizione di: visualizzazione contenuto.

</dd> <dt>

**menu di scelta rapida**
</dt> <dd>

Questo termine viene talvolta usato per indicare il menu di scelta rapida. Vedere definizione per: menu di scelta rapida.

</dd> <dt>

**gestore menu di scelta rapida**
</dt> <dd>

Questo termine viene talvolta usato per indicare il gestore dei menu di scelta rapida. Vedere definizione per: gestore del menu di scelta rapida.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**gestore dell'oggetto dati**
</dt> <dd>

Gestore che fornisce altri formati degli Appunti per l'oggetto dati (IDataObject) di un elemento. Gli oggetti dati vengono usati negli scenari di trascinamento della selezione e di copia e incolla.

</dd> <dt>

**origine dati**
</dt> <dd>

Questo termine viene talvolta usato per indicare l'origine dati dell'archivio dati o della shell. Vedere la definizione per: archivio dati, origine dati Shell.

</dd> <dt>

**archivio dati**
</dt> <dd>

Repository di dati. Un archivio dati può essere esposto al modello di programmazione della shell come contenitore usando un'origine dati della shell. Gli elementi in un archivio dati possono essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo.

</dd> <dt>

**composizione del desktop**
</dt> <dd>

Funzionalità di Windows Vista che consente di disegnare singole finestre per le superfici fuori schermo nella memoria video anziché il disegno direttamente sul dispositivo di visualizzazione principale.

</dd> <dt>

**document**
</dt> <dd>

Elemento della shell che contiene testo e per il quale è possibile implementare l'interfaccia IFilter.

</dd> <dt>

**gestore di trascinamento**
</dt> <dd>

Gestore che consente a un particolare tipo di elemento di supportare gli scenari di trascinamento della selezione e di copia e incolla.

</dd> <dt>

**destinazione di rilascio**
</dt> <dd>

Oggetto dati trascinato e rilasciato su un file. Vedere anche: gestore dati, Drop Handler.

</dd> <dt>

**verbo dinamico**
</dt> <dd>

Verbo che dipende dallo stato di un elemento della shell o del sistema; l'aspetto dell'elemento è basato sullo stato e richiede che il codice in esecuzione determini se l'elemento deve essere visualizzato. Vedere anche: gestore del menu di scelta rapida, verbo statico, verbo.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Comando Explorer**
</dt> <dd>

Oggetto che può essere visualizzato come pulsante nella parte superiore della finestra di Esplora risorse che fornisce la funzionalità per gli elementi e i contenitori in tale finestra. Un'origine dati della shell fornisce gli oggetti comando di Esplora risorse per un elemento contenitore specifico. I comandi vengono talvolta usati come verbi.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**associazione file**
</dt> <dd>

Vedere definizione per: associazione tipo di file.

</dd> <dt>

**formato file**
</dt> <dd>

Formato per i dati archiviati in un file con una specifica di formato documentata. Gli esempi includono OLE DocFile, OPC, XML, ZIP e altre specifiche del formato di file noto. Gli autori dei tipi di file usano in genere un formato di file esistente come base di un nuovo tipo di file. Un formato di file può essere semplicemente una definizione di cui non viene creata un'istanza come tipo di file.

</dd> <dt>

**gestore formato file**
</dt> <dd>

Questo termine è un sinonimo del gestore dei tipi di file. Vedere definizione per: gestore tipo di file.

</dd> <dt>

**estensione del nome file**
</dt> <dd>

L'indicatore principale di un tipo di file per file system elementi è la parte del nome file che segue il punto finale. L'estensione del nome file non può contenere spazi o caratteri non ASCII e si applica solo ai file (non alle cartelle). Le estensioni di file vengono confrontate utilizzando una funzione di confronto che non è sensibile a case o impostazioni locali. Vedere anche: formato di file, tipo di file.

</dd> <dt>

**tipo di file**
</dt> <dd>

Un particolare valore di estensione del nome di file, ad esempio ". htm" o ". jpg", che definisce una classe di file che sono dello stesso tipo e hanno un set comune di associazioni. Vedere anche: tipo, associazione del tipo di file.

</dd> <dt>

**associazione di tipi di file**
</dt> <dd>

Per un'estensione di file particolare, gli elementi di matrice di associazione che definiscono dove possono essere registrati i gestori e altri attributi. Vedere anche: array di associazioni, tipo di file.

</dd> <dt>

**personalizzazione del tipo di file**
</dt> <dd>

Un'associazione che consente a Shell di personalizzare il modo in cui la shell considera un tipo di file. Le personalizzazioni dei tipi di file includono: specificando l'applicazione utilizzata per aprire il file quando si fa doppio clic su di esso, aggiungendo comandi al menu di scelta rapida per un tipo di file, specificando un'icona personalizzata, specificando un tipo di contenuto MIME da associare a un tipo di file, specificando un tipo percepito e specificando una o più applicazioni associate dal tipo di file con Vedere anche: PerceivedType.

</dd> <dt>

**gestore tipo di file**
</dt> <dd>

Gestore registrato per un tipo di file. Vedere anche: handler.

</dd> <dt>

**cartella**
</dt> <dd>

Vedere la definizione per: container.

</dd> <dt>

**PIDL completo**
</dt> <dd>

PIDL che descrive in modo univoco un oggetto relativo alla cartella desktop.

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**gestore**
</dt> <dd>

Oggetto COM che fornisce la funzionalità per un elemento della shell. La maggior parte delle origini dati della Shell offre un sistema estensibile per l'associazione di gestori agli elementi. Ad esempio, la cartella file system usa il sistema di associazione per cercare i gestori per un tipo di file specifico. Vedere anche: associazione di file, tipo di file, personalizzazione del tipo di file.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**gestore icone**
</dt> <dd>

Gestore che fornisce le informazioni necessarie per generare e memorizzare nella cache un'icona per un elemento. L'archivio dati file system supporta il caricamento di un gestore di icone per un elemento in base al tipo di file, consentendo a tale gestore di fornire un'icona utilizzata per tutte le istanze del tipo di file.

</dd> <dt>

**gestore infotip**
</dt> <dd>

Gestore che fornisce il testo popup quando l'utente posiziona il puntatore del mouse su un oggetto dell'interfaccia utente.

</dd> <dt>

**item**
</dt> <dd>

Vedere la definizione di: elemento della shell.

</dd> <dt>

**classe Item**
</dt> <dd>

Vedere definizione per: tipo di file.

</dd> <dt>

**elenco degli identificatori di elemento**
</dt> <dd>

Sequenza di una o più strutture SHITEMID che definiscono in modo univoco un oggetto relativo a un oggetto radice.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Tipologia**
</dt> <dd>

Proprietà che fornisce un nome descrittivo per l'utente e può essere associata a un elenco di proprietà e a un modello di layout. Il tipo è stato introdotto in Windows Vista per esprimere una nozione di tipo file più intuitiva per l'utente finale ed è stata definita come una proprietà di stringa multivalore (valori stringa canonici), pertanto è possibile avere un valore Kind "audio; video" o "link; Document". Alcuni nomi descrittivi dei tipi sono già associati a proprietà e modelli di layout. Ad esempio, gli elementi associati a kind. Picture e gli elementi associati a Kind.Document visualizzano proprietà diverse anche quando si trovano nella stessa visualizzazione. Ogni tipo di elemento può essere associato a uno dei quattro modelli di layout univoci che definiscono il numero di proprietà visualizzate per ogni elemento e il relativo layout. Vedere anche: associazione di tipo, visualizzazione contenuto, modello di layout.

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**modello layout**
</dt> <dd>

Uno dei diversi accordi per la visualizzazione delle proprietà. In Windows 7 e versioni successive, quando si registra un nuovo tipo di file, è possibile usare la visualizzazione contenuto per registrare un elenco di proprietà e un modello di layout personalizzati per il tipo di file. È possibile scegliere tra quattro diversi modelli di layout: Alpha (per i risultati della ricerca di documenti contenenti frammenti di codice), beta (per i risultati della ricerca tramite posta elettronica con frammenti di codice), gamma (simile ad Alpha ma con layout a due righe anziché quattro) e Delta (per visualizzare molte proprietà più brevi, ad esempio con musica e immagini). Vedere anche: visualizzazione del contenuto, tipo, associazione di tipo.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**gestore di metadati**
</dt> <dd>

Questo termine viene talvolta usato per indicare il gestore della proprietà. Vedere la definizione di: gestore della proprietà.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**estensione dello spazio dei nomi**
</dt> <dd>

Vedere la definizione di: origine dati della shell.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Collegamento di oggetti e database di incorporamento (OLE DB)**
</dt> <dd>

Un set standard di interfacce che fornisce accesso eterogeneo a origini diverse di informazioni situate ovunque, ad esempio file System, cartelle di posta elettronica e database.

</dd> <dt>

**OLE DB**
</dt> <dd>

Vedere la definizione per: collegamento di oggetti e database di incorporamento.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**PerceivedType**
</dt> <dd>

Ampia categoria di tipi di formato di file. PerceivedType è stato introdotto in Windows XP e supporta un set limitato di tipi di file noti, ad esempio immagini, testo, audio e tipi di file compressi. I tipi di file, generalmente i tipi di file pubblici, possono anche avere un tipo percepito. Ad esempio, i tipi di file di immagine. bmp,. png,. jpg e. gif sono anche di tipo percepito, image. A livello di programmazione, PerceivedType viene espresso come numero intero. Poiché è presente codice che usa Kind e PerceivedType, i proprietari del formato di file devono registrarsi entrambi. Ad esempio, "Play All" dipende da PerceivedType. Vedere anche: tipo di file.

</dd> <dt>

**gestore di anteprime**
</dt> <dd>

Gestore che produce rapidamente una visualizzazione semplificata e di sola lettura dell'elemento della shell da visualizzare nel riquadro di anteprima di Esplora risorse.

</dd> <dt>

**Gestore proprietà**
</dt> <dd>

Gestore che converte i dati archiviati in un file in uno schema strutturato riconosciuto da e a cui è possibile accedere da Esplora risorse, da Windows Search e da altre applicazioni. Questi sistemi possono quindi interagire con il gestore delle proprietà per scrivere e leggere le proprietà da e verso il file. I dati tradotti includono la visualizzazione dettagli, infotip, il riquadro dettagli, le pagine delle proprietà e così via. Ogni gestore di proprietà è associato a un particolare tipo di file, identificato dall'estensione del nome file. Vedere anche: sistema di proprietà.

</dd> <dt>

**gestore della finestra delle proprietà**
</dt> <dd>

Gestore utilizzato per creare finestre delle proprietà personalizzate con le immagini e i controlli dell'interfaccia utente che consentono l'interazione personalizzata con un tipo di file.

</dd> <dt>

**sistema di proprietà**
</dt> <dd>

Sistema di lettura/scrittura estendibile di definizioni di dati che utilizza proprietà implementate come coppie nome-valore. Vedere anche: gestore della proprietà, elemento della shell.

</dd> <dt>

**valore proprietà**
</dt> <dd>

Valore associato a un nome di proprietà per un elemento della shell. Ad esempio, "Author", "size" e "date taked" sono proprietà. I valori delle proprietà vengono espressi come una struttura PROPVARIANT.

</dd> <dt>

**gestore di protocollo**
</dt> <dd>

Gestore che accede a origini contenuto e fornisce un oggetto IUrlAccessor per un protocollo e un URL specificati. I gestori di protocollo estendono la funzionalità di ricerca di Windows e possono fornire notifiche delle modifiche agli indicizzatori. Per indicizzare tipi specifici di archivi dati sono necessari gestori di protocollo diversi. Per garantire un'esperienza utente ragionevole, è necessario specificare anche un'origine dati della Shell per l'archivio dati, oltre a implementare il gestore di protocollo. Il gestore di protocollo espone gli elementi nell'archivio dati all'indicizzatore, mentre l'origine dati della shell espone gli elementi nell'archivio dati alla Shell.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**PIDL relativo**
</dt> <dd>

Un PIDL relativo a un oggetto radice nello spazio dei nomi della shell diverso dalla cartella desktop. Si tratta in genere della cartella padre dell'elemento.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Origine dati Shell**
</dt> <dd>

Componente utilizzato per estendere lo spazio dei nomi della shell ed esporre gli elementi in un archivio dati. In passato, l'origine dati della shell era denominata estensione dello spazio dei nomi della shell. Vedere anche: contenitore, gestore, elemento della shell.

</dd> <dt>

**Estensione della shell**
</dt> <dd>

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere definizione per: gestore tipo di file.

</dd> <dt>

**Gestore dell'estensione della shell**
</dt> <dd>

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere definizione per: gestore tipo di file.

</dd> <dt>

**Gestore Shell**
</dt> <dd>

Questo termine viene talvolta usato per indicare il gestore del tipo di file. Vedere definizione per: gestore tipo di file.

</dd> <dt>

**Elemento della shell**
</dt> <dd>

Una singola parte di contenuto. Alcuni elementi della shell sono origini di contenuto e altri no. Una cartella è un'origine di contenuto, ad esempio, ma non è presente un file con estensione jpg. I gestori di tipi di file espongono gli elementi della shell. In alcuni contesti "Item" viene usato per distinguere i contenitori da non contenitori. Vedere anche: contenitore, origine del contenuto, gestore del tipo di file.

</dd> <dt>

**Estensione dello spazio dei nomi shell**
</dt> <dd>

Questo termine viene talvolta usato per indicare l'origine dati della shell. Vedere la definizione di: origine dati della shell.

</dd> <dt>

**menu di scelta rapida**
</dt> <dd>

Interfaccia utente utilizzata per presentare una raccolta di verbi associati a un elemento dell'interfaccia utente, ad esempio un file o una cartella.

</dd> <dt>

**Gestore del menu di scelta rapida**
</dt> <dd>

Gestore che aggiunge verbi per un elemento o elementi. Questi verbi vengono in genere visualizzati in un menu di scelta rapida. Vedere anche: menu di scelta rapida.

</dd> <dt>

**PIDL semplice**
</dt> <dd>

PIDL analizzato senza verifica del disco.

</dd> <dt>

**verbo statico**
</dt> <dd>

Verbo che si applica a un elemento della shell senza che sia necessario controllare lo stato corrente di un elemento o di un sistema. Un verbo statico si basa su una registrazione statica degli elementi associati di un elemento e non cambia.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**gestore anteprime**
</dt> <dd>

Gestore che fornisce un'immagine statica per rappresentare un elemento della shell.

</dd> <dt>

**provider di anteprime**
</dt> <dd>

Questo termine viene talvolta usato per indicare il gestore di anteprime. Vedere la definizione per: gestore anteprime.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**nome descrittivo del tipo**
</dt> <dd>

Vedere la definizione per: Kind.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**verb**
</dt> <dd>

Singola azione che può essere chiamata da un elemento della shell. Gli esempi includono Open e Print. I verbi sono talvolta denominati comandi o attività. Vedere anche: verbo dinamico, gestore del menu di scelta rapida, verbo statico.

</dd> <dt>

**gestore di verbi**
</dt> <dd>

Questo termine viene talvolta usato per indicare il gestore dei menu di scelta rapida. Vedere definizione per: gestore del menu di scelta rapida.

</dd> </dl>

 

 



