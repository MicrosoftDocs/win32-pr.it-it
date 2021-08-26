---
title: Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento
description: I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione di Windows e basate su una combinazione di comportamenti predefiniti e modelli di layout (sia definiti dal framework che personalizzati) come dichiarati nel markup della barra multifunzione. Queste regole definiscono i comportamenti di layout adattivi del framework della barra multifunzione che influenzano il modo in cui i controlli nella barra dei comandi si adattano alle varie dimensioni della barra multifunzione in fase di esecuzione.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows Barra multifunzione, personalizzazione
- Barra multifunzione, personalizzazione
- Windows Barra multifunzione, modelli SizeDefinition
- Barra multifunzione, modelli SizeDefinition
- Windows Barra multifunzione, modelli personalizzati
- Barra multifunzione, modelli personalizzati
- personalizzazione della Windows barra multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eff1a9d1b2582d5386ce6ea0e02e20cfb5a806e1aaa4a98529474a756b5a8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933796"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento

I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione di Windows e basate su una combinazione di comportamenti predefiniti e modelli di layout (sia definiti dal framework che personalizzati) come dichiarati nel markup della barra multifunzione. Queste regole definiscono i comportamenti di layout adattivi del framework della barra multifunzione che influenzano il modo in cui i controlli nella barra dei comandi si adattano alle varie dimensioni della barra multifunzione in fase di esecuzione.

