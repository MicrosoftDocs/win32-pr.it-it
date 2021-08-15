---
title: Tipi di carattere di variabili OpenType
description: Questo argomento descrive i tipi di carattere delle variabili OpenType, il supporto in DirectWrite e Direct2D e come usarli nell'app. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c671bebce73cf3bdec42d1f7f570add914db7eb33b8a6bfd1b196d569b9975d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649394"
---
# <a name="opentype-variable-fonts"></a>Tipi di carattere di variabili OpenType

Questo argomento descrive i tipi di carattere delle variabili OpenType, il supporto in DirectWrite e Direct2D e come usarli nell'app. 

-   [Che cosa sono i tipi di carattere delle variabili OpenType?](#what-are-opentype-variable-fonts)
-   [Supporto dei tipi di carattere delle variabili OpenType in DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Uso dei tipi di carattere delle variabili OpenType](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>Che cosa sono i tipi di carattere delle variabili OpenType?

La versione 1.8 della specifica del formato del tipo di carattere [OpenType](https://www.microsoft.com/typography/otspec/) ha introdotto una nuova estensione per il formato noto come Variazioni del tipo [di carattere OpenType.](/typography/opentype/spec/otvaroverview) I tipi di carattere che usano queste estensioni sono noti come tipi di carattere variabili OpenType. Un tipo di carattere variabile OpenType è un singolo tipo di carattere che può comportarsi come diversi tipi di carattere usando l'interpolazione continua tra progettazioni diverse, tutte definite all'interno del singolo tipo di carattere.

Un tipo di carattere variabile OpenType può definire variazioni continue della progettazione lungo uno o più assi indipendenti, ad esempio spessore o larghezza: 

 

![Mostra un tipo di carattere variabile OpenType che usa la lettera "G" e mostra variazioni diverse lungo un asse di larghezza orizzontale e un asse di spessore verticale.](images/opentype-width-weight.png)

Uno sviluppatore di tipi di carattere determina un set di assi di variazione da usare in un determinato tipo di carattere. Questi assi possono includere un set di assi noti (o "registrati") di variazione, ad esempio peso e larghezza, ma possono anche includere assi arbitrari e personalizzati di variazione definiti dallo sviluppatore del tipo di carattere.  

Selezionando un set di assi di variazione per un tipo di carattere, lo sviluppatore del tipo di carattere definisce uno spazio astratto e ndimensionale di variazione di progettazione per il tipo di carattere. I motori di testo possono specificare potenzialmente qualsiasi posizione, o "istanza", all'interno di tale spazio continuo per il layout e il rendering del testo. 

Lo sviluppatore di tipi di carattere può anche selezionare e assegnare nomi a istanze specifiche all'interno dello spazio di progettazione-variazione; queste sono definite "istanze denominate". Ad esempio, un tipo di carattere con variazione di spessore può supportare variazioni continue tra tratti molto leggeri e molto pesanti, mentre lo sviluppatore del tipo di carattere ha selezionato pesi specifici lungo tale continuum e assegnato loro nomi, ad esempio "Light", "Regular" e "Semibold". 

Il formato del tipo di carattere della variabile OpenType usa tabelle di dati presenti nei tipi di carattere OpenType tradizionali e alcune tabelle aggiuntive che descrivono come cambiano i valori dei vari elementi di dati per istanze diverse. Il formato designa un'istanza di variante come "istanza predefinita", che usa le tabelle tradizionali per ottenere i valori predefiniti. Tutte le altre istanze dipendono dai dati predefiniti e da altri dati differenziali. Ad esempio, una tabella "glyf" può avere una descrizione della curva di Bézier di una forma nominale del glifo, ovvero la forma usata per l'istanza predefinita, mentre una tabella "gvar" descrive come i punti di controllo di Bezier per il glifo vengono regolati per altre istanze. Analogamente, altri valori del tipo di carattere possono avere un valore nominale più dati differenziali che descrivono come cambiano tali valori per istanze diverse. ad esempio, altezza x e altre metriche a livello di carattere o posizioni di ancoraggio del segno specifiche del glifo e regolazioni della crenatura. 

Poiché i tipi di carattere variabili possono supportare un set arbitrario di assi di variazione, richiedono un modello estendibile di famiglie di tipi di carattere che rifletta in modo più diretto il modo in cui i progettisti di tipi di carattere creano famiglie di tipi di carattere: una famiglia di caratteri è definita da un nome di famiglia e da determinate caratteristiche di progettazione costanti, con un numero arbitrario (determinato dallo sviluppatore di tipi di carattere) dei modi in cui la progettazione può variare. È possibile creare una famiglia di caratteri con varianti per il peso, ma una famiglia di caratteri diversa può essere creata con varianti per altezza x, dimensione serif, "perizia" o qualsiasi tipo di carattere desiderato dallo sviluppatore del tipo di carattere. In questo modello, una selezione del tipo di carattere è descritta meglio usando il nome della famiglia generale o "preferito" o "tipografico", più un set di coppie chiave-valore, ognuna delle quali rappresenta un tipo di variazione e un valore specifico, con i tipi di variazione in generale un set estendibile. Questa nozione generale di famiglia di caratteri può essere applicata ai tipi di carattere tradizionali non variabili, nonché ai tipi di carattere variabili. Ad esempio, in questo modello di famiglia tipografica generale, una famiglia "Selawik VF" potrebbe avere variazioni per peso, dimensioni ottiche e progettazione serif, con istanze come "Semilight Banner Sans". 

Alcune implementazioni software esistenti, incluse le API DirectWrite, possono essere progettate presupponendo un modello più limitato di famiglie di caratteri. Ad esempio, alcune applicazioni possono presupporre che una famiglia di caratteri possa avere al massimo varianti Regular, Bold, Italic e Bold Italic. Le interfacce [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) esistenti presuppongono un modello di famiglia weight/stretch/style ("WSS"), consentendo di impostare le varianti all'interno di una famiglia usando le enumerazioni [**DWRITE \_ FONT \_ WEIGHT,**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) [**DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) o [**DWRITE FONT \_ \_ STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) come parametri. Prendendo l'esempio precedente, le dimensioni ottiche e gli assi serif non verrebbero considerati come assi interni della famiglia di variazione nel modello WSS. 

Il supporto completo per i tipi di carattere variabili richiederebbe API che consentono di definire un membro della famiglia con potenzialmente diversi parametri, come determinato dal tipo di carattere. Le progettazioni api esistenti possono tuttavia essere in grado di fornire supporto parziale per i tipi di carattere variabili proiettando le istanze denominate definite in un tipo di carattere variabile nei modelli di famiglia di caratteri più limitati. Nell'esempio precedente, "Selawik VF Semilight Banner Sans" può essere proiettato nel modello WSS come famiglia "Selawik VF Banner Sans" con "Semilight" come variante di peso. 

Per un altro esempio, si consideri una famiglia di caratteri tipografici, ad esempio Sitka, con varianti di peso e dimensioni ottiche. Le varianti denominate all'interno della famiglia includono Sitka Text Regular e Sitka Banner Bold (oltre a molte altre). Il nome della famiglia tipografica è "Sitka", mentre i nomi dei visi per queste varianti nel modello di famiglia tipografica sono "Text Regular" e "Banner Bold". I modelli a quattro membri e WSS famiglia non consentono varianti di dimensioni ottiche all'interno di una famiglia e pertanto le distinzioni di dimensioni ottiche devono essere trattate come distinzioni a livello di famiglia. La tabella seguente illustra come una selezione di tipi di carattere della famiglia tipografica Sitka verrà trattata nel modello WSS famiglia di caratteri: 



Modello di famiglia tipografica

WSS modello di famiglia

Famiglia

Viso

Famiglia

Viso

Sitka

Testo normale

Testo Sitka

Normale

Sitka

Banner in grassetto

Sitka Banner

Bold

Sitka

Didascalia corsiva

Didascalia Sitka

Corsivo



 

La proiezione dei nomi da un modello di famiglia tipografica al modello WSS family può essere applicata ai tipi di carattere non variabili e alle istanze denominate dei tipi di carattere variabili. Questa operazione non può essere eseguita, tuttavia, per altre istanze non denominate dello spazio di progettazione continuo di un tipo di carattere variabile. Per questo motivo, il supporto per la funzionalità completa dei tipi di carattere variabili richiederà API progettate per fare riferimento ai visi all'interno di una famiglia tipografica in termini di un set non vincolato di assi di variazione e valori dell'asse. 

## <a name="opentype-variable-font-support-in-directwrite"></a>Supporto dei tipi di carattere delle variabili OpenType in DirectWrite

Al momento del rilascio del Windows 10 Creators Update, il formato del carattere della variabile OpenType è ancora molto nuovo e i fornitori di tipi di carattere, le piattaforme e le app sono ancora in corso di implementazione del nuovo formato. Questo aggiornamento fornisce l'implementazione iniziale per questo formato in DirectWrite. 

DirectWrite gli interni sono stati aggiornati per supportare i tipi di carattere delle variabili OpenType. Usando le API correnti, fornisce il supporto per tutte le istanze denominate di un tipo di carattere variabile. Questo supporto può essere usato per flussi di lavoro completi, dall'enumerazione delle istanze denominate, alla selezione di un'istanza denominata, all'uso nel layout e nel data shaping, al rendering e alla stampa. A vantaggio delle app che usano anche l'interoperabilità di testo GDI per determinate operazioni, è stato aggiunto un supporto simile anche nelle API GDI esistenti. 

Nell'Windows 10 Creators Update non DirectWrite istanze arbitrarie che utilizzano la funzionalità di variazione continua dei tipi di carattere variabili.

In molte operazioni, il comportamento in DirectWrite di istanze denominate di un tipo di carattere variabile non può essere distinto dal comportamento dei tipi di carattere non variabili. Poiché il supporto viene fornito usando le API DirectWrite esistenti, le istanze denominate dei tipi di carattere variabili possono funzionare anche in molte app DirectWrite esistenti senza modifiche. Le eccezioni possono tuttavia essere applicate in determinate situazioni:  

-   Se un'app elabora i dati dei tipi di carattere direttamente per determinate operazioni. Ad esempio, se un'app legge i dati della struttura del glifo direttamente dal file del tipo di carattere per creare determinati effetti visivi.
-   Se un'app usa una libreria di terze parti per determinate operazioni. Ad esempio, se un'app usa DirectWrite per il layout, per ottenere gli indici e le posizioni finali dei glifi, ma quindi usa una libreria di terze parti per il rendering.
-   Se un'app incorpora i dati del tipo di carattere in un documento o in altro modo passa i dati del tipo di carattere a un processo downstream.

Se le operazioni vengono eseguite usando implementazioni che non supportano tipi di carattere variabili, è possibile che queste operazioni non producano i risultati previsti. Ad esempio, le posizioni dei glifi possono essere calcolate per un'istanza denominata del tipo di carattere variabile, ma il rendering dei glifi può essere eseguito presupponendo un'istanza denominata diversa. A seconda dell'implementazione dell'applicazione, i risultati possono funzionare in alcuni contesti, ma non in altri contesti in cui è possibile usare altre librerie. Ad esempio, il testo può essere visualizzato correttamente sullo schermo, ma non quando viene stampato. Se i flussi di lavoro end-to-end vengono implementati usando solo DirectWrite, è possibile che sia previsto un comportamento corretto per le istanze denominate di un tipo di carattere variabile. 

Poiché le API DirectWrite esistenti supportano la selezione dei visi usando il modello weight/stretch/style, le istanze denominate dei tipi di carattere che usano altri assi di variazione verranno proiettate dal modello generale della famiglia tipografica nel modello WSS, come descritto in precedenza. Questo si basa su un tipo di carattere variabile che include una tabella "attributi di stile" ('STAT') con sottotable dei valori dell'asse, che DWrite usa per distinguere i token del nome del viso che designano gli attributi di spessore, estensione o stile dai token che riguardano altri assi di variazione.  

Se un tipo di carattere variabile non include una tabella "STAT", come richiesto per i tipi di carattere variabili dalla specifica OpenType, DirectWrite considera il tipo di carattere come un tipo di carattere non variabile contenente solo l'istanza predefinita.  

Se un tipo di carattere contiene una tabella "STAT" ma non include le sottotable appropriate per i valori dell'asse, ciò può causare risultati imprevisti, ad esempio la presenza di più visi con nomi di visi identici. Tali tipi di carattere non sono attualmente supportati. 

La specifica OpenType consente di rappresentare i dati della struttura del glifo in uno dei due formati seguenti: usando una tabella "glif", che usa il formato di struttura e hint TrueType, o una tabella "CFF", che usa la rappresentazione CFF (Compact Font Format). In un tipo di carattere variabile con strutture TrueType, la tabella 'glyf' continua a essere usata ed è integrata con una tabella "gvar" che fornisce i dati di variazione per le strutture. Ciò significa che l'istanza predefinita di un tipo di carattere variabile con strutture TrueType usa solo le tabelle OpenType tradizionali che saranno supportate nel software meno recente che non supporta tipi di carattere variabili. In un tipo di carattere variabile con strutture CFF, tuttavia, la tabella 'CFF' viene sostituita dalla tabella 'CFF2', che incapsula i dati di struttura predefiniti e i dati di variazione associati in una tabella. I dati CFF vengono elaborati da un rasterizzatore separato da quello usato per i dati TrueType e una tabella 'CFF2' richiede un rasterizzatore CFF aggiornato con supporto 'CFF2'. Una tabella 'CFF2' non può essere elaborata dai rasterizzatori CFF meno recenti. Per un tipo di carattere variabile con dati di struttura CFF, ciò significa che anche l'istanza predefinita non funzionerà nel software meno recente. 

Nell'Windows 10 Creators Update non DirectWrite tipi di carattere variabili con dati di struttura CFF usando la tabella 'CFF2'. 

## <a name="using-opentype-variable-fonts"></a>Uso dei tipi di carattere delle variabili OpenType

I tipi di carattere delle variabili OpenType possono essere facili da usare, tenendo presenti le limitazioni correnti indicate in precedenza: 

-   Al momento sono supportate solo le istanze denominate di un tipo di carattere variabile.
-   Al momento sono supportati solo i tipi di carattere variabili che usano i dati di struttura del glifo TrueType (non le strutture CFF). 
-   Per i tipi di carattere che usano assi di variazione di progettazione diversi da peso, estensione o stile, le istanze denominate verranno proiettate nel modello di famiglia di WSS, il che potrebbe comportare la visualizzazione di alcune istanze denominate come famiglie separate (come accadeva in passato per i tipi di carattere non variabili). Per supportare questo tipo di carattere, i tipi di carattere variabili devono avere una tabella "STAT" che include le tabelle secondarie asse-valore appropriate.
-   Le istanze denominate dei tipi di carattere variabili sono supportate nelle API DirectWrite, ma se determinate operazioni vengono eseguite in implementazioni precedenti che non supportano tipi di carattere variabili, è possibile che tali operazioni producano risultati non corretti. 
-   Alcune DIRECTWRITE usano le enumerazioni [**DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), [**DWRITE FONT \_ \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) e [**DWRITE FONT \_ \_ STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) per specificare gli attributi weight, stretch e style quando si selezionano i visi. Se un tipo di carattere variabile usa assi di variazione corrispondenti ma ha molte istanze denominate che richiedono una granularità più fine, non tutte le istanze denominate saranno selezionabili in tali API.

I tipi di carattere delle variabili OpenType conformi a questi requisiti possono essere installati dalla shell di Windows come altri tipi di carattere OpenType e possono essere usati anche in set di tipi di carattere personalizzati creati da un'app.  

Quando vengono installate nel sistema, tutte le istanze denominate di un tipo di carattere variabile verranno incluse nel set di tipi di carattere restituito chiamando il metodo IDWriteFontFamily3::[**GetSystemFontSet.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) Si noti che un set di caratteri è un elenco semplice senza una gerarchia di raggruppamento della famiglia, ma ogni elemento del set ha una proprietà family-name basata sul modello WSS family. Il set di caratteri può essere filtrato per una particolare istanza denominata variable-font usando i metodi [**IDWriteFontSet::GetMatchingFonts.**](idwritefontset-getmatchingfonts-overload.md) Se si usa l'overload **GetMatchingFonts** che accetta un familyName, tuttavia, il familyName specificato deve usare il nome conforme WSS modello della famiglia di caratteri. L'elenco completo dei nomi di famiglia compatibili con WSS che si verificano in un set di tipi di carattere può essere ottenuto usando i metodi [**IDWriteFontSet::GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) usando DWRITE \_ FONT PROPERTY ID FAMILY \_ \_ \_ \_ NAME.  

Analogamente, tutte le istanze denominate di un tipo di carattere variabile verranno rappresentate nella raccolta di tipi di carattere restituita dal metodo IDWriteFactory::[**GetSystemFontCollection.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) Poiché gli elementi di una raccolta di tipi di carattere sono famiglie di caratteri basate sul modello WSS, le istanze denominate di un tipo di carattere variabile possono essere rappresentate in una raccolta come membri di due o più famiglie di tipi di carattere. Se viene usato il metodo [**IDWriteFontCollection::FindFamilyName,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) il parametro familyName deve essere un nome di famiglia WSS compatibile con l'utente. Per trovare tutti i nomi di famiglia compatibili con WSS da una raccolta di tipi di carattere, un'app può scorrere in ciclo ogni famiglia e chiamare [**IDWriteFontFamily::GetFamilyNames,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames)anche se potrebbe essere più semplice ottenere un set di caratteri corrispondente e usare il [**metodo GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) come descritto in precedenza. 

Quando si lavora con tipi di carattere personalizzati, è possibile usare diversi approcci descritti nell'argomento [Set](custom-font-sets-win10.md) di caratteri personalizzati per creare un set di tipi di carattere. Per aggiungere un tipo di carattere variabile a un set di tipi di carattere personalizzato, è consigliabile utilizzare il metodo [**IDWriteFontSetBuilder1::AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) perché supporta tipi di carattere variabili e aggiungerà tutte le istanze denominate di un tipo di carattere variabile in una singola chiamata. Al momento non è possibile aggiungere singole istanze denominate di un tipo di carattere variabile personalizzato a un set di tipi di carattere usando i metodi [**IDWriteFontSetBuilder::AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) perché non è possibile creare un riferimento al tipo di carattere che specifica quale delle istanze denominate da un file di tipo di carattere variabile è destinato. Ciò significa che attualmente non è possibile aggiungere istanze denominate di un tipo di carattere personalizzato a un set di tipi di carattere personalizzato con proprietà personalizzate assegnate. Ciò significa che attualmente i tipi di carattere variabili personalizzati non possono essere usati facilmente in combinazione con le API DirectWrite per i tipi di carattere remoti. Se le istanze denominate di un tipo di carattere variabile sono incluse in un set di tipi di carattere di sistema, tuttavia, i riferimenti al tipo di carattere per ogni istanza denominata esistono già e possono essere aggiunti a set di tipi di carattere personalizzati, anche con l'uso di valori di proprietà personalizzati. Per altri dettagli, vedere l'argomento Set di caratteri personalizzati. 

Quando si lavora con tipi di carattere variabili, le enumerazioni [**DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) e [**DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) di DirectWrite sono strettamente connesse agli assi di variazione di spessore e larghezza definiti nella specifica OpenType, ma non sono uguali. In primo luogo, la scala numerica per qualsiasi asse di variazione supporta sempre valori frazionari, mentre fontWeight e fontStretch usano numeri interi. La scala dell'asse del peso OpenType usa valori compresi tra 1 e 1000, supportati anche da fontWeight. Pertanto, la modifica da un valore dell'asse del peso della variazione a fontWeight è relativamente minore: il fontWeight segnalato per un'istanza denominata può essere arrotondato dal valore preciso usato per definire l'istanza denominata all'interno del tipo di carattere. La distinzione tra DirectWrite fontStretch e la scala dell'asse di larghezza OpenType è maggiore: DirectWrite usa valori compresi tra 1 e 9, seguendo i valori [usWidthClass](/typography/opentype/spec/os2#uswidthclass) della tabella OpenType OS/2, mentre la scala dell'asse di larghezza OpenType usa valori positivi che rappresentano una percentuale di larghezza normale. La [documentazione usWidthClass](/typography/opentype/spec/os2#uswidthclass) nella specifica OpenType fornisce un mapping tra i valori da 1 a 9 e la percentuale dei valori normali. Il valore fontStretch segnalato per un'istanza denominata può comportare l'arrotondamento durante la conversione da valori dell'asse di larghezza. 

Quando si crea [**un oggetto IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)è necessario specificare una raccolta di tipi di carattere e WSS proprietà del carattere compatibili con WSS (nome della famiglia, spessore, estensione e stile). Ciò si applica anche quando si impostano le proprietà di formattazione dei caratteri in un intervallo di [**testo IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Le proprietà possono essere ottenute da un [**oggetto IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) o da [**oggetti IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) che rappresentano una particolare istanza denominata. Come osservato in precedenza, i valori restituiti dai metodi GetWeight e GetStretch possono essere approssimazioni arrotondate per i valori effettivi dell'asse usati per definire l'istanza denominata, ma DirectWrite esegue il mapping della combinazione di proprietà all'istanza denominata desiderata. 

Analogamente, se un'app usa [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) per creare dati di fallback dei tipi di carattere personalizzati, le famiglie vengono specificate per i mapping di intervalli di caratteri usando nomi di famiglia WSS compatibili con l'utente. Il fallback dei caratteri all'interno di DirectWrite si basa sulle famiglie con DirectWrite una variante all'interno di una famiglia di fallback che corrisponde più vicina alla variante della famiglia iniziale. Per le varianti che coinvolgono dimensioni diverse da peso, estensione e stile, DirectWrite attualmente non sarebbe in grado di selezionare tali varianti all'interno di una famiglia di fallback, a meno che non siano stati creati dati di fallback personalizzati specificamente per fornire mapping di fallback per le famiglie con particolari attributi non WSS, ad esempio varianti di dimensioni ottiche "Didascalia".

 

 