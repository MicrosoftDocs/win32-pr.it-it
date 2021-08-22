---
description: La tabella delle funzionalità definisce la struttura ad albero logica delle funzionalità e contiene le colonne illustrate nella tabella seguente.
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: Tabella delle funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dcf9177c44f407876cbe339925ca4524034a1335393161bb40310d60c158ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251761"
---
# <a name="feature-table"></a>Tabella delle funzionalità

La tabella delle funzionalità definisce la struttura ad albero logica delle funzionalità e contiene le colonne illustrate nella tabella seguente.



| Colonna          | Tipo                         | Chiave | Nullable |
|-----------------|------------------------------|-----|----------|
| Funzionalità         | [Identificatore](identifier.md) | S   | N        |
| Elemento padre \_ della funzionalità | [Identificatore](identifier.md) | N   | S        |
| Title           | [Text](text.md)             | N   | S        |
| Descrizione     | [Text](text.md)             | N   | S        |
| Visualizza         | [Integer](integer.md)       | N   | S        |
| Level           | [Integer](integer.md)       | N   | N        |
| Directory\_     | [Identificatore](identifier.md) | N   | S        |
| Attributi      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Feature"></span><span id="feature"></span><span id="FEATURE"></span>Funzionalità
</dt> <dd>

Chiave primaria utilizzata per identificare un record di funzionalità specifico. Il valore in questo campo non deve superare la lunghezza massima di 38 caratteri.

</dd> <dt>

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>Elemento padre \_ della funzionalità
</dt> <dd>

Chiave facoltativa di un record padre nella stessa tabella.

La chiave punta alla colonna Feature. Se la funzionalità padre non è selezionata, questa funzionalità non viene installata. Un valore Null in questo campo indica che questa funzionalità non ha un elemento padre ed è un elemento radice. La colonna \_ Feature Parent non deve essere uguale alla colonna Feature dello stesso record.

> [!Note]  
> La profondità massima di qualsiasi funzionalità è 16. Se esiste una funzionalità che supera la profondità massima, viene restituito un errore [2701.](windows-installer-error-messages.md)

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titolo
</dt> <dd>

Stringa breve di testo che identifica una funzionalità.

Questa stringa viene elencata come elemento dal [controllo SelectionTree della](selectiontree-control.md) finestra [di dialogo di selezione.](selection-dialog.md)

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Stringa di testo più lunga che descrive una funzionalità.

Questa stringa localizzabile viene visualizzata dal [controllo](text-control.md) Testo della finestra di dialogo [di selezione.](selection-dialog.md)

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>Visualizzazione
</dt> <dd>

Il numero in questo campo specifica l'ordine in cui la funzionalità deve essere visualizzata nell'interfaccia utente.

Il valore determina anche se la funzionalità viene inizialmente visualizzata espansa o compressa. Se il valore è Null o 0 (zero), il record non viene visualizzato.

-   Se il valore è dispari, il nodo della funzionalità viene inizialmente espanso.
-   Se il valore è pari, il nodo della funzionalità viene inizialmente compresso.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Livello
</dt> <dd>

