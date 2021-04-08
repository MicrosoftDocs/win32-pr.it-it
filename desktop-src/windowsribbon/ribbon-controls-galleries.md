---
title: Uso delle raccolte
description: Il Framework della barra multifunzione di Windows offre agli sviluppatori un modello affidabile e coerente per la gestione di contenuto dinamico in diversi controlli basati su raccolte.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Barra multifunzione di Windows, raccolte
- Barra multifunzione, raccolte
- Barra multifunzione di Windows, controllo DropDownGallery
- Barra multifunzione, controllo DropDownGallery
- Barra multifunzione di Windows, controllo SplitButtonGallery
- Barra multifunzione, controllo SplitButtonGallery
- Controllo DropDownGallery
- Controllo SplitButtonGallery
- raccolte per la barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729231"
---
# <a name="working-with-galleries"></a>Uso delle raccolte

Il Framework della barra multifunzione di Windows offre agli sviluppatori un modello affidabile e coerente per la gestione di contenuto dinamico in diversi controlli basati su raccolte. Grazie all'adattamento e alla riconfigurazione dell'interfaccia utente della barra multifunzione, questi controlli dinamici consentono al Framework di rispondere all'interazione dell'utente sia nell'applicazione host che nella barra multifunzione e offrono la flessibilità necessaria per gestire diversi ambienti di Runtime.

