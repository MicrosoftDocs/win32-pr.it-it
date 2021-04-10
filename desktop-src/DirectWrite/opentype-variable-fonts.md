---
title: Tipi di carattere di variabili OpenType
description: Questo argomento descrive i tipi di carattere delle variabili OpenType, il relativo supporto in DirectWrite e Direct2D e come usarli nell'app. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a9e6bdf27da0d70841973515636736859294dd
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "103885902"
---
# <a name="opentype-variable-fonts"></a>Tipi di carattere di variabili OpenType

Questo argomento descrive i tipi di carattere delle variabili OpenType, il relativo supporto in DirectWrite e Direct2D e come usarli nell'app. 

-   [Che cosa sono i tipi di carattere variabili OpenType?](#what-are-opentype-variable-fonts)
-   [Supporto dei tipi di carattere variabili OpenType in DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Utilizzo di tipi di carattere variabili OpenType](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>Che cosa sono i tipi di carattere variabili OpenType?

La versione 1,8 della [specifica del formato del tipo di carattere OpenType](https://www.microsoft.com/typography/otspec/) ha introdotto una nuova estensione nel formato noto come [variazioni dei tipi di carattere OpenType](/typography/opentype/spec/otvaroverview). I tipi di carattere che usano queste estensioni sono noti come tipi di carattere variabili OpenType. Un tipo di carattere variabile OpenType è un singolo tipo di carattere che può comportarsi come più tipi di carattere usando l'interpolazione continua tra diverse progettazioni, tutte definite all'interno del singolo tipo di carattere.

Un tipo di carattere della variabile OpenType può definire una variazione continua della progettazione lungo uno o più assi indipendenti, ad esempio il peso o la larghezza: 

 

![Mostra un tipo di carattere della variabile OpenType che usa la lettera "G" e mostra variazioni diverse lungo un asse della larghezza orizzontale e un asse di ponderazione verticale.](images/opentype-width-weight.png)

Uno sviluppatore di tipi di carattere determina un set di assi di variazione da usare in un tipo di carattere specificato. Questi assi possono includere un set di assi noti (o "registrati") di variazione, ad esempio il peso e la larghezza, ma possono includere anche assi arbitrari e personalizzati di variazione definiti dallo sviluppatore del tipo di carattere.  

Selezionando un set di assi di variazione per un tipo di carattere, lo sviluppatore del tipo di carattere definisce uno spazio astratto e n-dimensionale della variazione di progettazione per il tipo di carattere. I motori di testo possono specificare potenzialmente qualsiasi posizione, o "istanza", nello spazio continuo per il layout e il rendering del testo. 

Lo sviluppatore di tipi di carattere può inoltre selezionare e assegnare nomi a istanze specifiche all'interno dello spazio di variazione della progettazione. questi vengono definiti "istanze denominate". Ad esempio, un tipo di carattere con variazione del peso può supportare una variazione continua tra tratti molto leggeri e molto pesanti, mentre lo sviluppatore del tipo di carattere ha selezionato pesi specifici lungo tale continuum e assegna loro nomi, ad esempio "Light", "regular" e "SemiBold". 

Il formato del tipo di carattere della variabile OpenType utilizza tabelle di dati presenti nei tipi di carattere OpenType tradizionali, oltre ad alcune tabelle aggiuntive in cui viene descritto il modo in cui i valori dei vari elementi di dati cambiano per istanze Il formato definisce un'istanza di variazione come "istanza predefinita", che usa le tabelle tradizionali per ottenere i valori predefiniti. Tutte le altre istanze dipendono dai dati predefiniti e da altri dati Delta. Una tabella ' glyf ', ad esempio, può avere una descrizione della curva di Bezier di una forma di glifo nominale, ovvero la forma utilizzata per l'istanza predefinita, mentre una tabella ' GVAR ' descrive il modo in cui i punti di controllo di Bezier per il glifo vengono modificati per le altre istanze. Analogamente, altri valori del tipo di carattere possono avere un valore nominale più dati Delta che descrivono il modo in cui tali valori cambiano per le diverse istanze. ad esempio, altezza x e altre metriche a livello di carattere o posizioni di ancoraggio contrassegno specifiche del glifo e regolazioni della crenatura. 

Poiché i tipi di carattere variabili possono supportare un set arbitrario di assi di variazione, richiedono un modello estendibile di famiglie di caratteri che rispecchi più direttamente il modo in cui le finestre di progettazione dei tipi di carattere creano famiglie di tipi di carattere: una famiglia di caratteri è definita da un nome di famiglia e determinate caratteristiche di progettazione costanti, con un numero arbitrario (determinato dallo sviluppatore del tipo di carattere È possibile creare una famiglia di caratteri con varianti per il peso, ma è possibile creare una famiglia di caratteri diversa con varianti per x-height, serif-size, "funky" o qualsiasi altro tipo di carattere per lo sviluppatore. In questo modello, una selezione del tipo di carattere è meglio descritta utilizzando il nome generale, o "preferito" o "tipografico", oltre a un set di coppie chiave-valore, ognuna delle quali rappresenta un tipo di variazione e un valore specifico, con i tipi di variazione in generale un set estendibile. Questa nozione generale di una famiglia di caratteri può essere applicata a tipi di carattere tradizionali, non variabili e a tipi di carattere variabili. Ad esempio, in questo modello di famiglia tipografico generale, una famiglia "Selawik VF" potrebbe avere varianti per il peso, la dimensione ottica e la progettazione serif, con istanze quali "SemiLight banner San". 

Alcune implementazioni software esistenti, tuttavia, incluse le API DirectWrite esistenti, possono essere progettate presumendo un modello più limitato di famiglie di caratteri. Alcune applicazioni, ad esempio, possono presumere che una famiglia di caratteri possa avere varianti in corsivo, al massimo, normali, grassetto, corsivo e grassetto. Le interfacce [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) esistenti presuppongono un modello famiglia di peso/estensione/stile ("WSS"), che consente di specificare le varianti all'interno di una famiglia usando il [**\_ tipo di carattere DWrite \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), l' [**\_ \_ estensione del tipo di carattere DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) o le enumerazioni [**\_ \_ dello stile del tipo di carattere DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) come parametri. Prendendo l'esempio precedente, gli assi delle dimensioni ottiche e Serif non verrebbero considerati come assi interni della famiglia di variazione nel modello WSS. 

Il supporto completo per i tipi di carattere variabili richiederebbe API che consentono di specificare un membro della famiglia con potenzialmente diversi parametri, come determinato dal tipo di carattere. Tuttavia, le progettazioni API esistenti potrebbero essere in grado di fornire supporto parziale per i tipi di carattere variabili proiettando le istanze denominate definite in un tipo di carattere variabile in modelli di famiglia di caratteri più limitati. Nell'esempio precedente, "Selawik VF Semilight banner San" potrebbe essere proiettato nel modello WSS come famiglia "Selawik VF banner sans" con "SemiLight" come variante di peso. 

Per un altro esempio, si consideri una famiglia di caratteri tipografici, ad esempio Sitka, con varianti di peso e dimensioni ottiche. Le varianti denominate all'interno della famiglia includono il testo di Sitka Regular e Sitka Banner Bold (più numerosi altri). Il nome della famiglia tipografica è "Sitka", mentre i nomi di tali varianti nel modello di famiglia tipografico sono "text regular" e "Banner Bold". I modelli di famiglia a quattro membri e WSS non consentono le varianti di dimensioni ottiche all'interno di una famiglia, quindi le distinzioni di dimensione ottica devono essere considerate come le distinzioni a livello di famiglia. Nella tabella seguente viene illustrato il modo in cui una selezione di tipi di carattere del gruppo tipografico Sitka verrebbe considerata nel modello di famiglia WSS: 



Modello di famiglia tipografico

Modello di famiglia WSS

Famiglia

Viso

Famiglia

Viso

Sitka

Testo normale

Testo Sitka

Regular

Sitka

Banner in grassetto

Banner Sitka

Grassetto

Sitka

Didascalia corsivo

Didascalia Sitka

Corsivo



 

La proiezione di nomi da un modello di famiglia tipografico al modello di famiglia WSS può essere applicata a tipi di carattere non variabili e alle istanze denominate di tipi di carattere variabili. Questa operazione non può essere eseguita, tuttavia, per altre istanze non denominate dello spazio di variazione della progettazione continua di un tipo di carattere variabile. Per questo motivo, il supporto per la funzionalità completa dei tipi di carattere variabili richiederà API progettate per fare riferimento ai visi all'interno di una famiglia tipografica in termini di un set non vincolato di assi di variazione e valori dell'asse. 

## <a name="opentype-variable-font-support-in-directwrite"></a>Supporto dei tipi di carattere variabili OpenType in DirectWrite

Al momento del rilascio di Windows 10 Creators Update, il formato del tipo di carattere della variabile OpenType è ancora molto nuovo e i fornitori di tipi di carattere, le piattaforme e le app sono ancora in fase di implementazione del nuovo formato. Questo aggiornamento fornisce l'implementazione iniziale per questo formato in DirectWrite. 

Gli elementi interni di DirectWrite sono stati aggiornati per supportare tipi di carattere variabili OpenType. Utilizzando le API correnti, fornisce il supporto per tutte le istanze denominate di un tipo di carattere variabile. Questo supporto può essere usato per flussi di lavoro completi, dall'enumerazione delle istanze denominate, dalla selezione di un'istanza denominata, da usare nel layout e nel data shaping per il rendering e la stampa. Per il vantaggio delle app che usano anche l'interoperabilità del testo GDI per determinate operazioni, è stato aggiunto anche un supporto simile nelle API GDI esistenti. 

In Windows 10 Creators Update, DirectWrite non supporta istanze arbitrarie che utilizzano la funzionalità di variazione continua dei tipi di carattere variabili.

In molte operazioni, il comportamento in DirectWrite di istanze denominate di un tipo di carattere variabile non può essere distinto dal comportamento dei tipi di carattere non variabili. Poiché il supporto viene fornito usando le API DirectWrite esistenti, le istanze denominate dei tipi di carattere variabili possono anche funzionare in molte app DirectWrite esistenti senza apportare modifiche. Tuttavia, le eccezioni possono essere applicate in determinate situazioni:  

-   Se un'app elabora direttamente i dati del tipo di carattere per determinate operazioni. Ad esempio, se un'app legge i dati del contorno del glifo direttamente dal file del tipo di carattere per creare determinati effetti visivi.
-   Se un'app usa una libreria di terze parti per determinate operazioni. Se ad esempio un'app usa DirectWrite per il layout, per ottenere gli indici e le posizioni del glifo finale, ma usa una libreria di terze parti per il rendering.
-   Se un'app incorpora i dati del tipo di carattere in un documento o in altro modo passa i dati del tipo di carattere a un processo downstream.

Se le operazioni vengono eseguite utilizzando implementazioni che non supportano i tipi di carattere variabili, è possibile che tali operazioni non producano i risultati previsti. È possibile, ad esempio, calcolare le posizioni del glifo per un'istanza denominata del tipo di carattere della variabile, ma è possibile che venga eseguito il rendering dei glifi presumendo una diversa istanza denominata. A seconda dell'implementazione dell'applicazione, i risultati possono funzionare in alcuni contesti, ma non in altri contesti in cui è possibile usare altre librerie. Ad esempio, il testo può essere visualizzato correttamente sullo schermo, ma non quando viene stampato. Se i flussi di lavoro end-to-end vengono implementati usando solo DirectWrite, è possibile prevedere un comportamento corretto per le istanze denominate di un tipo di carattere variabile. 

Poiché le API DirectWrite esistenti supportano la selezione dei volti usando il modello di spessore/estensione/stile, le istanze denominate dei tipi di carattere che usano altri assi di variazione verranno proiettate dal modello di famiglia tipografico generale nel modello WSS, come descritto in precedenza. Si basa su un tipo di carattere variabile, inclusa una tabella "attributi di stile" ("STAT") con sottotabelle con valori di asse, che DWrite utilizza per distinguere i token del nome del volto che definiscono gli attributi di peso, estensione o stile dai token che riguardano altri assi di variazione.  

Se un tipo di carattere della variabile non include una tabella ' STAT ', come richiesto per i tipi di carattere variabili per la specifica OpenType, DirectWrite considererà il tipo di carattere come un tipo di carattere non variabile contenente solo l'istanza predefinita.  

Se un tipo di carattere contiene una tabella ' STAT ', ma non include sottotabelle appropriate per i valori di asse, è possibile che si verifichino risultati imprevisti, ad esempio la presenza di più visi con nomi di faccia identici. Questi tipi di carattere non sono supportati in questo momento. 

La specifica OpenType consente di rappresentare i dati della struttura del glifo in uno dei due formati seguenti: usando una tabella ' glyf ', che usa il formato di contorno e hint di TrueType, o usando una tabella ' CFF ', che usa la rappresentazione Compact Font Format ("CFF"). In un tipo di carattere variabile con strutture TrueType la tabella ' glyf ' continua a essere utilizzata ed è integrata con una tabella ' GVAR ' che fornisce i dati di variazione per le strutture. Ciò significa che l'istanza predefinita di un tipo di carattere variabile con le strutture TrueType utilizza solo le tabelle OpenType tradizionali che saranno supportate nel software precedente senza supporto per i tipi di carattere variabili. In un tipo di carattere variabile con le strutture CFF, tuttavia, la tabella ' CFF ' viene sostituita dalla tabella ' CFF2', che incapsula i dati di struttura predefiniti e i dati di variazione associati in una tabella. I dati CFF vengono elaborati da un rasterizzatore separato da quello usato per i dati TrueType e una tabella ' CFF2' richiede un rasterizzatore CFF aggiornato con supporto ' CFF2'. Una tabella ' CFF2' non può essere elaborata da rasterizzatori CFF precedenti. Per un tipo di carattere variabile con i dati della struttura CFF, ciò significa che anche l'istanza predefinita non funzionerà nel software meno recente. 

In Windows 10 Creators Update, DirectWrite non supporta i tipi di carattere variabili con i dati della struttura CFF usando la tabella ' CFF2'. 

## <a name="using-opentype-variable-fonts"></a>Utilizzo di tipi di carattere variabili OpenType

I tipi di carattere di variabili OpenType possono essere facili da usare, tenendo presenti le limitazioni correnti indicate sopra: 

-   Al momento sono supportate solo le istanze denominate di un tipo di carattere variabile.
-   Al momento sono supportati solo i tipi di carattere variabili che usano i dati della struttura del glifo TrueType (non le strutture CFF). 
-   Per i tipi di carattere che usano gli assi della variante di progettazione diversa dal peso, dall'estensione o dallo stile, le istanze denominate verranno proiettate nel modello di famiglia WSS, che può comportare la visualizzazione di alcune istanze denominate come famiglie separate (come avviene nel passato per i tipi di carattere non variabili). Per supportare questa operazione, i tipi di carattere delle variabili devono contenere una tabella ' STAT ' che include le sottotabelle appropriate per il valore dell'asse.
-   Le istanze denominate di tipi di carattere variabili sono supportate nelle API DirectWrite, ma se determinate operazioni vengono eseguite nelle implementazioni precedenti che non supportano i tipi di carattere variabili, possono produrre risultati non corretti. 
-   Alcune API DirectWrite utilizzano le enumerazioni del tipo di carattere [**DWrite \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), DWrite e DWrite per specificare gli attributi di spessore, adattamento e stile quando si selezionano i visi. [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) Se un tipo di carattere variabile utilizza gli assi di variazione corrispondenti ma dispone di molte istanze denominate che richiedono una granularità più fine, non tutte le istanze denominate saranno selezionabili in tali API.

I tipi di carattere di variabili OpenType conformi a questi requisiti possono essere installati dalla shell di Windows esattamente come altri tipi di carattere OpenType e possono essere usati anche nei set di caratteri personalizzati creati da un'app.  

Quando viene installato nel sistema, tutte le istanze denominate di un tipo di carattere variabile verranno incluse nel set di caratteri restituito chiamando il metodo IDWriteFontFamily3::[**GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) . Si noti che un set di caratteri è un elenco semplice senza una gerarchia di raggruppamento delle famiglie, ma ogni elemento del set ha una proprietà nome famiglia basata sul modello di famiglia WSS. Il set di caratteri può essere filtrato per un'istanza specifica del tipo di carattere, usando i metodi [**IDWriteFontSet:: GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) . Se si usa l'overload di **GetMatchingFonts** che accetta un familyName, tuttavia, il nome di famiglia specificato deve usare il nome conforme al modello di famiglia di caratteri WSS. L'elenco completo dei nomi di famiglia compatibili con WSS che si verificano in un set di caratteri può essere ottenuto usando i metodi [**IDWriteFontSet:: GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) usando il \_ nome della famiglia di caratteri \_ ID della proprietà DWrite \_ \_ \_ .  

Analogamente, tutte le istanze denominate di un tipo di carattere variabile verranno rappresentate nella raccolta di tipi di carattere restituita dal metodo IDWriteFactory archiviata nei::[**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Poiché gli elementi di una raccolta di tipi di carattere sono gruppi di caratteri basati sul modello WSS, le istanze denominate di un tipo di carattere variabile possono essere rappresentate in una raccolta come membri di due o più famiglie di caratteri. Se viene usato il metodo [**IDWriteFontCollection:: FindFamilyName**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) , il parametro familyName deve essere un nome di famiglia compatibile con WSS. Per trovare tutti i nomi di famiglia compatibili con WSS da una raccolta di tipi di carattere, un'app può scorrere in ciclo ogni famiglia e chiamare [**IDWriteFontFamily:: GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames), anche se può essere più semplice ottenere un set di caratteri corrispondente e usare il metodo [**GetPropertyValues**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) come descritto in precedenza. 

Quando si utilizzano tipi di carattere personalizzati, è possibile utilizzare diversi approcci descritti nell'argomento [set di caratteri personalizzati](custom-font-sets-win10.md) per creare un set di caratteri. Per aggiungere un tipo di carattere variabile a un set di caratteri personalizzato, è consigliabile usare il metodo [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) perché supporta i tipi di carattere variabili e aggiunge tutte le istanze denominate di un tipo di carattere variabile in una singola chiamata. Al momento non esiste alcun modo per aggiungere singole istanze denominate di un tipo di carattere della variabile personalizzata a un set di caratteri usando i metodi [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) , poiché non esiste alcun modo per creare un riferimento a un tipo di carattere che specifichi le istanze denominate da un file di tipo di carattere variabile. Ciò significa che attualmente non è possibile aggiungere istanze denominate di un tipo di carattere personalizzato a un set di caratteri personalizzato con proprietà personalizzate assegnate. Ciò significa a sua volta che i tipi di carattere di variabili personalizzate attualmente non possono essere facilmente usati insieme alle API DirectWrite per i tipi di carattere remoti. Se le istanze denominate di un tipo di carattere variabile sono incluse in un set di caratteri di sistema, tuttavia, i riferimenti del tipo di carattere per ogni istanza denominata saranno già esistenti e potranno essere aggiunti a set di caratteri personalizzati, incluso l'utilizzo di valori di proprietà personalizzati. Per ulteriori informazioni, vedere l'argomento set di caratteri personalizzati. 

Quando si utilizzano tipi di carattere variabili, le enumerazioni di [**\_ \_ estensione**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) del tipo di carattere DirectWrite [**DWrite \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) e DWrite sono strettamente connesse agli assi di variazione di spessore e peso definiti nella specifica OpenType, ma non sono uguali. In primo luogo, la scala numerica per qualsiasi asse delle varianti supporta sempre i valori frazionari, mentre fontWeight e fontStretch utilizzano numeri interi. La scala dell'asse del peso OpenType usa valori compresi tra 1 e 1000, anch ' essi supportati da fontWeight. Quindi, la modifica da un valore dell'asse del peso variazione a fontWeight è relativamente secondaria: il fontWeight segnalato per un'istanza denominata può essere arrotondato a partire dal valore preciso usato per definire l'istanza denominata all'interno del tipo di carattere. La distinzione tra DirectWrite fontStretch e la scala dell'asse della larghezza OpenType è maggiore: DirectWrite usa i valori da 1 a 9, dopo i valori [usWidthClass](/typography/opentype/spec/os2#uswidthclass) della tabella OS/2 OpenType, mentre la scala dell'asse della larghezza OpenType usa valori positivi che rappresentano una percentuale della larghezza normale. La documentazione di [usWidthClass](/typography/opentype/spec/os2#uswidthclass) nella specifica OpenType fornisce un mapping tra i valori da 1 a 9 e i valori percentuali di normali. Il valore di fontStretch restituito per un'istanza denominata può comportare l'arrotondamento durante la conversione dai valori dell'asse della larghezza. 

Quando si crea un [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), è necessario specificare una raccolta di tipi di carattere e le proprietà dei tipi di carattere compatibili con WSS (nome della famiglia, peso, estensione e stile). Questo vale anche quando si impostano le proprietà di formattazione del carattere in un intervallo di testo [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Le proprietà possono essere ottenute da un oggetto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) o da oggetti [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) che rappresentano una particolare istanza denominata. Come osservato in precedenza, i valori restituiti dai metodi getWeight e getStretch possono essere approssimazioni arrotondate per i valori di asse effettivi utilizzati per definire l'istanza denominata, ma DirectWrite eseguirà il mapping della combinazione di proprietà all'istanza denominata desiderata. 

Analogamente, se un'app usa [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) per creare dati di fallback del tipo di carattere personalizzati, le famiglie vengono specificate per i mapping di intervalli di caratteri usando nomi di famiglia compatibili con WSS. Il fallback del tipo di carattere all'interno di DirectWrite è basato sulle famiglie con DirectWrite che seleziona una variante all'interno di una famiglia di fallback che rappresenta una corrispondenza più vicina per la variante della famiglia iniziale. Per le varianti che coinvolgono dimensioni diverse da weight, stretch e Style, DirectWrite non è attualmente in grado di selezionare tali varianti all'interno di una famiglia di fallback, a meno che non siano stati creati dati di fallback personalizzati per fornire mapping di fallback per le famiglie con particolari attributi non WSS, ad esempio le varianti di dimensione ottica "didascalia".

 

 