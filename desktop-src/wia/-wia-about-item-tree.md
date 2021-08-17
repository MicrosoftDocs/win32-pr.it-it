---
description: Con Windows Vista, l'albero Windows di elementi di acquisizione di immagini (WIA) è stato modificato in modo significativo.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Informazioni sull'albero degli elementi IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae342f5a85e61b6384604dae703881c6888e3e1cf8e61cc8a39a32ac77ad436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264431"
---
# <a name="about-the-iwiaitem2-item-tree"></a>Informazioni sull'albero degli elementi IWiaItem2

Con Windows Vista, l'albero Windows di elementi di acquisizione di immagini (WIA) è stato modificato in modo significativo. [**Gli elementi IWiaItem2**](-wia-iwiaitem2.md) vengono usati per rappresentare gli attributi e i dati del dispositivo. Le applicazioni di creazione dell'immagine vedono un dispositivo di acquisizione di immagini di Windows (WIA) 2.0 come albero gerarchico di elementi, con l'elemento radice che rappresenta il dispositivo stesso e gli elementi figlio che rappresentano elementi come origini dati programmabili, immagini o cartelle che contengono immagini.

-   [Elementi dell'applicazione](#application-items)
-   [Flag di elemento](#item-flags)
-   [Categorie di elementi](#item-categories)
-   [Elemento radice](#root-item)
-   [Elemento dati](#data-item)
-   [Argomenti correlati](#related-topics)

## <a name="application-items"></a>Elementi dell'applicazione

L'albero degli elementi WIA 2.0 che un'applicazione può visualizzare è separato dall'albero creato e gestito da un minidriver WIA 2.0. Quando un minidriver crea un albero, il servizio WIA 2.0 usa questo albero di elementi WIA 2.0 come guida per creare una copia dell'albero che può essere visualizzata dalle applicazioni di creazione dell'immagine. Gli elementi nell'albero copiato sono denominati *elementi dell'applicazione.* Gli elementi nell'albero creati da un minidriver sono denominati *elementi driver.*

Un elemento WIA può rappresentare un'origine dati programmabile per l'alimentatore di documenti di uno scanner o i dati archiviati in tale dispositivo. Un dispositivo WIA deve essere suddiviso in singoli elementi che descrivono dati diversi prodotti da tale dispositivo.

Ad esempio, uno scanner WIA che supporta sia l'analisi bi flat che l'analisi dell'alimentatore di documenti potrebbe essere suddiviso in due elementi figlio. Uno rappresenta la funzionalità di analisi bi flat e l'altro rappresenta la funzionalità di analisi dell'alimentatore di documenti.

È possibile inserire in un'unica cartella più immagini disposte su uno scanner bi flat e analizzate contemporaneamente. Usando il filtro di segmentazione [**(IWiaSegmentationFilter),**](-wia-iwiasegmentationfilter.md)ogni immagine o sottoarea può quindi essere creata come elemento figlio della cartella.

L'albero WIA per un dispositivo fotocamera che archivia foto ("Film") può essere diviso in elementi che rappresentano cartelle, sottocartelle e foto.

## <a name="item-flags"></a>Flag di elemento

I flag di elemento WIA consentono di classificare il contenuto o il comportamento supportato di un particolare elemento WIA. I flag di elemento WIA rientrano in due gruppi.

1.  I flag di stato dell'elemento segnalano lo stato corrente dell'elemento WIA, ad esempio [**WiaItemTypeDisconnected,**](-wia-wia-item-type-flags.md) **WiaItemTypeDeleted** e così via.
2.  I flag di rappresentazione/utilizzo dei dati degli elementi segnalano i dati che l'elemento WIA rappresenta o può produrre se trasferito. Ad esempio, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) è un flag di rappresentazione dei dati che indica all'applicazione che i dati associati all'elemento WIA corrente sono dati immagine e devono avere proprietà dei dati immagine. **WiA \_ IPA \_ ITEM \_ FLAGS** è un flag di utilizzo degli elementi che indica all'applicazione che l'elemento WIA è configurabile e segue un set di regole di configurazione predefinite basate sulla CATEGORIA DI ELEMENTI [**\_ IPA \_ \_ WIA**](-wia-wiaitempropcommonitem.md) e che la configurazione può eventualmente modificare il risultato per ogni trasferimento dei dati. Per altre informazioni sulle definizioni di categoria, vedere [Categorie di elementi.](#item-categories)

La figura seguente mostra un esempio di albero di elementi WIA e i vari flag che possono essere associati a ogni elemento.

![esempi di flag di elementi per gli elementi in un albero](images/scannertree1.jpg)

## <a name="item-categories"></a>Categorie di elementi

Gli elementi WIA vengono raggruppati in categorie usando i valori della proprietà ITEM CATEGORY di [**\_ WIA IPA. \_ \_**](-wia-wiaitempropcommonitem.md) Queste categorie definiscono il modo in cui un elemento WIA deve essere trattato o usato. Ad esempio, se l'elemento rappresenta un file completato (WIA CATEGORY FINISHED FILE), un'applicazione WIA deve presupporre che i dati siano statici e si \_ \_ \_ trovino nel dispositivo. Se l'elemento rappresenta un feeder (WIA CATEGORY FEEDER), l'applicazione deve aspettarsi che contenga le proprietà obbligatorie dell'alimentatore di documenti e funzioni come un \_ \_ feeder di documenti.

Le categorie definite da WIA sono:

-   WIA \_ CATEGORY \_ AUTO
-   FEEDER CATEGORIA WIA \_ \_
-   WIA \_ CATEGORY \_ FILM
-   FILE CATEGORIA WIA \_ \_ \_ COMPLETATO
-   CATEGORIA WIA \_ \_ FLATBED

Ad esempio, l'elemento flat di uno scanner può avere i FLAG ELEMENTO [**\_ IPA \_ \_ WIA**](-wia-wiaitempropcommonitem.md) impostati su [**WiaItemTypeImage,**](-wia-wia-item-type-flags.md) **WiaItemTypeTransfer** e **WiaItemTypeProgrammableDataSource** e la proprietà **WIA \_ IPA \_ ITEM \_ CATEGORY** impostata su WIA \_ CATEGORY \_ FLATBED.

La tabella seguente illustra il raggruppamento delle categorie WIA con i flag di elemento e gli elementi WIA. Questa tabella non include un elenco completo dei flag di elementi WIA definiti da WIA.



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
<th>Flag di elementi WIA validi</th>
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
<td>Il set di proprietà include le proprietà dello scanner configurate automaticamente.</td>
<td>Elemento automatico WIA che rappresenta le impostazioni di analisi configurate automaticamente dello scanner.</td>
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
<td>Il set di proprietà include le proprietà del controllo dello scanner di feed (in genere set di proprietà specifiche dell'immagine e del documento).</td>
<td>Elementi del feeder WIA, inclusi gli elementi figlio che rappresentano le pagine anteriore e posteriore di un documento.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>Il set di proprietà include le proprietà del controllo dello scanner di film (in genere set di proprietà specifiche di immagini e documenti).</td>
<td>Elementi WIA Film, inclusi gli elementi figlio che rappresentano i singoli fotogrammi di analisi.</td>
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
<td>La proprietà impostata su questo elemento dipende dal tipo di elemento segnalato. Ad esempio, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> deve includere alcune proprietà dell'elemento immagine, ad esempio bit per pixel e così via.</td>
<td>Elementi di archiviazione WIA, inclusi gli elementi figlio che rappresentano il contenuto del file completato (file di dati come JPEG, HTML, TXT e così via).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder:</strong></a>può essere presente se lo scanner supporta l'analisi di più elementi.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated:</strong></a>può essere presente se l'applicazione genera un elemento WIA durante una sessione di analisi di più elementi.</li>
</ul></td>
<td>Il set di proprietà include le proprietà dei controlli dello scanner flat (in genere set di proprietà specifiche dell'immagine e del documento).</td>
<td>Elementi bi flat WIA, inclusi gli elementi figlio che rappresentano le aree analizzate sulla pinza a piana dello scanner.</td>
</tr>
</tbody>
</table>



 

La figura seguente mostra un esempio di albero di elementi WIA e le varie categorie che possono essere associate a ogni elemento.

![esempi di categorie di elementi per gli elementi in un albero](images/scannertree2.jpg)

## <a name="root-item"></a>Elemento radice

Un elemento radice WIA è un elemento della cartella contrassegnato con i flag [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) e **WiaItemTypeDevice** che rappresenta il dispositivo stesso. Contiene attributi di dispositivo come produttore, nome del dispositivo e attributi del driver, ad esempio la versione del driver e l'identificatore di classe dell'interfaccia utente (CLSID). Le applicazioni di creazione dell'immagine ottengono la radice dell'albero degli elementi WIA chiamando [**il metodo IWiaDevMgr2::CreateDevice.**](-wia-iwiadevmgr2-createdevice.md) L'applicazione usa l'elemento radice per ottenere l'accesso ai singoli elementi WIA figlio enumerando l'albero (vedere [**IEnumWiaItem2).**](-wia-ienumwiaitem2.md)

## <a name="data-item"></a>DataItem

Qualsiasi elemento che può essere utilizzato per trasferire i dati viene considerato un elemento di dati. Sono inclusi gli elementi contrassegnati con il flag [**WiaItemTypeProgrammableDataSource.**](-wia-wia-item-type-flags.md)

Gli elementi cartella e gli elementi non cartella possono esporre la possibilità di trasferire i dati contrassegnati con il flag [**WiaItemTypeTransfer.**](-wia-wia-item-type-flags.md) Qualsiasi elemento con questo flag impostato deve fornire le proprietà dell'elemento WIA seguenti:

-   [**DIRITTI DI \_ ACCESSO IPA DI WIA \_ \_**](-wia-wiaitempropcommonitem.md)
-   [**DIMENSIONI \_ DELL'ELEMENTO IPA WIA \_ \_**](-wia-wiaitempropcommonitem.md)
-   [**DIMENSIONI \_ DEL BUFFER IPA WIA \_ \_**](-wia-wiaitempropcommonitem.md)
-   [**FORMATO \_ IPA WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**FORMATO PREFERITO \_ IPA WIA \_ \_**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ TYMED**](-wia-wiaitempropcommonitem.md)
-   [**ESTENSIONE DEL \_ NOME FILE IPA DI WIA \_ \_**](-wia-wiaitempropcommonitem.md)

Anche gli elementi dell'origine dati programmabili contrassegnati con il flag [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) devono fornire il set di proprietà obbligatorio dell'elemento dati.

Gli elementi di dati WIA possono avere proprietà aggiuntive a seconda delle impostazioni del flag dell'elemento. Ad esempio, gli elementi WIA contrassegnati con il flag [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) devono avere proprietà di informazioni specifiche dell'immagine, ad esempio [**WIA \_ IPA \_ DEPTH**](-wia-wiaitempropcommonitem.md) e **WIA \_ IPA \_ NUMBER OF \_ \_ LINES.**

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

 

 



