---
description: La tabella Feature definisce la struttura ad albero logica delle funzionalità e contiene le colonne mostrate nella tabella seguente.
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: Tabella delle funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa91df750c4994a2d8a2308705213e48c864518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309482"
---
# <a name="feature-table"></a>Tabella delle funzionalità

La tabella Feature definisce la struttura ad albero logica delle funzionalità e contiene le colonne mostrate nella tabella seguente.



| Colonna          | Tipo                         | Chiave | Nullable |
|-----------------|------------------------------|-----|----------|
| Funzionalità         | [Identificatore](identifier.md) | S   | N        |
| \_Elemento padre della funzionalità | [Identificatore](identifier.md) | N   | S        |
| Titolo           | [Text](text.md)             | N   | S        |
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

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>\_Elemento padre della funzionalità
</dt> <dd>

Chiave facoltativa di un record padre nella stessa tabella.

La chiave punta alla colonna feature. Se la funzionalità padre non è selezionata, la funzionalità non è installata. Un valore null in questo campo indica che questa funzionalità non dispone di un elemento padre e è un elemento radice. La \_ colonna padre della funzionalità non deve corrispondere alla colonna feature dello stesso record.

> [!Note]  
> La profondità massima di qualsiasi funzionalità è 16. Se una funzionalità che supera questa profondità massima esiste, viene restituito un [errore 2701](windows-installer-error-messages.md) .

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titolo
</dt> <dd>

Stringa di testo breve che identifica una funzionalità.

