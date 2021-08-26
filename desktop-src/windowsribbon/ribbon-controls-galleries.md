---
title: Uso delle raccolte
description: Il framework Windows ribbon offre agli sviluppatori un modello affidabile e coerente per la gestione del contenuto dinamico in un'ampia gamma di controlli basati su raccolta.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows Barra multifunzione, raccolte
- Barra multifunzione, raccolte
- Windows Barra multifunzione, controllo DropDownGallery
- Barra multifunzione, controllo DropDownGallery
- Windows Barra multifunzione, controllo SplitButtonGallery
- Barra multifunzione, controllo SplitButtonGallery
- Controllo DropDownGallery
- Controllo SplitButtonGallery
- raccolte per la barra multifunzione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce142c1159d7a7c4129f402716ed7e394ebb4829f043d7c58dd23221b1479720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933447"
---
# <a name="working-with-galleries"></a>Uso delle raccolte

Il framework Windows ribbon offre agli sviluppatori un modello affidabile e coerente per la gestione del contenuto dinamico in un'ampia gamma di controlli basati su raccolta. Adattando e riconfigurando l'interfaccia utente della barra multifunzione, questi controlli dinamici consentono al framework di rispondere all'interazione dell'utente sia nell'applicazione host che nella barra multifunzione stessa e offrono la flessibilità necessaria per gestire vari ambienti di run-time.