-   [Introduzione](#introduction)
-   [Raccolte](#working-with-galleries)
    -   [Raccolte di elementi](#item-galleries)
    -   [Raccolte comandi](#command-galleries)
    -   [Controlli della raccolta](#working-with-galleries)
-   [Come implementare una raccolta](#how-to-implement-a-gallery)
    -   [Componenti di base](#the-basic-components)
    -   [Dichiarare i controlli nel markup](#declare-the-controls-in-markup)
    -   [Creazione di un gestore di comandi](#create-a-command-handler)
    -   [Associare il gestore di comandi](#bind-the-command-handler)
    -   [Inizializzare una raccolta](#initialize-a-collection)
    -   [Gestisci eventi raccolta](#handle-collection-events)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Questa capacità del Framework della barra multifunzione di adattarsi dinamicamente alle condizioni di runtime, ai requisiti delle applicazioni e all'input dell'utente finale evidenzia le funzionalità avanzate dell'interfaccia utente del Framework e offre agli sviluppatori la flessibilità necessaria per soddisfare un'ampia gamma di esigenze dei clienti.

Questa guida descrive i controlli della raccolta dinamica supportati dal Framework, ne spiega le differenze, discute quando e dove possono essere usati meglio e illustra come possono essere incorporati in un'applicazione Ribbon.

## <a name="galleries"></a>Raccolte

Le raccolte sono controlli casella di riepilogo funzionalmente e graficamente avanzati. La raccolta di elementi di una raccolta può essere organizzata in base a categorie, visualizzate in layout flessibili basati su righe e colonne, rappresentate con immagini e testo e a seconda del tipo di raccolta, supporta l'anteprima in tempo reale.

Le raccolte sono separate dal punto di vista funzionale da altri controlli della barra multifunzione dinamici per i motivi seguenti:

-   Le raccolte implementano l'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) che definisce i vari metodi per la modifica delle raccolte di elementi della raccolta.
-   Le raccolte possono essere aggiornate in fase di esecuzione, in base alle attività che si verificano direttamente nella barra multifunzione, ad esempio quando un utente aggiunge un comando alla barra di accesso rapido (QAT).
-   Le raccolte possono essere aggiornate in fase di esecuzione, in base all'attività che si verifica indirettamente dall'ambiente di runtime, ad esempio quando un driver della stampante supporta solo layout di pagine verticale.
-   Le raccolte possono essere aggiornate in fase di esecuzione, in base all'attività che si verifica indirettamente nell'applicazione host, ad esempio quando un utente seleziona un elemento in un documento.

Il Framework della barra multifunzione espone due tipi di raccolte: raccolte di elementi e raccolte di comandi.

### <a name="item-galleries"></a>Raccolte di elementi

Le raccolte di elementi contengono una raccolta basata su indici di elementi correlati in cui ogni elemento è rappresentato da un'immagine, da una stringa o da entrambi. Il controllo è associato a un singolo gestore di comando che si basa sul valore di indice identificato dalla proprietà [ \_ \_ SelectedItem pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-selecteditem.md) .

Le raccolte di elementi supportano l'anteprima in tempo reale, ovvero la visualizzazione del risultato di un comando, in base al passaggio del mouse o allo stato attivo, senza eseguire il commit o richiamare effettivamente il comando.

> [!IMPORTANT]
> Il Framework non supporta l'hosting di raccolte di elementi nel menu dell'applicazione.

 

### <a name="command-galleries"></a>Raccolte comandi

Le raccolte di comandi contengono una raccolta di elementi distinti e non indicizzati. Ogni elemento è rappresentato da un singolo controllo associato a un gestore di comandi tramite un ID di comando. Analogamente ai controlli autonomi, ogni elemento in una raccolta di comandi indirizza gli eventi di input a un gestore di comandi associato: la raccolta di comandi non è in ascolto degli eventi.

Le raccolte comandi non supportano l'anteprima in tempo reale.

### <a name="gallery-controls"></a>Controlli della raccolta

Sono disponibili quattro controlli della raccolta nel framework della barra multifunzione: [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), [**inribbongallery**](windowsribbon-element-inribbongallery.md)e [**ComboBox**](windowsribbon-element-combobox.md). All eccetto **ComboBox** può essere implementato come raccolta di elementi o come raccolta di comandi.

### <a name="dropdowngallery"></a>DropDownGallery

Un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) è un pulsante che visualizza un elenco a discesa che contiene una raccolta di elementi o comandi che si escludono a vicenda.

Lo screenshot seguente illustra il controllo raccolta a [discesa](windowsribbon-controls-dropdowngallery.md) della barra multifunzione in Microsoft Paint per Windows 7.

![Screenshot di un controllo raccolta a discesa in Microsoft Paint per Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>SplitButtonGallery

Un [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) è un controllo composito che espone un singolo elemento o comando predefinito dalla raccolta in un pulsante principale e visualizza altri elementi o comandi in un elenco a discesa che viene escluso a vicenda quando si fa clic su un pulsante secondario.

Lo screenshot seguente illustra il controllo raccolta dei [pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md) della barra multifunzione in Microsoft Paint per Windows 7.

![Screenshot di un controllo raccolta di pulsanti di suddivisione in Microsoft Paint per Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>Inribbongallery

Un [**inribbongallery**](windowsribbon-element-inribbongallery.md) è una raccolta che visualizza una raccolta di elementi o comandi correlati nella barra multifunzione. Se la raccolta contiene troppi elementi, viene fornita una freccia di espansione per visualizzare il resto della raccolta in un riquadro espanso.

Lo screenshot seguente illustra il controllo della raccolta della barra [multifunzione](windowsribbon-controls-inribbongallery.md) in Microsoft Paint per Windows 7.

![Screenshot di un controllo della raccolta nella barra multifunzione nella barra multifunzione di Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a>ComboBox

[**ComboBox**](windowsribbon-element-combobox.md) è una casella di riepilogo a colonna singola che contiene una raccolta di elementi con un controllo statico o un controllo di modifica e una freccia a discesa. La parte della casella di riepilogo del controllo viene visualizzata quando l'utente fa clic sulla freccia a discesa.

Lo screenshot seguente illustra un controllo [casella combinata](windowsribbon-controls-combobox.md) della barra multifunzione di Windows Live Movie Maker.

![Screenshot di un controllo ComboBox sulla barra multifunzione di Microsoft Paint.](images/controls/combobox.png)

Poiché [**ComboBox**](windowsribbon-element-combobox.md) è esclusivamente una raccolta di elementi, non supporta gli elementi di comando. È anche l'unico controllo raccolta che non supporta uno spazio dei comandi. Uno spazio di comando è una raccolta di comandi dichiarati nel markup ed elencati nella parte inferiore di una raccolta di elementi o di una raccolta di comandi.

Nell'esempio di codice seguente viene illustrato il markup necessario per dichiarare uno spazio dei comandi a tre pulsanti in un [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



Lo screenshot seguente illustra lo spazio dei comandi a tre pulsanti dell'esempio di codice precedente.

![Screenshot di uno spazio dei comandi a tre pulsanti in un dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Come implementare una raccolta

In questa sezione vengono illustrati i dettagli di implementazione delle raccolte della barra multifunzione e viene illustrato come incorporarli in un'applicazione Ribbon.

### <a name="the-basic-components"></a>Componenti di base

In questa sezione viene descritto il set di proprietà e metodi che costituiscono la struttura di contenuto dinamico nel framework della barra multifunzione e il supporto per l'aggiunta, l'eliminazione, l'aggiornamento e la modifica del contenuto e il layout visivo delle raccolte della barra multifunzione in fase di esecuzione.

### <a name="iuicollection"></a>IUICollection

Le raccolte richiedono un set di base di metodi per accedere e modificare i singoli elementi nelle raccolte.

L'interfaccia [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) definisce questi metodi e il Framework integra le funzionalità con metodi aggiuntivi definiti nell'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . **IUICollection** viene implementato dal Framework per ogni dichiarazione della raccolta nel markup della barra multifunzione.

Se è necessaria una funzionalità aggiuntiva non fornita dall'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , è possibile sostituire un oggetto raccolta personalizzato implementato dall'applicazione host e derivato da [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) per la raccolta di Framework.

### <a name="iuicollectionchangedevent"></a>IUICollectionChangedEvent

Affinché un'applicazione risponda alle modifiche in una raccolta di raccolta, deve implementare l'interfaccia [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) . Le applicazioni possono sottoscrivere le notifiche da un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite il listener di eventi [**IUICollectionChangedEvent:: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .

Quando l'applicazione sostituisce la raccolta di raccolta fornita dal Framework con una raccolta personalizzata, l'applicazione deve implementare l'interfaccia [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) . Se [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) non è implementato, l'applicazione non è in grado di notificare al Framework le modifiche apportate alla raccolta personalizzata che richiedono aggiornamenti dinamici per il controllo raccolta.

Nei casi in cui [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) non è implementato, il controllo raccolta può essere aggiornato solo tramite invalidazione tramite [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) e [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)oppure chiamando [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).

### <a name="iuisimplepropertyset"></a>IUISimplePropertySet

Le applicazioni devono implementare IUISimplePropertySet per ogni elemento o comando in una raccolta di raccolta. Tuttavia, le proprietà che possono essere richieste con [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) variano.

Gli elementi vengono definiti e associati a una raccolta tramite la chiave della proprietà [ \_ \_ ItemsSource dell'interfaccia utente pkey](windowsribbon-reference-properties-uipkey-itemssource.md) ed espongono le proprietà con un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Nella tabella seguente sono descritte le proprietà valide per gli elementi nelle raccolte di elementi ([**\_ \_ raccolta COMMANDTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)).

> [!Note]  
> Alcune proprietà dell'elemento, ad esempio l' [ \_ \_ etichetta pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md), possono essere definite nel markup. Per informazioni dettagliate, vedere la documentazione di riferimento per le [chiavi di proprietà](windowsribbon-reference-properties.md) .

 



Control

Proprietà

[**ComboBox**](windowsribbon-element-combobox.md)

[Interfaccia utente \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)

[Interfaccia utente \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**Inribbongallery**](windowsribbon-element-inribbongallery.md)

[Interfaccia utente \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)

[Interfaccia utente \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md), [UI \_ pkey \_ ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[Interfaccia utente \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) è una proprietà della raccolta di elementi.



 

Nella tabella seguente sono descritte le proprietà degli elementi valide per le raccolte di comandi ([**UI \_ COMMANDTYPE \_ CommandCollection**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)).



| Control                                                                | Proprietà                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       | [Interfaccia utente \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**Inribbongallery**](windowsribbon-element-inribbongallery.md)       | [Interfaccia utente \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) | [Interfaccia utente \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

Le categorie vengono usate per organizzare gli elementi e i comandi nelle raccolte. Le categorie vengono definite e associate a una raccolta tramite la chiave della proprietà [ \_ \_ categorie pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-categories.md) ed espongono le proprietà con un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) specifico per la categoria.

Le categorie non hanno un CommandType e non supportano l'interazione dell'utente. Le categorie, ad esempio, non possono diventare SelectedItem in una raccolta di elementi e non sono associate a un comando in una raccolta di comandi. Analogamente ad altre proprietà degli elementi della raccolta, è possibile recuperare le proprietà di categoria, ad esempio [UI \_ pkey \_ Label](windowsribbon-reference-properties-uipkey-label.md) e [UI \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) , chiamando [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).

> [!IMPORTANT]
> [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) deve restituire [**la \_ raccolta \_ di interfaccia utente INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) quando è richiesto l' [interfaccia utente \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) per un elemento a cui non è associata una categoria.

 

### <a name="declare-the-controls-in-markup"></a>Dichiarare i controlli nel markup

Le raccolte, come tutti i controlli della barra multifunzione, devono essere dichiarate nel markup. Una raccolta viene identificata nel markup come raccolta di elementi o raccolta di comandi e vengono dichiarati diversi dettagli di presentazione. A differenza di altri controlli, le raccolte richiedono che il controllo di base o il contenitore della raccolta vengano dichiarati nel markup. Le raccolte effettive vengono popolate in fase di esecuzione. Quando una raccolta viene dichiarata nel markup, l'attributo *Type* viene usato per specificare se la raccolta è una raccolta di elementi di una raccolta di comandi.

Sono disponibili diversi attributi di layout facoltativi per ognuno dei controlli descritti qui. Questi attributi forniscono preferenze per gli sviluppatori per il Framework da seguire che influiscono direttamente sulla modalità di popolamento e visualizzazione di un controllo in una barra multifunzione. Le preferenze applicabili al markup sono correlate ai modelli di visualizzazione e di layout e ai comportamenti descritti in [personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md).

Se un particolare controllo non consente le preferenze di layout direttamente nel markup oppure le preferenze di layout non sono specificate, il Framework definisce le convenzioni di visualizzazione specifiche del controllo in base alla quantità di spazio disponibile sullo schermo.

Gli esempi seguenti illustrano come incorporare un set di raccolte in una barra multifunzione.

### <a name="command-declarations"></a>Dichiarazioni di comando

I comandi devono essere dichiarati con un attributo *CommandName* usato per associare un controllo o un set di controlli con il comando.

Qui è anche possibile specificare un attributo *CommandID* usato per associare un comando a un gestore di comandi quando il markup viene compilato. Se non viene fornito alcun ID, ne viene generato uno dal Framework.


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a>Dichiarazioni di controllo

Questa sezione contiene esempi che illustrano il markup di base del controllo necessario per i vari tipi di raccolta. Illustrano come dichiarare i controlli della raccolta e associarli a un comando tramite l'attributo *CommandName* .

Nell'esempio seguente viene illustrata una dichiarazione di controllo per [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) in cui viene usato l'attributo *Type* per specificare che si tratta di una raccolta di comandi.


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



Nell'esempio seguente viene illustrata una dichiarazione di controllo per [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



Nell'esempio seguente viene illustrata una dichiarazione di controllo per l'oggetto [**inribbongallery**](windowsribbon-element-inribbongallery.md).

> [!Note]  
> Poiché l' [**inribbongallery**](windowsribbon-element-inribbongallery.md) è progettato per visualizzare un subset della relativa raccolta di elementi nella barra multifunzione senza attivare un menu a discesa, fornisce un numero di attributi facoltativi che ne regolano la dimensione e il layout dell'elemento nell'inizializzazione della barra multifunzione. Questi attributi sono univoci per gli **inribbongallery** e non sono disponibili dagli altri controlli dinamici.

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



Nell'esempio seguente viene illustrata una dichiarazione di controllo per [**ComboBox**](windowsribbon-element-combobox.md).


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>Creazione di un gestore di comandi

Per ogni comando, il Framework della barra multifunzione richiede un gestore di comando corrispondente nell'applicazione host. I gestori di comandi sono implementati dall'applicazione host della barra multifunzione e derivano dall'interfaccia [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .

> [!Note]  
> È possibile associare più comandi a un singolo gestore di comandi.

 

Un gestore di comando svolge due finalità:

-   [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) risponde alle richieste di aggiornamento delle proprietà. I valori delle proprietà del comando, ad esempio [interfaccia utente \_ pkey \_ abilitata](windowsribbon-reference-properties-uipkey-enabled.md) o [ \_ \_ etichetta pkey interfaccia utente](windowsribbon-reference-properties-uipkey-label.md), vengono impostati tramite chiamate a [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) o [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).
-   [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) risponde per eseguire gli eventi. Questo metodo supporta i tre stati di esecuzione seguenti specificati dal parametro [**\_ EXECUTIONVERB dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) .
    -   Lo stato Execute esegue o esegue il commit in tutti i comandi a cui è associato il gestore.
    -   Lo stato di anteprima Visualizza in anteprima tutti i comandi a cui è associato il gestore. Questa operazione esegue essenzialmente i comandi senza commit nel risultato.
    -   Lo stato CancelPreview Annulla tutti i comandi visualizzati in anteprima. Questa operazione è necessaria per supportare l'attraversamento tramite un menu o un elenco ed eseguire l'anteprima sequenziale e annullare i risultati secondo le esigenze.

Nell'esempio seguente viene illustrato un gestore di comandi della raccolta.


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a>Associare il gestore di comandi

Dopo aver definito un gestore di comandi, il comando deve essere associato al gestore.

Nell'esempio seguente viene illustrato come associare un comando della raccolta a un gestore di comandi specifico. In questo caso, entrambi i controlli [**ComboBox**](windowsribbon-element-combobox.md) e Gallery sono associati ai rispettivi gestori di comandi.


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a>Inizializzare una raccolta

Nell'esempio seguente viene illustrata un'implementazione personalizzata di [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per le raccolte di elementi e comandi.

La classe CItemProperties in questo esempio è derivata da [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset). Oltre al metodo [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)necessario, la classe CItemProperties implementa un set di funzioni di supporto per l'inizializzazione e il rilevamento degli indici.


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a>Gestisci eventi raccolta

Nell'esempio seguente viene illustrata un'implementazione di IUICollectionChangedEvent.


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà della raccolta](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Creazione di un'applicazione Ribbon](windowsribbon-stepbystep.md)
</dt> <dt>

[Informazioni sui comandi e sui controlli](windowsribbon-commandscontrols.md)
</dt> <dt>

[Linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Esempio di raccolta](windowsribbon-gallerysample.md)
</dt> </dl>

 

 