Livello di installazione iniziale di questa funzionalità. [L'elaborazione della tabella delle condizioni](condition-table.md) può modificare il valore del livello.

Un livello di installazione pari a 0 (zero) disabilita l'elemento e ne impedisce la visualizzazione. Una funzionalità con livello di installazione 0 (zero) non viene installata durante l'installazione, incluse le installazioni amministrative. Per altre informazioni, vedere le informazioni sul livello di installazione nella sezione Osservazioni di questo argomento.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

La colonna \_ Directory specifica il nome di una directory che può essere configurata da una finestra [di dialogo di selezione.](selection-dialog.md)

Poiché questo campo è una chiave nella [tabella di directory](directory-table.md), la directory specificata deve essere elencata nella prima colonna della tabella directory. È necessario immettere una [proprietà pubblica](public-properties.md) in questa colonna per rendere configurabile la directory e visualizzare un **pulsante** Sfoglia nella finestra di dialogo [di selezione.](selection-dialog.md)

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

L'opzione di esecuzione remota per le funzionalità non installate e per le quali non viene effettuata alcuna richiesta di stato della funzionalità tramite una delle proprietà seguenti.

-   [**Proprietà ADDLOCAL**](addlocal.md)
-   [**Proprietà ADDSOURCE**](addsource.md)
-   [**Proprietà ADDDEFAULT**](adddefault.md)
-   [**Proprietà COMPADDLOCAL**](compaddlocal.md)
-   [**Proprietà COMPADDSOURCE**](compaddsource.md)
-   [**Proprietà FILEADDLOCAL**](fileaddlocal.md)
-   [**Proprietà FILEADDSOURCE**](fileaddsource.md)
-   [**REMOVE Property**](remove.md)
-   [**Proprietà REINSTALL**](reinstall.md)
-   [**Proprietà ADVERTISE**](advertise.md)

Aggiungere i bit indicati al valore totale di questa colonna per includere un'opzione di esecuzione remota.

-   Se questo campo è vuoto, il valore predefinito è 0 (zero), msidbFeatureAttributesFavorLocal.
-   Se il livello di installazione della funzionalità è 0 (zero) o maggiore o uguale al livello di installazione corrente, non viene apportata alcuna modifica nello stato della funzionalità.



| Nome                                         | Decimal | Valore esadecimale | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbFeatureAttributesFavorLocal             | 0       | 0x0000      | I componenti di questa funzionalità non contrassegnati per l'installazione dall'origine vengono installati in locale. Un componente condiviso da due o più funzionalità, alcune delle quali sono impostate su msidbFeatureAttributesFavorLocal e altre su msidbFeatureAttributesFavorSource, viene installato localmente. I componenti contrassegnati come msidbComponentAttributesSourceOnly nella [tabella dei](component-table.md) componenti vengono sempre eseguiti dal CD/server di origine. I bit msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource funzionano con le funzionalità non elencate dalla [**proprietà ADVERTISE**](advertise.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbFeatureAttributesFavorSource            | 1       | 0x0001      | I componenti di questa funzionalità non contrassegnati per l'installazione locale vengono installati per l'esecuzione dal CD-ROM o dal server di origine. Un componente condiviso da due o più funzionalità, alcune delle quali sono impostate su msidbFeatureAttributesFavorLocal e altre su msidbFeatureAttributesFavorSource, viene installato per l'esecuzione in locale. I componenti contrassegnati come msidbComponentAttributesLocalOnly nella [tabella dei](component-table.md) componenti vengono sempre installati in locale. I bit msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource funzionano con funzionalità non elencate dalla [**proprietà ADVERTISE**](advertise.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesFollowParent           | 2       | 0x0002      | Impostare questo attributo e lo stato della funzionalità è lo stesso dello stato dell'elemento padre della funzionalità. Non è possibile usare questa opzione se la funzionalità si trova nella radice di un albero delle funzionalità. Omettere questo attributo e lo stato della funzionalità viene determinato in base a msidbFeatureAttributesDisallowAdvertise e msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/> Per garantire che lo stato della funzionalità figlio segua sempre lo stato del relativo elemento padre, anche quando l'elemento figlio e l'elemento padre sono inizialmente impostati su absent nel controllo SelectionTree, è necessario includere sia msidbFeatureAttributesFollowParent che msidbFeatureAttributesUIDisallowAbsent negli attributi della funzionalità figlio.<br/> Si noti che se si imposta msidbFeatureAttributesFollowParent senza impostare msidbFeatureAttributesUIDisallowAbsent, il programma di installazione non può forzare la funzionalità figlio fuori dallo stato assente. In questo caso, la funzionalità figlio corrisponde allo stato di installazione dell'elemento padre solo se l'elemento figlio è impostato su un valore diverso da absent.<br/> Impostare msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent per assicurarsi che una funzionalità figlio segua lo stato della funzionalità padre.<br/> |
| msidbFeatureAttributesFavorAdvertise         | 4       | 0x0004      | Impostare questo attributo e lo stato della funzionalità è Advertise. Se la funzionalità è elencata dalla proprietà [**ADDDEFAULT,**](adddefault.md) questo bit viene ignorato e lo stato della funzionalità viene determinato in base a msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource. Omettere questo attributo e lo stato della funzionalità viene determinato in base a msidbFeatureAttributesDisallowAdvertise e msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbFeatureAttributesDisallowAdvertise      | 8       | 0x0008      | Si noti che questo bit funziona solo con le funzionalità elencate dalla [**proprietà ADVERTISE**](advertise.md). Impostare questo attributo per impedire l'annuncio della funzionalità.<br/> Impostare questo attributo e se la funzionalità elencata non è padre o figlio, la funzionalità viene installata in base a msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/> Impostare questo attributo per l'elemento padre di una funzionalità elencata e l'elemento padre viene installato.<br/> Impostare questo attributo per l'elemento figlio di una funzionalità elencata e lo stato dell'elemento figlio è Absent.<br/> Omettere questo attributo e se la funzionalità elencata non è padre o figlio, lo stato della funzionalità è Advertise.<br/> Omettere questo attributo e se la funzionalità elencata è padre o figlio, lo stato di entrambe le funzionalità è Advertise.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbFeatureAttributesUIDisallowAbsent       | 16      | 0x0010      | Impostare questo attributo e l'interfaccia utente non visualizza un'opzione per modificare lo stato della funzionalità su Absent. L'impostazione di questo attributo forza la funzionalità allo stato di installazione, indipendentemente dal fatto che sia visibile o meno nell'interfaccia utente. Omettere questo attributo e nell'interfaccia utente viene visualizzata un'opzione per modificare lo stato della funzionalità in Absent.<br/> Impostare msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent per assicurarsi che una funzionalità figlio segua lo stato della funzionalità padre.<br/> L'impostazione di questo attributo non influisce solo sull'interfaccia utente, ma forza anche la funzionalità allo stato di installazione indipendentemente dal fatto che la funzionalità sia visibile o meno nell'interfaccia utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesNoUnsupportedAdvertise | 32      | 0x0020      | Impostare questo attributo e la pubblicità è disabilitata per la funzionalità se la shell del sistema operativo non supporta Windows descrittori del programma di installazione. Omettere questo attributo e la pubblicità non è disabilitata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Alcuni attributi sono esclusivi l'uno dall'altro. Se si tenta di impostare questi attributi insieme sulla stessa funzionalità, il pacchetto di installazione non riesce [**a convalidare il pacchetto**](package-validation.md).

-   Non usare msidbFeatureAttributesFavorAdvertise con msidbFeatureAttributesDisallowAdvertise.
-   Non usare msidbFeatureAttributesNoUnsupportedAdvertise con msidbFeatureAttributesDisallowAdvertise insieme.
-   Non usare msidbFeatureAttributesFollowParent con msidbFeatureAttributesFavorSource.
-   Si noti che i valori msidbFeatureAttributesFollowParent e msidbFeatureAttributesFavorLocal si escludono a vicenda. Se si usa il valore msidbFeatureAttributesFollowParent, si presuppone che il valore msidbFeatureAttributesFavorLocal non esista.

</dd> </dl>

Si noti che se è installata una funzionalità figlio, viene installata anche la funzionalità padre. Se è installata una funzionalità padre, la relativa funzionalità figlio non viene necessariamente installata a meno che non siano impostati gli attributi msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent. Questa relazione gerarchica dell'installazione delle funzionalità padre e figlio viene usata anche per le installazioni gui e le installazioni che usano le proprietà della riga di comando.

## <a name="remarks"></a>Commenti

A questa tabella vengono aggiunte diverse colonne temporanee aggiuntive quando viene caricata in memoria per i calcoli usati dalla determinazione dei costi e dalla selezione dell'interfaccia utente.

Un componente può essere condiviso tra due o più funzionalità o applicazioni. Se due o più funzionalità fanno riferimento allo stesso componente, tale componente viene selezionato per l'installazione se è selezionata una delle funzionalità associate. Questo può anche essere il motivo per cui le funzionalità figlio non vengono disinstallate quando viene rimossa una funzionalità padre. Se la funzionalità figlio è costituita da componenti necessari per altre funzionalità o applicazioni, il Windows Installer non rimuove la funzionalità figlio.

Per altre informazioni, vedere [Controllo degli stati di selezione delle funzionalità](controlling-feature-selection-states.md).

Livello di installazione:

-   Per qualsiasi installazione è presente un livello di installazione definito, ovvero un valore integrale compreso tra 1 e 32.767. Il valore iniziale è determinato dalla [**proprietà INSTALLLEVEL**](installlevel.md), impostata nella [tabella delle proprietà](property-table.md).
-   Una funzionalità viene installata solo se il valore del livello di funzionalità è minore o uguale al livello di installazione corrente. È possibile creare l'interfaccia utente in modo che, quando l'installazione viene inizializzata, il programma di installazione consenta all'utente di modificare il livello di installazione di qualsiasi funzionalità nella tabella delle funzionalità. Ad esempio, un autore può definire valori del livello di installazione che rappresentano opzioni di installazione specifiche, ad esempio Custom **,** **Typical** o **Minimum,** e quindi creare una finestra di dialogo che usa [SetInstallLevel ControlEvents](setinstalllevel-controlevent.md) per consentire all'utente di selezionare uno di questi stati.
-   A seconda dello stato selezionato dall'utente, la finestra di dialogo imposta la proprietà del livello di installazione sul valore corrispondente. Se l'autore assegna a **Typical** un livello 100 e l'utente seleziona **Typical**, vengono installate solo le funzionalità con un livello di 100 o inferiore. Inoltre, **l'opzione Personalizzata** può causare un'altra finestra di dialogo che contiene un [controllo SelectionTree](selectiontree-control.md). Il controllo SelectionTree consente quindi all'utente di modificare singolarmente l'installazione di ogni funzionalità.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE10](ice10.md)  
[ICE14](ice14.md)  
[ICE21](ice21.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE45](ice45.md)  
[ICE47](ice47.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
[ICE94](ice94.md)  
</dl>

 

 