Questa stringa viene elencata come elemento dal [controllo SelectionTree](selectiontree-control.md) della finestra di [dialogo di selezione](selection-dialog.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Stringa di testo più lunga che descrive una funzionalità.

Questa stringa localizzabile viene visualizzata dal [controllo testo](text-control.md) della finestra di [dialogo di selezione](selection-dialog.md).

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>Visualizzare
</dt> <dd>

Il numero in questo campo specifica l'ordine in cui la funzionalità deve essere visualizzata nell'interfaccia utente.

Il valore determina anche se la funzionalità viene inizialmente visualizzata espansa o compressa. Se il valore è null o 0 (zero), il record non viene visualizzato.

-   Se il valore è dispari, il nodo della funzionalità viene espanso inizialmente.
-   Se il valore è pari, il nodo della funzionalità viene inizialmente compresso.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Livello
</dt> <dd>

Livello di installazione iniziale della funzionalità. L'elaborazione della [tabella della condizione](condition-table.md) può modificare il valore del livello.

Un livello di installazione pari a 0 (zero) Disabilita l'elemento e ne impedisce la visualizzazione. Una funzionalità con un livello di installazione pari a 0 (zero) non viene installata durante l'installazione, incluse le installazioni amministrative. Per ulteriori informazioni, vedere le informazioni sul livello di installazione nella sezione Osservazioni di questo argomento.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Nella \_ colonna directory viene specificato il nome di una directory che può essere configurata tramite una [finestra di dialogo di selezione](selection-dialog.md).

Poiché questo campo è una chiave nella [tabella di directory](directory-table.md), la directory specificata deve essere elencata nella prima colonna della tabella directory. Per rendere la directory configurabile e visualizzare un pulsante **Sfoglia** nella [finestra di dialogo di selezione](selection-dialog.md), è necessario immettere una [proprietà pubblica](public-properties.md) in questa colonna.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Opzione di esecuzione remota per le funzionalità che non sono installate e per le quali non viene effettuata alcuna richiesta di stato della funzionalità utilizzando una delle proprietà seguenti.

-   [**Proprietà ADDLOCAL**](addlocal.md)
-   [**Proprietà ADDSOURCE**](addsource.md)
-   [**Proprietà ADDDEFAULT**](adddefault.md)
-   [**Proprietà COMPADDLOCAL**](compaddlocal.md)
-   [**Proprietà COMPADDSOURCE**](compaddsource.md)
-   [**Proprietà FILEADDLOCAL**](fileaddlocal.md)
-   [**Proprietà FILEADDSOURCE**](fileaddsource.md)
-   [**Rimuovi proprietà**](remove.md)
-   [**Reinstalla proprietà**](reinstall.md)
-   [**Pubblicizza proprietà**](advertise.md)

Aggiungere i bit indicati al valore totale di questa colonna per includere un'opzione di esecuzione remota.

-   Se questo campo è vuoto, il valore predefinito è 0 (zero), msidbFeatureAttributesFavorLocal.
-   Se il livello di installazione della funzionalità è 0 (zero) o maggiore o uguale al livello di installazione corrente, non viene apportata alcuna modifica nello stato della funzionalità.



| Nome                                         | Decimal | Valore esadecimale | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbFeatureAttributesFavorLocal             | 0       | 0x0000      | I componenti di questa funzionalità che non sono contrassegnati per l'installazione dall'origine sono installati localmente. Componente condiviso da due o più funzionalità, alcune delle quali sono impostate su msidbFeatureAttributesFavorLocal e alcune su msidbFeatureAttributesFavorSource, vengono installate localmente. I componenti contrassegnati come msidbComponentAttributesSourceOnly nella [tabella dei componenti](component-table.md) vengono sempre eseguiti dal CD/server di origine. BITS msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource funzionano con le funzionalità non elencate dalla [**proprietà ADVERTISE**](advertise.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbFeatureAttributesFavorSource            | 1       | 0x0001      | I componenti di questa funzionalità non contrassegnati per l'installazione locale sono installati per l'esecuzione dal CD-ROM o dal server di origine. Un componente condiviso da due o più funzionalità, alcune delle quali sono impostate su msidbFeatureAttributesFavorLocal e alcune su msidbFeatureAttributesFavorSource, viene installato per l'esecuzione in locale. I componenti contrassegnati come msidbComponentAttributesLocalOnly nella [tabella dei componenti](component-table.md) vengono sempre installati localmente. BITS msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource funzionano con le funzionalità non elencate dalla [**proprietà ADVERTISE**](advertise.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesFollowParent           | 2       | 0x0002      | Impostare questo attributo e lo stato della funzionalità corrisponde allo stato dell'elemento padre della funzionalità. Non è possibile usare questa opzione se la funzionalità si trova nella radice di un albero delle funzionalità. Omettere questo attributo e lo stato della funzionalità viene determinato in base a msidbFeatureAttributesDisallowAdvertise e msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/> Per garantire che lo stato della funzionalità figlio segua sempre lo stato del relativo elemento padre, anche quando l'elemento figlio e il padre vengono inizialmente impostati come assenti nel controllo SelectionTree, è necessario includere sia msidbFeatureAttributesFollowParent che msidbFeatureAttributesUIDisallowAbsent negli attributi della funzionalità figlio.<br/> Si noti che se si imposta msidbFeatureAttributesFollowParent senza impostare msidbFeatureAttributesUIDisallowAbsent, il programma di installazione non è in grado di forzare la funzionalità figlio fuori dallo stato assente. In questo caso, la funzionalità figlio corrisponde allo stato di installazione del padre solo se l'elemento figlio è impostato su un valore diverso da assente.<br/> Impostare msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent per assicurarsi che una funzionalità figlio segua lo stato della funzionalità padre.<br/> |
| msidbFeatureAttributesFavorAdvertise         | 4       | 0x0004      | Impostare questo attributo e lo stato della funzionalità è advertise. Se la funzionalità è elencata dalla [**Proprietà AddDefault**](adddefault.md) , questo bit viene ignorato e lo stato della funzionalità viene determinato in base a MsidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource. Omettere questo attributo e lo stato della funzionalità viene determinato in base a msidbFeatureAttributesDisallowAdvertise e msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbFeatureAttributesDisallowAdvertise      | 8       | 0x0008      | Si noti che questo bit funziona solo con le funzionalità elencate dalla [**proprietà ADVERTISE**](advertise.md). Impostare questo attributo per impedire che la funzionalità venga annunciata.<br/> Impostare questo attributo e se la funzionalità elencata non è un elemento padre o un elemento figlio, la funzionalità viene installata in base a msidbFeatureAttributesFavorLocal e msidbFeatureAttributesFavorSource.<br/> Impostare questo attributo per l'elemento padre di una funzionalità elencata e l'elemento padre è installato.<br/> Impostare questo attributo per l'elemento figlio di una funzionalità elencata e lo stato del figlio è assente.<br/> Omettere questo attributo e se la funzionalità elencata non è un elemento padre o un elemento figlio, lo stato della funzionalità è advertise.<br/> Omettere questo attributo e se la funzionalità elencata è un elemento padre o un elemento figlio, lo stato di entrambe le funzionalità è advertise.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbFeatureAttributesUIDisallowAbsent       | 16      | 0x0010      | Impostare questo attributo e l'interfaccia utente non visualizza un'opzione per impostare lo stato della funzionalità su assente. L'impostazione di questo attributo impone la funzionalità allo stato di installazione, indipendentemente dal fatto che la funzionalità sia visibile o meno nell'interfaccia utente. Omettere questo attributo e l'interfaccia utente visualizza un'opzione per modificare lo stato della funzionalità in assente.<br/> Impostare msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent per assicurarsi che una funzionalità figlio segua lo stato della funzionalità padre.<br/> L'impostazione di questo attributo non solo influisca sull'interfaccia utente, ma impone anche alla funzionalità lo stato di installazione se la funzionalità è visibile o meno nell'interfaccia utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesNoUnsupportedAdvertise | 32      | 0x0020      | Impostare questo attributo e la pubblicità viene disabilitata per la funzionalità se la shell del sistema operativo non supporta i descrittori di Windows Installer. Omettere questo attributo e la pubblicità non è disabilitata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Alcuni attributi sono esclusivi tra loro. Se si tenta di impostare questi attributi insieme nella stessa funzionalità, il pacchetto di installazione non riesce a eseguire la [**convalida del pacchetto**](package-validation.md).

-   Non usare msidbFeatureAttributesFavorAdvertise con msidbFeatureAttributesDisallowAdvertise.
-   Non usare msidbFeatureAttributesNoUnsupportedAdvertise con msidbFeatureAttributesDisallowAdvertise insieme.
-   Non usare msidbFeatureAttributesFollowParent con msidbFeatureAttributesFavorSource.
-   Si noti che i valori msidbFeatureAttributesFollowParent e msidbFeatureAttributesFavorLocal si escludono a vicenda. Se viene usato il valore msidbFeatureAttributesFollowParent, si presuppone che il valore di msidbFeatureAttributesFavorLocal non esista.

</dd> </dl>

Si noti che se è installata una funzionalità figlio, viene installata anche la relativa funzionalità padre. Se è installata una funzionalità padre, la relativa funzionalità figlio non viene necessariamente installata a meno che non siano impostati gli attributi msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent. Questa relazione gerarchica dell'installazione delle funzionalità padre e figlio viene usata anche per le installazioni e le installazioni GUI che usano le proprietà della riga di comando.

## <a name="remarks"></a>Commenti

A questa tabella vengono aggiunte diverse colonne temporanee quando vengono caricate in memoria per i calcoli utilizzati dalla selezione di costi e interfacce utente (UI).

Un componente può essere condiviso tra due o più funzionalità o applicazioni. Se due o più funzionalità fanno riferimento allo stesso componente, il componente verrà selezionato per l'installazione se è stata selezionata una delle funzionalità associate. Questo può anche essere il motivo per cui le funzionalità figlio non vengono disinstallate quando viene rimossa una funzionalità padre. Se la funzionalità figlio è costituita da componenti necessari per altre funzionalità o applicazioni, il Windows Installer non rimuove la funzionalità figlio.

Per ulteriori informazioni, vedere [controllo degli Stati di selezione delle funzionalità](controlling-feature-selection-states.md).

Livello di installazione:

-   Per qualsiasi installazione, è disponibile un livello di installazione definito, che è un valore integrale compreso tra 1 e 32.767. Il valore iniziale è determinato dalla [**Proprietà INSTALLLEVEL**](installlevel.md), impostata nella [tabella delle proprietà](property-table.md).
-   Una funzionalità viene installata solo se il valore del livello di funzionalità è minore o uguale al livello di installazione corrente. L'interfaccia utente può essere creata in modo che, al momento dell'inizializzazione dell'installazione, il programma di installazione consenta all'utente di modificare il livello di installazione di qualsiasi funzionalità nella tabella delle funzionalità. Un autore, ad esempio, può definire i valori del livello di installazione che rappresentano opzioni di installazione specifiche, ad esempio **personalizzato**, **tipico** o **minimo**, quindi creare una finestra di dialogo che usa [SetInstallLevel ControlEvents](setinstalllevel-controlevent.md) per consentire all'utente di selezionare uno di questi Stati.
-   A seconda dello stato selezionato dall'utente, la finestra di dialogo Imposta la proprietà livello di installazione sul valore corrispondente. Se l'autore assegna un livello **tipico** di 100 e l'utente seleziona **tipico**, vengono installate solo le funzionalità con un livello di 100 o inferiore. Inoltre, l'opzione **personalizzata** potrebbe causare un'altra finestra di dialogo che contiene un [controllo SelectionTree](selectiontree-control.md). Il controllo SelectionTree consente quindi all'utente di modificare singolarmente se ogni funzionalità è installata o meno.

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

 

 