-   [Introduzione](#introduction)
    -   [Modelli sizeDefinition della barra multifunzione](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Modelli personalizzati](#custom-templates)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il layout adattivo, come definito dal framework della barra multifunzione, è la possibilità di tutti i controlli all'interno dell'interfaccia utente della barra multifunzione di modificare dinamicamente l'organizzazione, le dimensioni, il formato e la scala relativa in base alle modifiche alle dimensioni della barra multifunzione in fase di esecuzione.

Il framework espone la funzionalità di layout adattivo tramite un set di elementi di markup dedicati alla specifica e alla personalizzazione di vari comportamenti di layout. Una raccolta di modelli, denominata [**SizeDefinitions,**](windowsribbon-element-sizedefinition.md)è definita dal framework, ognuno dei quali supporta vari scenari di controllo e layout. Tuttavia, il framework supporta anche modelli personalizzati se i modelli predefiniti non forniscono l'esperienza o i layout dell'interfaccia utente richiesti da un'applicazione.

Per visualizzare i controlli in un layout preferito con una determinata dimensione della barra multifunzione, sia i modelli predefiniti che i modelli personalizzati funzionano in combinazione con [**l'elemento ScalingPolicy.**](windowsribbon-element-scalingpolicy.md) Questo elemento contiene un manifesto delle preferenze di dimensione che il framework usa come guida per il rendering della barra multifunzione.

> [!Note]  
> Il framework della barra multifunzione fornisce comportamenti di layout predefiniti basati su un set di euristiche predefinite per l'organizzazione e la presentazione dei controlli in fase di esecuzione senza la necessità di modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefiniti. Tuttavia, questa funzionalità è destinata solo a scopo di prototipazione.

 

### <a name="ribbon-sizedefinition-templates"></a>Modelli sizedefinition della barra multifunzione

Il framework della barra multifunzione fornisce un set completo di [**modelli SizeDefinition**](windowsribbon-element-sizedefinition.md) che specificano le dimensioni e il comportamento del layout per [un gruppo](windowsribbon-controls-group.md) di controlli della barra multifunzione. Questi modelli riguardano gli scenari più comuni per l'organizzazione dei controlli in un'applicazione barra multifunzione.

Per applicare un'esperienza utente coerente tra le applicazioni della barra multifunzione, ogni modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impone restrizioni ai controlli o alla famiglia di controlli supportati.

Ad esempio, la famiglia di controlli button include:

-   [Button](windowsribbon-controls-button.md)
-   [Interruttore](windowsribbon-controls-togglebutton.md)
-   [Pulsante a discesa](windowsribbon-controls-dropdownbutton.md)
-   [Pulsante Dividi](windowsribbon-controls-splitbutton.md)
-   [Raccolta a discesa](windowsribbon-controls-dropdowngallery.md)
-   [Raccolta pulsanti di divisione](windowsribbon-controls-splitbuttongallery.md)
-   [Elenco a discesa Selezione colori](windowsribbon-controls-dropdowncolorpicker.md)

Mentre la famiglia di controlli di input include:

-   [ComboBox](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

[Check Box](windowsribbon-controls-checkbox.md) e [Raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) non appartengono alla famiglia di pulsanti o alla famiglia di input. Questi due controlli possono essere usati solo se indicati in modo esplicito in un [**modello SizeDefinition.**](windowsribbon-element-sizedefinition.md)

Di seguito è riportato un elenco dei [**modelli SizeDefinition**](windowsribbon-element-sizedefinition.md) con una descrizione del layout e dei controlli consentiti da ogni modello.

> [!IMPORTANT]
> Se i controlli dichiarati nel markup non vengono mappati esattamente al tipo [](windowsribbon-compilationerrors.md) di controllo, all'ordine e alla quantità definiti nel modello associato, viene registrato un errore di convalida dal compilatore [di markup](windowsribbon-intentcl.md) e la compilazione viene terminata.

 



OneButton

Un controllo famiglia di pulsanti.<br/> Sono supportate solo le dimensioni del gruppo large.<br/>

![immagine del modello onebutton sizedefinition.](images/overviews/sizedefinition-onebutton.png)

TwoButtons

Due controlli della famiglia di pulsanti.<br/> Sono supportate solo le dimensioni dei gruppi Large e Medium.<br/>

![immagine di un modello di definizione delle dimensioni di grandi dimensioni a due pulsanti.](images/overviews/sizedefinition-twobuttons-large.png)

![Immagine del modello twobuttons medium sizedefinition.](images/overviews/sizedefinition-twobuttons-medium.png)

ThreeButtons

Tre controlli della famiglia di pulsanti.<br/> Sono supportate solo le dimensioni dei gruppi Large e Medium.<br/>

![immagine del modello di definizione di dimensioni di grandi dimensioni a tre pulsanti.](images/overviews/sizedefinition-threebuttons-large.png)

![Immagine del modello di definizione a tre pulsanti di dimensioni medie.](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Tre controlli della famiglia di pulsanti.<br/> Il primo pulsante viene presentato in modo evidente in tutte e tre le dimensioni.<br/>

![immagine del modello threebuttons-onebigandtwosmall large sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![immagine del modello threebuttons-onebigandtwosmall medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![immagine del modello threebuttons-onebigandtwosmall small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

ThreeButtonsAndOneCheckBox

Tre controlli della famiglia di pulsanti accompagnati da un singolo controllo CheckBox.<br/> Sono supportate solo le dimensioni dei gruppi Large e Medium.<br/>

![immagine del modello threebuttonsandonecheckbox large sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![immagine del modello threebuttonsandonecheckbox medium sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

FourButtons

Quattro controlli della famiglia di pulsanti.<br/>

![immagine del modello di definizione delle dimensioni di grandi dimensioni a quattro pulsanti.](images/overviews/sizedefinition-fourbuttons-large.png)

![Immagine del modello fourbuttons medium sizedefinition.](images/overviews/sizedefinition-fourbuttons-medium.png)

![immagine del modello small sizedefinition a quattro pulsanti.](images/overviews/sizedefinition-fourbuttons-small.png)

FiveButtons

Cinque controlli della famiglia di pulsanti.<br/>

![Immagine di un modello di definizione delle dimensioni di dimensioni di cinque pulsanti.](images/overviews/sizedefinition-fivebuttons-large.png)

![Immagine del modello di definizione di dimensioni medie dei cinque pulsanti.](images/overviews/sizedefinition-fivebuttons-medium.png)

![Immagine di un modello di definizione di dimensioni ridotte a cinque pulsanti.](images/overviews/sizedefinition-fivebuttons-small.png)

FiveOrSixButtons

Cinque controlli della famiglia di pulsanti e un sesto pulsante facoltativo.<br/>

![immagine di fiveorsixbuttons large sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![immagine di fiveorsixbuttons medium sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![immagine di fiveorsixbuttons small sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

SixButtons

Sei controlli della famiglia di pulsanti.<br/>

![immagine del modello di definizione delle dimensioni large di sei pulsanti.](images/overviews/sizedefinition-sixbuttons-large.png)

![Immagine del modello sixbuttons medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-medium.png)

![Immagine del modello small sizedefinition a sei pulsanti.](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Sei controlli della famiglia di pulsanti (presentazione alternativa).<br/>

![immagine del modello di definizione delle dimensioni large sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![modello sixbuttons-twocolumns medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![immagine del modello small sizedefinition a sei pulsanti-due colonne.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

SevenButtons

Sette controlli della famiglia di pulsanti.<br/>

![immagine del modello di definizione delle dimensioni di dimensioni di sette pulsanti.](images/overviews/sizedefinition-sevenbuttons-large.png)

![immagine del modello sevenbuttons mediumsizedefinition.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![immagine del modello di definizione di dimensioni ridotte di sette pulsanti.](images/overviews/sizedefinition-sevenbuttons-small.png)

EightButtons

Otto controlli della famiglia di pulsanti.<br/>

![immagine di eightbuttons-lastthreesmall large sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![immagine di eightbuttons-lastthreesmall medium sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![immagine di eightbuttons-lastthreesmall small sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Otto controlli della famiglia di pulsanti (presentazione alternativa).<br/>

> [!Note]  
> Tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti in due elementi [**ControlGroup:**](windowsribbon-element-controlgroup.md) uno per i primi cinque elementi e uno per gli ultimi tre elementi.

<br/> Nell'esempio seguente viene illustrato il markup necessario per questo modello.<br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![Immagine di un modello di definizione delle dimensioni di grandi dimensioni a otto pulsanti.](images/overviews/sizedefinition-eightbuttons-large.png)

![Immagine del modello di definizione delle dimensioni medie degli otto pulsanti.](images/overviews/sizedefinition-eightbuttons-medium.png)

![immagine di otto pulsanti small sizedefinition modello.](images/overviews/sizedefinition-eightbuttons-small.png)

NineButtons

Nove controlli della famiglia di pulsanti.

![immagine del modello ninebuttons large sizedefinition.](images/overviews/sizedefinition-ninebuttons-large.png)

![Immagine del modello ninebuttons medium sizedefinition.](images/overviews/sizedefinition-ninebuttons-medium.png)

![Immagine del modello ninebuttons small sizedefinition.](images/overviews/sizedefinition-ninebuttons-small.png)

TenButtons

Dieci controlli della famiglia di pulsanti.

![Immagine del modello tenbuttons large sizedefinition.](images/overviews/sizedefinition-tenbuttons-large.png)

![Immagine del modello tenbuttons medium sizedefinition.](images/overviews/sizedefinition-tenbuttons-medium.png)

![Immagine del modello tenbuttons small sizedefinition.](images/overviews/sizedefinition-tenbuttons-small.png)

ElevenButtons

Undicesimo controllo della famiglia di pulsanti.

![Immagine di undicesimo modello sizedefinition di pulsanti di grandi dimensioni.](images/overviews/sizedefinition-elevenbuttons-large.png)

![Immagine di undicesimo modello di definizione delle dimensioni medie dei pulsanti.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![immagine di undicesimobuttons small sizedefinition template.](images/overviews/sizedefinition-elevenbuttons-small.png)

OneFontControl

Un [**oggetto FontControl.**](windowsribbon-element-fontcontrol.md)

Sono supportate solo le dimensioni dei gruppi Large e Medium.

> [!IMPORTANT]
> L'inclusione [**di un oggetto FontControl**](windowsribbon-element-fontcontrol.md) all'interno di una definizione di modello personalizzata non è supportata dal framework.

 

![immagine di un modello large sizedefinition di onefontcontrol.](images/overviews/sizedefinition-onefontcontrol-large.png)

![immagine di un modello di definizione delle dimensioni medie di unfontcontrol.](images/overviews/sizedefinition-onefontcontrol-medium.png)

OneInRibbonGallery

Un [**controllo InRibbonGallery.**](windowsribbon-element-inribbongallery.md)

Sono supportate solo le dimensioni dei gruppi Large e Small.

![immagine di un modello oneinribbongallery large sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![immagine di un modello oneinribbongallery small sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-small.png)

InRibbonGalleryAndBigButton

Un [**controllo InRibbonGallery**](windowsribbon-element-inribbongallery.md) e un controllo famiglia di pulsanti.

Sono supportate solo le dimensioni dei gruppi Large e Small.

![immagine del modello inribbongalleryandbigbutton large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![immagine del modello inribbongalleryandbigbutton small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Un [controllo Raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) e due o tre controlli della famiglia di pulsanti.

La raccolta viene compressa nella rappresentazione Popup nelle dimensioni dei gruppi Medio e Piccolo.

![immagine di inribbongalleryandbuttons-galleryscalesfirst large sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![immagine di inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![immagine di inribbongalleryandbuttons-galleryscalesfirst small sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

ButtonGroups

Una disposizione complessa di 32 controlli della famiglia di pulsanti (la maggior parte dei quali sono facoltativi).

> [!Note]  
> A parte il pulsante facoltativo a dimensione intera del modello ButtonGroups di grandi dimensioni, tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti negli [**elementi ControlGroup.**](windowsribbon-element-controlgroup.md)

 

L'esempio seguente illustra il markup necessario per visualizzare tutti e 32 gli elementi di controllo (obbligatori e facoltativi) con questo modello.


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![immagine del modello buttongroups large sizedefinition.](images/overviews/sizedefinition-buttongroups-large.png)

![Immagine del modello buttongroups medium sizedefinition.](images/overviews/sizedefinition-buttongroups-medium.png)

![Immagine del modello buttongroups small sizedefinition.](images/overviews/sizedefinition-buttongroups-small.png)

ButtonGroupsAndInputs

Due controlli della famiglia di input (il secondo è facoltativo) seguiti da una disposizione complessa di 29 controlli della famiglia di pulsanti (la maggior parte dei quali è facoltativa).

Sono supportate solo le dimensioni dei gruppi Large e Medium.

> [!Note]  
> Tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti negli [**elementi ControlGroup.**](windowsribbon-element-controlgroup.md)

 

L'esempio seguente illustra il markup necessario per visualizzare tutti gli elementi del controllo (obbligatori e facoltativi) con questo modello.


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![immagine di buttongroupsandinputs large sizedefinition template.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![immagine del modello buttongroupsandinputs medium sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

BigButtonsAndSmallButtonsOrInputs

Due controlli della famiglia di pulsanti (entrambi facoltativi) seguiti da due o tre pulsanti o controlli della famiglia di input.

Sono supportate solo le dimensioni dei gruppi Large e Medium.

![immagine di bigbuttonsandsmallbuttonsorinputs large sizedefinition template.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![immagine del modello bigbuttonsandsmallbuttonsorinputs medium sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Esempio di SizeDefinition di base

L'esempio di codice seguente fornisce una dimostrazione di base di come dichiarare un [**modello SizeDefinition**](windowsribbon-element-sizedefinition.md) nel markup della barra multifunzione.

*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) viene usato per questo particolare esempio, ma tutti i modelli di framework vengono specificati in modo simile.


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



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>Esempio di SizeDefinition complesso con criteri di ridimensionamento

Il comportamento di compressione dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) può essere controllato tramite l'uso di criteri di ridimensionamento nel markup della barra multifunzione.

[**L'elemento ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contiene un manifesto delle dichiarazioni [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e [**Scale**](windowsribbon-element-scale.md) che specificano le preferenze di layout adattivo per uno o più elementi [**Group**](windowsribbon-element-group.md) quando la barra multifunzione viene ridimensionata.

> [!Note]  
> È consigliabile che i dettagli dei criteri di ridimensionamento adeguati siano specificati in modo che la maggior parte degli elementi [**Group,**](windowsribbon-element-group.md) se non tutti, siano associati a un elemento [**Scale**](windowsribbon-element-scale.md) in cui l'attributo *Size* è uguale a `Popup` . In questo modo il framework può eseguire il rendering della barra multifunzione con le dimensioni più piccole possibili e supportare la più ampia gamma di dispositivi di visualizzazione, prima di introdurre automaticamente un meccanismo di scorrimento.

 

L'esempio di codice seguente illustra un manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) che specifica una preferenza [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una **scheda Home.** Inoltre, gli [**elementi Scale**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di dimensione decrescente, di ogni gruppo.


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a>Modelli personalizzati

Se i comportamenti di layout predefiniti e i modelli Predefiniti di [**SizeDefinition**](windowsribbon-element-sizedefinition.md) non offrono la flessibilità o il supporto per uno scenario di layout specifico, i modelli personalizzati sono supportati dal framework della barra multifunzione tramite l'elemento [**Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)

I modelli personalizzati possono essere dichiarati in due modi: un metodo autonomo che usa l'elemento [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) per dichiarare modelli riutilizzabili, denominati o un metodo inline specifico di [**Group.**](windowsribbon-element-group.md)

### <a name="standalone-template"></a>Modello autonomo

L'esempio di codice seguente illustra un modello personalizzato di base riutilizzabile.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a>Modello inline

Gli esempi di codice seguenti illustrano un modello personalizzato inline di base per un gruppo di quattro pulsanti.

Questa sezione di codice illustra le dichiarazioni command per un gruppo di pulsanti. Qui vengono specificate anche le risorse per immagini di grandi e piccole dimensioni.


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



Questa sezione di codice illustra come definire modelli [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) di grandi, medie e piccole dimensioni per visualizzare i quattro pulsanti di varie dimensioni e layout. La [**dichiarazione ScalingPolicy**](windowsribbon-element-scalingpolicy.md) per la scheda definisce quale modello viene usato per un gruppo di controlli in base alle dimensioni e allo spazio della barra multifunzione richiesti dalla scheda attiva.


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



Le immagini seguenti illustrano come vengono applicati i modelli dell'esempio precedente all'interfaccia utente della barra multifunzione per ridurre le dimensioni della barra multifunzione.



|  Tipo  |      Immagine                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| Grande  | ![immagine di un modello personalizzato di grandi dimensioni inline.](images/overviews/sizedefinition-custom-large.png)   |
| Medio | ![Immagine di un modello personalizzato medio inline.](images/overviews/sizedefinition-custom-medium.png) |
| Small  | ![immagine di un modello personalizzato di piccole dimensioni inline.](images/overviews/sizedefinition-custom-small.png)   |
| Popup  | ![immagine di un modello personalizzato popup inline.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**SizeDefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Scalabilità**](windowsribbon-element-scale.md)
</dt> <dt>

[**Group**](windowsribbon-element-group.md)
</dt> </dl>

 

 





