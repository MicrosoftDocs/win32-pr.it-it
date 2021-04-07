---
description: Con Windows Vista, l'albero degli elementi Windows Image Acquisition (WIA) è stato modificato in modo significativo.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Informazioni sull'albero degli elementi IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881901"
---
# <a name="about-the-iwiaitem2-item-tree"></a>Informazioni sull'albero degli elementi IWiaItem2

Con Windows Vista, l'albero degli elementi Windows Image Acquisition (WIA) è stato modificato in modo significativo. Gli elementi [**IWiaItem2**](-wia-iwiaitem2.md) vengono usati per rappresentare gli attributi del dispositivo e i dati del dispositivo. Le applicazioni di imaging visualizzano un dispositivo Windows Image Acquisition (WIA) 2,0 come albero gerarchico di elementi, con l'elemento radice che rappresenta il dispositivo stesso e gli elementi figlio che rappresentano elementi come origini dati programmabili, immagini o cartelle contenenti immagini.

-   [Elementi dell'applicazione](#application-items)
-   [Flag elemento](#item-flags)
-   [Categorie di elementi](#item-categories)
-   [Elemento radice](#root-item)
-   [Elemento dati](#data-item)
-   [Argomenti correlati](#related-topics)

## <a name="application-items"></a>Elementi dell'applicazione

L'albero degli elementi WIA 2,0 che un'applicazione può visualizzare è separato dall'albero creato e gestito da un WIA 2,0 minidriver. Quando un minidriver crea un albero, il servizio WIA 2,0 utilizza questo albero degli elementi WIA 2,0 come guida per creare una copia dell'albero che può essere visualizzato dalle applicazioni di imaging. Gli elementi dell'albero copiato sono detti elementi *dell'applicazione* . Gli elementi dell'albero creati da un minidriver sono denominati elementi del *driver* .

Un elemento WIA può rappresentare un'origine dati programmabile per il feeder di documenti di uno scanner o i dati archiviati nel dispositivo. Un dispositivo WIA deve essere suddiviso in singoli elementi che descrivono dati diversi prodotti da tale dispositivo.

Uno scanner WIA, ad esempio, che supporta l'analisi di livello piano e l'analisi dei feed di documenti può essere suddiviso in due elementi figlio. Uno rappresenta la funzionalità di analisi piana e l'altro rappresenta la funzionalità di analisi del feeder di documenti.

Più immagini disposte in uno scanner piano e analizzate contemporaneamente possono essere inserite in una cartella. Utilizzando il filtro di segmentazione ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), è possibile creare ogni immagine o area secondaria come elemento figlio della cartella.

L'albero WIA per un dispositivo fotocamera che archivia foto ("film") può essere suddiviso in elementi che rappresentano cartelle, sottocartelle e foto.

## <a name="item-flags"></a>Flag elemento

I flag elemento WIA consentono di classificare il contenuto o il comportamento supportato di un particolare elemento WIA. I flag elemento WIA rientrano in due gruppi.

1.  I flag di stato dell'elemento segnalano lo stato corrente dell'elemento WIA, ad esempio [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted** e così via.
2.  I flag di rappresentazione/utilizzo dati elemento segnalano i dati che l'elemento WIA rappresenta o può produrre se trasferiti. Ad esempio, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) è un flag di rappresentazione dei dati che indica all'applicazione che i dati associati all'elemento WIA corrente sono dati di immagine e devono avere proprietà dei dati di immagine. **WIA \_ I \_ \_ flag degli elementi IPA** sono un flag di utilizzo degli elementi che indica all'applicazione che l'elemento WIA è configurabile e segue un set di regole di configurazione predefinite basate sulla [**\_ \_ \_ categoria di elementi dell'IPA WIA**](-wia-wiaitempropcommonitem.md) e che la configurazione può eventualmente modificare il risultato per ogni trasferimento dei dati. Per ulteriori informazioni sulle definizioni di categoria, vedere categorie di elementi delle [categorie di elementi](#item-categories) .

Nell'immagine seguente viene illustrato un esempio di albero degli elementi WIA e dei diversi flag che possono essere associati a ogni elemento.

![esempi di flag di elemento per gli elementi in un albero](images/scannertree1.jpg)

## <a name="item-categories"></a>Categorie di elementi

Gli elementi WIA sono raggruppati in categorie usando i valori delle proprietà di [**\_ \_ \_ categoria**](-wia-wiaitempropcommonitem.md) degli elementi dell'IPA WIA. Queste categorie definiscono la modalità di trattamento o di utilizzo di un elemento WIA. Se, ad esempio, l'elemento rappresenta un file terminato ( \_ file di categoria \_ terminata WIA \_ ), un'applicazione WIA deve presupporre che i dati siano statici e che si trovino nel dispositivo. Se l'elemento rappresenta un feeder (WIA \_ Category \_ Feeder), l'applicazione deve prevedere che contenga le proprietà richieste del feed di documenti e funzioni come un feeder di documenti.

Le categorie definite da WIA sono:

-   \_categoria WIA \_ auto
-   \_feed di categoria WIA \_
-   \_film di categoria WIA \_
-   \_file di categoria \_ completato \_ WIA
-   \_categoria WIA \_ piana

Ad esempio, è possibile che un elemento piano dello scanner includa i [**flag degli \_ \_ elementi \_ dell'IPA WIA**](-wia-wiaitempropcommonitem.md) impostati su [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** e **WiaItemTypeProgrammableDataSource** e che la proprietà della **categoria di \_ \_ elementi \_ WIA IPA** sia impostata su WIA \_ categoria \_ piana.

La tabella seguente illustra il raggruppamento di categorie WIA con i flag di elemento e gli elementi WIA. Questa tabella non include un elenco completo dei flag di elemento WIA definiti da WIA.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoria WIA</th>
<th>Flag elemento WIA validi</th>
<th>Set di proprietà WIA</th>
<th>Elementi WIA</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_AUTO</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></li>
</ul></td>
<td>Il set di proprietà include proprietà dello scanner configurate automaticamente.</td>
<td>Elemento WIA automatico che rappresenta le impostazioni di analisi configurate automaticamente dello scanner.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FEEDER</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>Il set di proprietà include le proprietà del controllo dello scanner di Feeder, in genere l'immagine e il set di proprietà specifico del documento</td>
<td>Elementi del feed WIA, inclusi gli elementi figlio che rappresentano le pagine iniziali e secondarie di un documento.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>Il set di proprietà include le proprietà del controllo dello scanner di film (in genere immagini e set di proprietà specifiche del documento).</td>
<td>Elementi di film WIA, inclusi gli elementi figlio che rappresentano i singoli frame di analisi.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
</ul></td>
<td>Il set di proprietà per questo elemento dipende dal tipo di elemento segnalato. Ad esempio, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> deve includere alcune proprietà dell'elemento immagine, come bits per pixel e così via.</td>
<td>Elementi di archiviazione WIA, inclusi gli elementi figlio che rappresentano il contenuto del file completato (file di dati quali JPEG, HTML, TXT e così via).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>: può essere presente se lo scanner supporta l'analisi a più elementi.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>: può essere presente se l'applicazione genera un elemento WIA durante una sessione di analisi di più elementi.</li>
</ul></td>
<td>Il set di proprietà include le proprietà del controllo scanner piano (in genere l'immagine e il set di proprietà specifico del documento).</td>
<td>Gli elementi del piano WIA, inclusi gli elementi figlio che rappresentano le aree sottoposte ad analisi sulla piastra piana dello scanner.</td>
</tr>
</tbody>
</table>



 

Il grafico seguente mostra un esempio di albero degli elementi WIA e le varie categorie che possono essere associate a ogni elemento.

![esempi di categorie di elementi per gli elementi in un albero](images/scannertree2.jpg)

## <a name="root-item"></a>Elemento radice

Un elemento radice WIA è un elemento di cartella contrassegnato con i flag [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) e **WiaItemTypeDevice** che rappresenta il dispositivo stesso. Contiene attributi del dispositivo come il produttore, il nome del dispositivo e gli attributi del driver, ad esempio la versione del driver e l'identificatore di classe dell'interfaccia utente (CLSID). Le applicazioni per la creazione di immagini ottengono la radice nell'albero degli elementi WIA chiamando il metodo [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) . L'applicazione usa l'elemento radice per accedere ai singoli elementi WIA figlio enumerando l'albero (vedere [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).

## <a name="data-item"></a>DataItem

Qualsiasi elemento che può essere utilizzato per trasferire i dati viene considerato un elemento di dati. Sono inclusi gli elementi contrassegnati con il flag [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) .

Gli elementi della cartella e gli elementi non cartella possono esporre la possibilità di trasferire i dati tramite la funzione contrassegnata con il flag [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) . Qualsiasi elemento con questo set di flag deve fornire le seguenti proprietà dell'elemento WIA:

-   [**\_diritti di \_ accesso con IPA WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_ \_ dimensioni elemento IPA \_ WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_dimensioni del \_ buffer \_ IPA WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_formato ipa \_ WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_ \_ formato preferito dell'IPA WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_TYMED IPA \_ WIA**](-wia-wiaitempropcommonitem.md)
-   [**\_estensione del \_ nome file IPA WIA \_**](-wia-wiaitempropcommonitem.md)

Le origini dati programmabili contrassegnate con il flag [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) devono anche fornire il set di proprietà obbligatorio per l'elemento dati.

Gli elementi di dati WIA possono avere proprietà aggiuntive a seconda delle impostazioni dei flag dell'elemento. Ad esempio, gli elementi WIA contrassegnati con il flag [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) devono avere proprietà delle informazioni specifiche dell'immagine, ad esempio la [**\_ \_ profondità dell'IPA WIA**](-wia-wiaitempropcommonitem.md) e il **\_ \_ numero \_ di \_ righe dell'IPA WIA**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)
</dt> <dt>

[**IWiaDevMgr2**](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



