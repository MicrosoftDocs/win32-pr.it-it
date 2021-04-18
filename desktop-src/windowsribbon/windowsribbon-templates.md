---
title: Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità
description: I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione di Windows e basati su una combinazione di comportamenti predefiniti e modelli di layout (definiti dal Framework e personalizzati) come dichiarati nel markup della barra multifunzione. Queste regole definiscono i comportamenti del layout adattivo del Framework della barra multifunzione che influenzano il modo in cui i controlli della barra dei comandi si adattano a diverse dimensioni della barra multifunzione in fase di esecuzione.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Barra multifunzione di Windows, personalizzazione
- Barra multifunzione, personalizzazione
- Barra multifunzione di Windows, modelli SizeDefinition
- Barra multifunzione, modelli SizeDefinition
- Barra multifunzione di Windows, modelli personalizzati
- Barra multifunzione, modelli personalizzati
- personalizzazione della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b12618f88576cddeff119534215e501216193c3
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2020
ms.locfileid: "104554664"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità

I controlli ospitati nella barra dei comandi della barra multifunzione sono soggetti alle regole di layout applicate dal framework della barra multifunzione di Windows e basati su una combinazione di comportamenti predefiniti e modelli di layout (definiti dal Framework e personalizzati) come dichiarati nel markup della barra multifunzione. Queste regole definiscono i comportamenti del layout adattivo del Framework della barra multifunzione che influenzano il modo in cui i controlli della barra dei comandi si adattano a diverse dimensioni della barra multifunzione in fase di esecuzione.