-   [Introduzione](#introduction)
-   [Raccolte](#working-with-galleries)
    -   [Raccolte di elementi](#item-galleries)
    -   [Raccolte di comandi](#command-galleries)
    -   [Controlli della raccolta](#working-with-galleries)
-   [Come implementare una raccolta](#how-to-implement-a-gallery)
    -   [Componenti di base](#the-basic-components)
    -   [Dichiarare i controlli nel markup](#declare-the-controls-in-markup)
    -   [Creare un gestore comandi](#create-a-command-handler)
    -   [Associare il gestore comandi](#bind-the-command-handler)
    -   [Inizializzare una raccolta](#initialize-a-collection)
    -   [Gestire gli eventi di raccolta](#handle-collection-events)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Questa capacità del framework della barra multifunzione di adattarsi in modo dinamico alle condizioni di esecuzione, ai requisiti dell'applicazione e all'input dell'utente finale evidenzia le funzionalità avanzate dell'interfaccia utente del framework e offre agli sviluppatori la flessibilità necessaria per soddisfare un'ampia gamma di esigenze dei clienti.

L'obiettivo di questa guida è descrivere i controlli della raccolta dinamica supportati dal framework, illustrarne le differenze, illustrare quando e dove possono essere usati al meglio e illustrare come possono essere incorporati in un'applicazione barra multifunzione.

## <a name="galleries"></a>Raccolte

Le raccolte sono controlli casella di riepilogo dal punto di vista funzionale e grafico. La raccolta di elementi di una raccolta può essere organizzata per categorie, visualizzate in layout flessibili basati su colonne e righe, rappresentate con immagini e testo e, a seconda del tipo di raccolta, supportano l'anteprima live.

Le raccolte sono funzionalmente distinte dagli altri controlli dinamici della barra multifunzione per i motivi seguenti:

-   Le raccolte implementano [**l'interfaccia IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) che definisce i vari metodi per la modifica delle raccolte di elementi della raccolta.
-   Le raccolte possono essere aggiornate in fase di esecuzione, in base all'attività che si verifica direttamente nella barra multifunzione, ad esempio quando un utente aggiunge un comando alla barra di accesso rapido.
-   Le raccolte possono essere aggiornate in fase di esecuzione, in base all'attività che si verifica indirettamente dall'ambiente di esecuzione, ad esempio quando un driver della stampante supporta solo layout di pagina verticale.
-   Le raccolte possono essere aggiornate in fase di esecuzione, in base all'attività che si verifica indirettamente nell'applicazione host, ad esempio quando un utente seleziona un elemento in un documento.

Il framework della barra multifunzione espone due tipi di raccolte: raccolte di elementi e raccolte di comandi.

### <a name="item-galleries"></a>Raccolte di elementi

Le raccolte di elementi contengono una raccolta basata su indice di elementi correlati in cui ogni elemento è rappresentato da un'immagine, una stringa o entrambi. Il controllo è associato a un singolo gestore command che si basa sul valore di indice identificato dalla proprietà [ \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) dell'interfaccia utente.

Le raccolte di elementi supportano l'anteprima dinamica, ovvero la visualizzazione di un risultato del comando, in base al passaggio del mouse o dello stato attivo, senza eseguire il commit o richiamare effettivamente il comando.

> [!IMPORTANT]
> Il framework non supporta l'hosting di raccolte di elementi nel menu dell'applicazione.

 

### <a name="command-galleries"></a>Raccolte di comandi

Le raccolte di comandi contengono una raccolta di elementi distinti non indicizzati. Ogni elemento è rappresentato da un singolo controllo associato a un gestore command tramite un ID comando. Analogamente ai controlli autonomi, ogni elemento in una raccolta di comandi indirizza gli eventi di input a un gestore command associato. La raccolta comandi stessa non è in ascolto degli eventi.

Le raccolte di comandi non supportano l'anteprima live.

### <a name="gallery-controls"></a>Controlli della raccolta

Nel framework della barra multifunzione sono disponibili quattro controlli della raccolta: [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)e [**ComboBox**](windowsribbon-element-combobox.md). Tutti, ad **eccezione di ComboBox,** possono essere implementati come raccolta di elementi o raccolta di comandi.

### <a name="dropdowngallery"></a>DropDownGallery

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) è un pulsante che visualizza un elenco a discesa contenente una raccolta di elementi o comandi che si escludono a vicenda.

La schermata seguente illustra il controllo [Raccolta](windowsribbon-controls-dropdowngallery.md) a discesa della barra multifunzione in Microsoft Paint per Windows 7.

![Screenshot di un controllo raccolta a discesa in Microsoft Paint per Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>SplitButtonGallery

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) è un controllo composito che espone un singolo elemento predefinito o command dalla raccolta in un pulsante primario e visualizza altri elementi o comandi in un elenco a discesa che si escludono a vicenda che viene visualizzato quando si fa clic su un pulsante secondario.

La schermata seguente illustra il controllo [Raccolta](windowsribbon-controls-splitbuttongallery.md) pulsanti di divisione della barra multifunzione in Microsoft Paint per Windows 7.

![Screenshot di un controllo della raccolta di pulsanti di divisione in Microsoft Paint per Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>InRibbonGallery

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md) è una raccolta che visualizza una raccolta di elementi o comandi correlati nella barra multifunzione. Se nella raccolta sono presenti troppi elementi, viene fornita una freccia di espansione per visualizzare il resto della raccolta in un riquadro espanso.

La schermata seguente illustra il controllo Raccolta barra multifunzione [in](windowsribbon-controls-inribbongallery.md) Microsoft Paint per Windows 7.

![Screenshot di un controllo della raccolta nella barra multifunzione di Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a>ComboBox

Un [**controllo ComboBox**](windowsribbon-element-combobox.md) è una casella di riepilogo a colonna singola che contiene una raccolta di elementi con un controllo statico o un controllo di modifica e una freccia a discesa. La parte della casella di riepilogo del controllo viene visualizzata quando l'utente fa clic sulla freccia a discesa.

La schermata seguente illustra un controllo Casella [combinata](windowsribbon-controls-combobox.md) della barra multifunzione Windows Live Movie Maker.

![Screenshot di un controllo casella combinata nella barra multifunzione di Microsoft Paint.](images/controls/combobox.png)

Poiché [**ComboBox è**](windowsribbon-element-combobox.md) esclusivamente una raccolta di elementi, non supporta gli elementi Command. È anche l'unico controllo della raccolta che non supporta uno spazio dei comandi. Uno spazio dei comandi è una raccolta di comandi dichiarati nel markup ed elencati nella parte inferiore di una raccolta di elementi o di una raccolta di comandi.

Nell'esempio di codice seguente viene illustrato il markup necessario per dichiarare uno spazio dei comandi a tre pulsanti in [**un controllo DropDownGallery.**](windowsribbon-element-dropdowngallery.md)


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



La schermata seguente illustra lo spazio dei comandi a tre pulsanti dell'esempio di codice precedente.

![Screenshot di uno spazio dei comandi a tre pulsanti in un elenco a discesa.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Come implementare una raccolta

Questa sezione illustra i dettagli di implementazione delle raccolte della barra multifunzione e illustra come incorporarle in un'applicazione barra multifunzione.

### <a name="the-basic-components"></a>Componenti di base

Questa sezione descrive il set di proprietà e metodi che formano la colonna portante del contenuto dinamico nel framework della barra multifunzione e supportano l'aggiunta, l'eliminazione, l'aggiornamento e la modifica del contenuto e del layout visivo delle raccolte della barra multifunzione in fase di esecuzione.

### <a name="iuicollection"></a>IUICollection

Le raccolte richiedono un set di metodi di base per accedere e modificare i singoli elementi nelle raccolte.

[L'interfaccia IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) definisce questi metodi e il framework integra le funzionalità con metodi aggiuntivi definiti nell'interfaccia [**IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) **IUICollection viene** implementato dal framework per ogni dichiarazione della raccolta nel markup della barra multifunzione.

Se sono necessarie funzionalità aggiuntive non fornite dall'interfaccia [**IUICollection,**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) un oggetto raccolta personalizzato implementato dall'applicazione host e derivato da [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) può essere sostituito con la raccolta del framework.

### <a name="iuicollectionchangedevent"></a>IUICollectionChangedEvent

Perché un'applicazione risponda alle modifiche in una raccolta di raccolta, deve implementare [**l'interfaccia IUICollectionChangedEvent.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) Le applicazioni possono sottoscrivere le notifiche [**da un oggetto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite il listener di [**eventi IUICollectionChangedEvent::OnChanged.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged)

Quando l'applicazione sostituisce la raccolta fornita dal framework con una raccolta personalizzata, l'applicazione deve implementare [l'interfaccia IConnectionPointContainer.](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) Se [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) non è implementato, l'applicazione non è in grado di notificare al framework le modifiche nella raccolta personalizzata che richiedono aggiornamenti dinamici al controllo raccolta.

Nei casi in cui [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) non è implementato, il controllo della raccolta può essere aggiornato solo tramite [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) e [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)o chiamando [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).

### <a name="iuisimplepropertyset"></a>IUISimplePropertySet

Le applicazioni devono implementare IUISimplePropertySet per ogni elemento o comando in una raccolta. Tuttavia, le proprietà che possono essere richieste con [**IUISimplePropertySet::GetValue variano.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)

Gli elementi vengono definiti e associati a una raccolta tramite la chiave della proprietà [ \_ \_ ItemsSource PKEY dell'interfaccia](windowsribbon-reference-properties-uipkey-itemssource.md) utente ed espongono le proprietà con un [**oggetto IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Le proprietà valide per gli elementi nelle raccolte di elementi ([**UI \_ COMMANDTYPE \_ COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) sono descritte nella tabella seguente.

> [!Note]  
> Alcune proprietà dell'elemento, ad [esempio \_ L'etichetta PKEY \_ dell'interfaccia](windowsribbon-reference-properties-uipkey-label.md)utente, possono essere definite nel markup. Per altre informazioni, vedere la documentazione [di riferimento sulle chiavi](windowsribbon-reference-properties.md) di proprietà.

 



Control

Proprietà

[**ComboBox**](windowsribbon-element-combobox.md)

[Interfaccia utente \_ Etichetta \_ PKEY,](windowsribbon-reference-properties-uipkey-label.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)

[Interfaccia utente \_ Etichetta \_ PKEY,](windowsribbon-reference-properties-uipkey-label.md) [UI \_ PKEY \_ ItemImage,](windowsribbon-reference-properties-uipkey-itemimage.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)

[Interfaccia utente \_ Etichetta \_ PKEY,](windowsribbon-reference-properties-uipkey-label.md) [UI \_ PKEY \_ ItemImage,](windowsribbon-reference-properties-uipkey-itemimage.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)

[Interfaccia utente \_ Etichetta \_ PKEY,](windowsribbon-reference-properties-uipkey-label.md) [UI \_ PKEY \_ ItemImage,](windowsribbon-reference-properties-uipkey-itemimage.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)

[Interfaccia utente \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) è una proprietà della raccolta di elementi.



 

Le proprietà dell'elemento valide per le raccolte Command ([**UI \_ COMMANDTYPE \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) sono descritte nella tabella seguente.



| Control                                                                | Proprietà                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       | [Interfaccia utente \_ PKEY \_ CommandId,](windowsribbon-reference-properties-uipkey-commandid.md) [UI \_ PKEY \_ CommandType,](windowsribbon-reference-properties-uipkey-commandtype.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       | [Interfaccia utente \_ PKEY \_ CommandId,](windowsribbon-reference-properties-uipkey-commandid.md) [UI \_ PKEY \_ CommandType,](windowsribbon-reference-properties-uipkey-commandtype.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) | [Interfaccia utente \_ PKEY \_ CommandId,](windowsribbon-reference-properties-uipkey-commandid.md) [UI \_ PKEY \_ CommandType,](windowsribbon-reference-properties-uipkey-commandtype.md) [UI \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

Le categorie vengono usate per organizzare gli elementi e i comandi nelle raccolte. Le categorie vengono definite e associate a una raccolta tramite la chiave della proprietà [Ui \_ PKEY \_ Categories](windowsribbon-reference-properties-uipkey-categories.md) ed espongono le proprietà con un oggetto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) specifico della categoria.

Le categorie non hanno commandtype e non supportano l'interazione dell'utente. Ad esempio, le categorie non possono diventare SelectedItem in una raccolta di elementi e non sono associate a un comando in una raccolta di comandi. Analogamente ad altre proprietà dell'elemento della raccolta, le proprietà di categoria, ad esempio [l'etichetta \_ PKEY \_](windowsribbon-reference-properties-uipkey-label.md) dell'interfaccia utente e [l'ID categoria \_ PKEY \_](windowsribbon-reference-properties-uipkey-categoryid.md) dell'interfaccia utente, possono essere recuperate chiamando [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).

> [!IMPORTANT]
> [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) deve restituire [**UI \_ COLLECTION \_ INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) quando l'interfaccia utente [ \_ PKEY \_ CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) viene richiesta per un elemento a cui non è associata una categoria.

 

### <a name="declare-the-controls-in-markup"></a>Dichiarare i controlli nel markup

Le raccolte, come tutti i controlli barra multifunzione, devono essere dichiarate nel markup. Una raccolta viene identificata nel markup come raccolta di elementi o raccolta di comandi e vengono dichiarati vari dettagli della presentazione. A differenza di altri controlli, le raccolte richiedono che solo il controllo di base, o contenitore di raccolta, sia dichiarato nel markup. Le raccolte effettive vengono popolate in fase di esecuzione. Quando una raccolta viene dichiarata nel markup, *l'attributo Type* viene usato per specificare se la raccolta è una raccolta di elementi di una raccolta di comandi.

Per ognuno dei controlli illustrati di seguito sono disponibili diversi attributi di layout facoltativi. Questi attributi forniscono preferenze per gli sviluppatori da seguire per il framework che influiscono direttamente sul modo in cui un controllo viene popolato e visualizzato in una barra multifunzione. Le preferenze applicabili nel markup sono correlate ai modelli di visualizzazione e layout e ai comportamenti descritti in Personalizzazione di una barra multifunzione tramite definizioni [di dimensioni e criteri di ridimensionamento](windowsribbon-templates.md).

Se un determinato controllo non consente preferenze di layout direttamente nel markup o non vengono specificate, il framework definisce convenzioni di visualizzazione specifiche del controllo in base alla quantità di spazio disponibile sullo schermo.

Gli esempi seguenti illustrano come incorporare un set di raccolte in una barra multifunzione.

### <a name="command-declarations"></a>Dichiarazioni di comando

I comandi devono essere dichiarati con un *attributo CommandName* usato per associare un controllo o un set di controlli al comando .

Qui è possibile specificare anche un attributo *CommandId* usato per associare un oggetto Command a un gestore command quando il markup viene compilato. Se non viene specificato alcun ID, ne viene generato uno dal framework.


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

Questa sezione contiene esempi che illustrano il markup di controllo di base necessario per i vari tipi di raccolta. Illustrano come dichiarare i controlli della raccolta e associarli a un oggetto Command tramite *l'attributo CommandName.*

Nell'esempio seguente viene illustrata una dichiarazione di controllo [**per DropDownGallery**](windowsribbon-element-dropdowngallery.md) in cui viene usato l'attributo *Type* per specificare che si tratta di una raccolta di comandi.


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



Nell'esempio seguente viene illustrata una dichiarazione di controllo [**per SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).


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



Nell'esempio seguente viene illustrata una dichiarazione di controllo [**per InRibbonGallery**](windowsribbon-element-inribbongallery.md).

> [!Note]  
> Poiché [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) è progettato per visualizzare un subset della raccolta di elementi nella barra multifunzione senza attivare un menu a discesa, fornisce una serie di attributi facoltativi che ne regolano le dimensioni e il layout degli elementi durante l'inizializzazione della barra multifunzione. Questi attributi sono univoci per **InRibbonGallery** e non sono disponibili dagli altri controlli dinamici.

 


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



### <a name="create-a-command-handler"></a>Creare un gestore comandi

Per ogni comando, il framework della barra multifunzione richiede un gestore command corrispondente nell'applicazione host. I gestori dei comandi vengono implementati dall'applicazione host della barra multifunzione e derivano [**dall'interfaccia IUICommandHandler.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)

> [!Note]  
> Più comandi possono essere associati a un singolo gestore di comandi.

 

Un gestore comandi ha due scopi:

-   [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) risponde alle richieste di aggiornamento delle proprietà. I valori delle proprietà Command, ad esempio [UI \_ PKEY \_ Enabled](windowsribbon-reference-properties-uipkey-enabled.md) o [UI \_ PKEY \_ Label,](windowsribbon-reference-properties-uipkey-label.md)vengono impostati tramite chiamate a [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) o [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).
-   [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) risponde all'esecuzione di eventi. Questo metodo supporta i tre stati di esecuzione seguenti specificati dal parametro [**\_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) dell'interfaccia utente.
    -   Lo stato Execute esegue o esegue il commit di tutti i comandi a cui è associato il gestore.
    -   Lo stato Anteprima visualizza in anteprima tutti i comandi a cui è associato il gestore. In questo modo vengono essenzialmente eseguiti i comandi senza eseguire il commit nel risultato.
    -   Lo stato CancelPreview annulla tutti i comandi in anteprima. Questa operazione è necessaria per supportare l'attraversamento attraverso un menu o un elenco e visualizzare in anteprima in sequenza e annullare i risultati in base alle esigenze.

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



### <a name="bind-the-command-handler"></a>Associare il gestore comandi

Dopo aver definito un gestore command, il comando deve essere associato al gestore.

L'esempio seguente illustra come associare un oggetto Command della raccolta a un gestore command specifico. In questo caso, entrambi i [**controlli ComboBox**](windowsribbon-element-combobox.md) e gallery sono associati ai rispettivi gestori Command.


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

L'esempio seguente illustra un'implementazione personalizzata [**di IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) per raccolte di elementi e comandi.

La classe CItemProperties in questo esempio è derivata da [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset). Oltre al metodo [**obbligatorio IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), la classe CItemProperties implementa un set di funzioni helper per l'inizializzazione e il rilevamento degli indici.


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



### <a name="handle-collection-events"></a>Gestire gli eventi di raccolta

L'esempio seguente illustra un'implementazione di IUICollectionChangedEvent.


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

[Proprietà raccolta](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Creazione di un'applicazione barra multifunzione](windowsribbon-stepbystep.md)
</dt> <dt>

[Informazioni su comandi e controlli](windowsribbon-commandscontrols.md)
</dt> <dt>

[Linee guida per l'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Esempio di raccolta](windowsribbon-gallerysample.md)
</dt> </dl>

 

 