-   [Introduzione](#introduction)
    -   [Modelli SizeDefinition della barra multifunzione](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Modelli personalizzati](#custom-templates)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il layout adattivo, come definito dal framework della barra multifunzione, è la capacità di tutti i controlli all'interno dell'interfaccia utente della barra multifunzione di regolare dinamicamente l'organizzazione, le dimensioni, il formato e la scala relativa in base alle modifiche apportate alle dimensioni della barra multifunzione in fase di esecuzione.

Il Framework espone la funzionalità di layout adattivo tramite un set di elementi di markup dedicati per specificare e personalizzare diversi comportamenti di layout. Un insieme di modelli, denominato [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), viene definito dal Framework, ognuno dei quali supporta vari scenari di controllo e layout. Tuttavia, il Framework supporta anche modelli personalizzati se i modelli predefiniti non forniscono l'esperienza dell'interfaccia utente o i layout richiesti da un'applicazione.

Per visualizzare i controlli in un layout preferito a una determinata dimensione della barra multifunzione, sia i modelli predefiniti che i modelli personalizzati funzionano insieme all'elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) . Questo elemento contiene un manifesto di preferenze di dimensione utilizzato dal Framework come guida durante il rendering della barra multifunzione.

> [!Note]  
> Il Framework Ribbon fornisce comportamenti di layout predefiniti basati su un set di regole euristiche predefinite per l'organizzazione e la presentazione di controlli in fase di esecuzione senza la necessità di modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefiniti. Questa funzionalità, tuttavia, è destinata solo ai prototipi.

 

### <a name="ribbon-sizedefinition-templates"></a>Modelli SizeDefinition della barra multifunzione

Il Framework della barra multifunzione fornisce un set completo di modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) che specificano il comportamento delle dimensioni e del layout per un [gruppo](windowsribbon-controls-group.md) di controlli della barra multifunzione. Questi modelli riguardano scenari più comuni per organizzare i controlli in un'applicazione Ribbon.

Per applicare un'esperienza utente coerente tra le applicazioni della barra multifunzione, ogni modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impone restrizioni sui controlli o sulla famiglia di controlli supportati.

Ad esempio, la famiglia di controlli Button include:

-   [Button](windowsribbon-controls-button.md)
-   [Interruttore](windowsribbon-controls-togglebutton.md)
-   [Pulsante a discesa](windowsribbon-controls-dropdownbutton.md)
-   [Pulsante di divisione](windowsribbon-controls-splitbutton.md)
-   [Raccolta a discesa](windowsribbon-controls-dropdowngallery.md)
-   [Raccolta di pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md)
-   [Selezione colori a discesa](windowsribbon-controls-dropdowncolorpicker.md)

Sebbene la famiglia di controlli di input includa:

-   [ComboBox](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

La [casella di controllo](windowsribbon-controls-checkbox.md) e la [raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) non appartengono al gruppo di pulsanti o alla famiglia di input. Questi due controlli possono essere usati solo laddove indicato in modo esplicito in un modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

Di seguito è riportato un elenco dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) con una descrizione del layout e dei controlli consentiti da ogni modello.

> [!IMPORTANT]
> Se i controlli dichiarati nel markup non eseguono esattamente il mapping al tipo di controllo, all'ordine e alla quantità definiti nel modello associato, viene registrato un [errore di convalida](windowsribbon-compilationerrors.md) da parte del [compilatore di markup](windowsribbon-intentcl.md) e la compilazione viene terminata.

 



OneButton

Un controllo della famiglia di pulsanti.<br/> Sono supportate solo le dimensioni di gruppo grandi.<br/>

![immagine del modello sizedefinition di OneButton.](images/overviews/sizedefinition-onebutton.png)

TwoButtons

Due controlli della famiglia di pulsanti.<br/> Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.<br/>

![immagine del modello sizedefinition di twobuttons di grandi dimensioni.](images/overviews/sizedefinition-twobuttons-large.png)

![immagine del modello sizedefinition twobuttons medium.](images/overviews/sizedefinition-twobuttons-medium.png)

ThreeButtons

Tre controlli della famiglia di pulsanti.<br/> Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.<br/>

![immagine del modello sizedefinition di threebuttons di grandi dimensioni.](images/overviews/sizedefinition-threebuttons-large.png)

![immagine del modello sizedefinition threebuttons medium.](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Tre controlli della famiglia di pulsanti.<br/> Il primo pulsante è riportato in evidenza in tutte e tre le dimensioni.<br/>

![immagine di threebuttons-onebigandtwosmall modello di sizedefinition di grandi dimensioni.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![immagine del modello threebuttons-onebigandtwosmall medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![immagine di threebuttons-onebigandtwosmall Small sizedefinition template.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

ThreeButtonsAndOneCheckBox

Tre controlli della famiglia di pulsanti accompagnati da un singolo controllo CheckBox.<br/> Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.<br/>

![immagine del modello sizedefinition di threebuttonsandonecheckbox di grandi dimensioni.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![immagine del modello sizedefinition threebuttonsandonecheckbox medium.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

FourButtons

Quattro controlli della famiglia di pulsanti.<br/>

![immagine del modello sizedefinition di fourbuttons di grandi dimensioni.](images/overviews/sizedefinition-fourbuttons-large.png)

![immagine del modello sizedefinition fourbuttons medium.](images/overviews/sizedefinition-fourbuttons-medium.png)

![immagine di fourbuttons Small sizedefinition template.](images/overviews/sizedefinition-fourbuttons-small.png)

FiveButtons

Cinque controlli della famiglia di pulsanti.<br/>

![immagine del modello sizedefinition di fivebuttons di grandi dimensioni.](images/overviews/sizedefinition-fivebuttons-large.png)

![immagine del modello sizedefinition fivebuttons medium.](images/overviews/sizedefinition-fivebuttons-medium.png)

![immagine di fivebuttons Small sizedefinition template.](images/overviews/sizedefinition-fivebuttons-small.png)

FiveOrSixButtons

Cinque controlli della famiglia Button e un sesto pulsante facoltativo.<br/>

![immagine del modello sizedefinition di fiveorsixbuttons di grandi dimensioni.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![immagine del modello sizedefinition fiveorsixbuttons medium.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![immagine di fiveorsixbuttons Small sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

SixButtons

Sei controlli della famiglia di pulsanti.<br/>

![immagine del modello sizedefinition di sixbuttons di grandi dimensioni.](images/overviews/sizedefinition-sixbuttons-large.png)

![immagine del modello sizedefinition sixbuttons medium.](images/overviews/sizedefinition-sixbuttons-medium.png)

![immagine di sixbuttons Small sizedefinition template.](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Sei controlli della famiglia di pulsanti (presentazione alternativa).<br/>

![immagine di sixbuttons-twocolumns modello di sizedefinition di grandi dimensioni.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns modello di sizedefinition medio.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![immagine di sixbuttons-twocolumns Small sizedefinition template.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

SevenButtons

Sette controlli della famiglia di pulsanti.<br/>

![immagine del modello sizedefinition di sevenbuttons di grandi dimensioni.](images/overviews/sizedefinition-sevenbuttons-large.png)

![immagine del modello mediumsizedefinition di sevenbuttons.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![immagine di sevenbuttons Small sizedefinition template.](images/overviews/sizedefinition-sevenbuttons-small.png)

EightButtons

Otto controlli della famiglia di pulsanti.<br/>

![immagine di eightbuttons-lastthreesmall modello di sizedefinition di grandi dimensioni.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![immagine del modello eightbuttons-lastthreesmall medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![immagine di eightbuttons-lastthreesmall Small sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Otto controlli della famiglia di pulsanti (presentazione alternativa).<br/>

> [!Note]  
> Tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti in due elementi [**ControlGroup**](windowsribbon-element-controlgroup.md) : uno per i primi cinque elementi e uno per gli ultimi tre elementi.

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



![immagine del modello sizedefinition di eightbuttons di grandi dimensioni.](images/overviews/sizedefinition-eightbuttons-large.png)

![immagine del modello sizedefinition eightbuttons medium.](images/overviews/sizedefinition-eightbuttons-medium.png)

![immagine di eightbuttons Small sizedefinition template.](images/overviews/sizedefinition-eightbuttons-small.png)

NineButtons

Nove controlli della famiglia di pulsanti.

![immagine del modello sizedefinition di ninebuttons di grandi dimensioni.](images/overviews/sizedefinition-ninebuttons-large.png)

![immagine del modello sizedefinition ninebuttons medium.](images/overviews/sizedefinition-ninebuttons-medium.png)

![immagine di ninebuttons Small sizedefinition template.](images/overviews/sizedefinition-ninebuttons-small.png)

TenButtons

Dieci controlli della famiglia di pulsanti.

![immagine del modello sizedefinition di tenbuttons di grandi dimensioni.](images/overviews/sizedefinition-tenbuttons-large.png)

![immagine del modello sizedefinition tenbuttons medium.](images/overviews/sizedefinition-tenbuttons-medium.png)

![immagine di tenbuttons Small sizedefinition template.](images/overviews/sizedefinition-tenbuttons-small.png)

ElevenButtons

Undici controlli della famiglia di pulsanti.

![immagine del modello sizedefinition di elevenbuttons di grandi dimensioni.](images/overviews/sizedefinition-elevenbuttons-large.png)

![immagine del modello sizedefinition elevenbuttons medium.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![immagine di elevenbuttons Small sizedefinition template.](images/overviews/sizedefinition-elevenbuttons-small.png)

OneFontControl

Un [**FontControl**](windowsribbon-element-fontcontrol.md).

Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.

> [!IMPORTANT]
> L'inclusione di un [**FontControl**](windowsribbon-element-fontcontrol.md) all'interno di una definizione di modello personalizzata non è supportata dal Framework.

 

![immagine del modello sizedefinition di onefontcontrol di grandi dimensioni.](images/overviews/sizedefinition-onefontcontrol-large.png)

![immagine del modello sizedefinition onefontcontrol medium.](images/overviews/sizedefinition-onefontcontrol-medium.png)

OneInRibbonGallery

Un controllo [**inribbongallery**](windowsribbon-element-inribbongallery.md) .

Sono supportate solo dimensioni di gruppi di grandi dimensioni e di dimensioni ridotte.

![immagine del modello sizedefinition di oneinribbongallery di grandi dimensioni.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![immagine di oneinribbongallery Small sizedefinition template.](images/overviews/sizedefinition-oneinribbongallery-small.png)

InRibbonGalleryAndBigButton

Un controllo [**inribbongallery**](windowsribbon-element-inribbongallery.md) e un controllo della famiglia di pulsanti.

Sono supportate solo dimensioni di gruppi di grandi dimensioni e di dimensioni ridotte.

![immagine del modello sizedefinition di inribbongalleryandbigbutton di grandi dimensioni.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![immagine di inribbongalleryandbigbutton Small sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Un controllo [della raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) e due o tre controlli della famiglia di pulsanti.

La raccolta comprime la rappresentazione popup in dimensioni medie e piccole del gruppo.

![immagine di inribbongalleryandbuttons-galleryscalesfirst modello di sizedefinition di grandi dimensioni.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![immagine del modello inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![immagine di inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

ButtonGroups

Una disposizione complessa di controlli della famiglia di pulsanti 32 (la maggior parte dei quali è facoltativa).

> [!Note]  
> Oltre al pulsante di ridimensionamento completo facoltativo del modello ButtonGroups di grandi dimensioni, tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti in elementi [**ControlGroup**](windowsribbon-element-controlgroup.md) .

 

Nell'esempio seguente viene illustrato il markup necessario per visualizzare tutti gli elementi del controllo 32 (obbligatorio e facoltativo) con questo modello.


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



![immagine del modello sizedefinition di buttongroups di grandi dimensioni.](images/overviews/sizedefinition-buttongroups-large.png)

![immagine del modello sizedefinition buttongroups medium.](images/overviews/sizedefinition-buttongroups-medium.png)

![immagine di buttongroups Small sizedefinition template.](images/overviews/sizedefinition-buttongroups-small.png)

ButtonGroupsAndInputs

Due controlli della famiglia di input (il secondo è facoltativo) seguiti da una disposizione complessa di 29 controlli della famiglia di pulsanti (la maggior parte dei quali è facoltativa).

Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.

> [!Note]  
> Tutti gli elementi di controllo dichiarati con questo modello devono essere contenuti negli elementi [**ControlGroup**](windowsribbon-element-controlgroup.md) .

 

Nell'esempio seguente viene illustrato il markup necessario per visualizzare tutti gli elementi del controllo (obbligatorio e facoltativo) con questo modello.


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



![immagine del modello sizedefinition di buttongroupsandinputs di grandi dimensioni.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![immagine del modello sizedefinition buttongroupsandinputs medium.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

BigButtonsAndSmallButtonsOrInputs

Due controlli della famiglia di pulsanti (entrambi facoltativi) seguiti da due o tre pulsanti o controlli della famiglia di input.

Sono supportate solo le dimensioni di gruppi di grandi dimensioni e medie.

![immagine del modello sizedefinition di bigbuttonsandsmallbuttonsorinputs di grandi dimensioni.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![immagine del modello sizedefinition bigbuttonsandsmallbuttonsorinputs medium.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Esempio di SizeDefinition di base

L'esempio di codice seguente fornisce una dimostrazione di base di come dichiarare un modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) nel markup della barra multifunzione.

Per questo particolare esempio viene usato *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) , ma tutti i modelli di Framework sono specificati in modo analogo.


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



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>Esempio SizeDefinition complesso con criteri di ridimensionamento

Il comportamento di compressione dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) può essere controllato tramite l'uso di criteri di ridimensionamento nel markup della barra multifunzione.

L'elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contiene un manifesto di [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e le dichiarazioni di [**scala**](windowsribbon-element-scale.md) che specificano le preferenze di layout adattivo per uno o più elementi [**Group**](windowsribbon-element-group.md) quando la barra multifunzione viene ridimensionata.

> [!Note]  
> È consigliabile specificare i dettagli dei criteri di scalabilità adeguati in modo che la maggior parte degli elementi di [**gruppo**](windowsribbon-element-group.md) , se non tutti, siano associati a un elemento [**scale**](windowsribbon-element-scale.md) in cui l'attributo *size* è uguale a `Popup` . Questa operazione consente al Framework di eseguire il rendering della barra multifunzione con le dimensioni minime possibili e di supportare la più ampia gamma di dispositivi di visualizzazione, prima di introdurre automaticamente un meccanismo di scorrimento.

 

Nell'esempio di codice seguente viene illustrato un manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) che specifica una preferenza [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una scheda **Home** . Inoltre, gli elementi di [**scala**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di ridimensionamento decrescente, di ogni gruppo.


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

Se i comportamenti di layout predefiniti e i modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefiniti non offrono la flessibilità o il supporto per uno scenario di layout specifico, i modelli personalizzati sono supportati dal framework della barra multifunzione tramite l'elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .

I modelli personalizzati possono essere dichiarati in due modi: un metodo autonomo che usa l'elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) per dichiarare i modelli riutilizzabili, denominati o un metodo inline specifico del [**gruppo**](windowsribbon-element-group.md).

### <a name="standalone-template"></a>Modello autonomo

Nell'esempio di codice riportato di seguito viene illustrato un modello personalizzato di base riutilizzabile.


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

Negli esempi di codice seguenti viene illustrato un modello personalizzato inline di base per un gruppo di quattro pulsanti.

In questa sezione del codice vengono illustrate le dichiarazioni di comando per un gruppo di pulsanti. Qui sono specificate anche le risorse per immagini di grandi dimensioni e di dimensioni ridotte.


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



Questa sezione di codice illustra come definire modelli [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) di grandi dimensioni, medi e piccoli per visualizzare i quattro pulsanti in diverse dimensioni e layout. La Dichiarazione [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) per la scheda definisce il modello usato per un gruppo di controlli in base alla dimensione della barra multifunzione e allo spazio richiesto dalla scheda attiva.


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



Le immagini seguenti mostrano come vengono applicati i modelli dell'esempio precedente all'interfaccia utente della barra multifunzione per ridurre le dimensioni della barra multifunzione.



|        |                                                                                                    |
|--------|----------------------------------------------------------------------------------------------------|
| Grande  | ![immagine di un modello personalizzato di grandi dimensioni in linea.](images/overviews/sizedefinition-custom-large.png)   |
| Medio | ![immagine di un modello personalizzato medio in linea.](images/overviews/sizedefinition-custom-medium.png) |
| Piccola  | ![immagine di un modello personalizzato piccolo inline.](images/overviews/sizedefinition-custom-small.png)   |
| Popup  | ![immagine di un modello personalizzato popup in linea.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**SizeDefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Scalabilità**](windowsribbon-element-scale.md)
</dt> <dt>

[**Group**](windowsribbon-element-group.md)
</dt> </dl>

 

 





