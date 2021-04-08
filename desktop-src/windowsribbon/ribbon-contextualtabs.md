---
title: Visualizzazione di schede contestuali
description: In un'applicazione della barra multifunzione di Windows una scheda contestuale è un controllo struttura a schede nascosto visualizzato nella scheda quando viene selezionato o evidenziato un oggetto nell'area di lavoro dell'applicazione, ad esempio un'immagine.
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Barra multifunzione di Windows, schede contestuali
- Barra multifunzione, schede contestuali
- visualizzazione delle schede contestuali della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727367"
---
# <a name="displaying-contextual-tabs"></a>Visualizzazione di schede contestuali

In un'applicazione della barra multifunzione di Windows una scheda contestuale è un controllo struttura a [schede](windowsribbon-controls-tab.md) nascosto visualizzato nella scheda quando viene selezionato o evidenziato un oggetto nell'area di lavoro dell'applicazione, ad esempio un'immagine.

-   [Introduzione](#introduction)
-   [Implementazione di schede contestuali](#implementing-contextual-tabs)
    -   [markup](#markup)
    -   [Codice](#code)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Diversamente dalle schede principali, che contengono vari comandi comuni che sono rilevanti indipendentemente dal contesto dell'area di lavoro, le schede contestuali contengono in genere uno o più comandi applicabili solo a un oggetto selezionato o evidenziato.

Quando un oggetto viene selezionato o evidenziato nell'area di lavoro dell'applicazione, il tipo e il contesto dell'oggetto potrebbero richiedere comandi diversi che non rendono il senso aziendale o funzionale in una scheda contestuale. In questi casi, potrebbe essere necessario disporre di più schede contestuali, contenute all'interno di un [gruppo di schede](windowsribbon-controls-tabgroup.md). Ad esempio, la selezione di un'immagine contenuta in una cella della tabella potrebbe richiedere due schede contestuali che espongono le funzionalità di tabella e immagine.

> [!Note]  
> Oltre a più schede contestuali, il Framework della barra multifunzione supporta anche più controlli [gruppo di schede](windowsribbon-controls-tabgroup.md) in una barra multifunzione.

 

Quando si visualizzano le schede contestuali, il Framework della barra multifunzione impone un set di comportamenti di base che includono:

-   Le schede contestuali sono posizionate nell'ordine in cui sono dichiarate e a destra delle schede principali nella riga della scheda della barra multifunzione.
-   Quando la barra multifunzione viene ridimensionata, le tabulazioni vengono ridimensionate e le etichette di tabulazione vengono troncate come richiesto dallo spazio. Tuttavia, alle schede contestuali visibili viene assegnata una priorità di visualizzazione superiore in cui vengono ridimensionate e troncate per ultime.
-   L'etichetta per un [gruppo di schede](windowsribbon-controls-tabgroup.md) viene visualizzata nella barra del titolo dell'applicazione e si estende a tutte le schede contestuali associate.
-   Quando più controlli [gruppo di schede](windowsribbon-controls-tabgroup.md) vengono visualizzati contemporaneamente, uno dei cinque colori univoci viene assegnato allo sfondo di ogni gruppo di schede nella barra del titolo dell'applicazione. Questo colore viene usato anche come colore di evidenziazione per le schede contestuali nel gruppo di schede.
-   L'assegnazione dei colori del [gruppo di schede](windowsribbon-controls-tabgroup.md) è basata sull'ordine con cui gli elementi del gruppo di schede sono dichiarati nel markup. I colori sono definiti dal Framework e non possono essere specificati dall'applicazione.
-   I colori del [gruppo di schede](windowsribbon-controls-tabgroup.md) definiti dal Framework possono essere modificati indirettamente tramite le chiavi delle proprietà del [Framework](windowsribbon-reference-properties-framework.md) . Per ulteriori informazioni, vedere [personalizzazione dei colori della barra multifunzione](ribbon-color.md).
-   Quando più di cinque controlli [gruppo di schede](windowsribbon-controls-tabgroup.md) vengono visualizzati in una sola volta, il Framework esegue il ciclo dei colori associati.
-   Il numero massimo di controlli struttura a [schede](windowsribbon-controls-tab.md) in una barra multifunzione è limitato a 100. Sono incluse le schede contestuali, visibili o meno.

Lo screenshot seguente mostra una scheda contestuale del disegno di Windows 7.

![screenshot che mostra un controllo scheda contestuale.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a>Implementazione di schede contestuali

In questa sezione vengono illustrati i dettagli di implementazione delle schede contestuali della barra multifunzione e viene illustrato come incorporarli in un'applicazione Ribbon.

### <a name="markup"></a>markup

Gli esempi seguenti illustrano il markup di base per un elemento [**TabGroup**](windowsribbon-element-tabgroup.md) che contiene due schede contestuali.

Questa sezione di codice mostra le dichiarazioni dei comandi [**TabGroup**](windowsribbon-element-tabgroup.md) e [Tab](windowsribbon-controls-tab.md) .


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



In questa sezione del codice vengono illustrate le dichiarazioni di controllo necessarie per visualizzare due schede contestuali all'interno di un [**TabGroup**](windowsribbon-element-tabgroup.md).


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



### <a name="code"></a>Codice

[Interfaccia utente \_ PKEY \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) è la singola chiave di proprietà definita dal Framework per specificare la visibilità e lo stato delle schede contestuali. Quando si seleziona un oggetto nell'area di lavoro dell'applicazione, è possibile assegnare a questa proprietà uno dei tre valori dell'enumerazione [**\_ CONTEXTAVAILABILITY dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) che definiscono se una scheda contestuale esiste e, in tal caso, se viene visualizzata come scheda attiva.

Un'applicazione richiede un aggiornamento del [gruppo di schede](windowsribbon-controls-tabgroup.md) invalidando e aggiornando la proprietà [ \_ pkey \_ ContextAvailable dell'interfaccia utente](windowsribbon-reference-properties-uipkey-contextavailable.md) quando viene modificato il contesto dell'area di lavoro.

Nelle sezioni seguenti del codice viene illustrato come visualizzare una scheda contestuale quando si seleziona un'immagine in un'area di lavoro dell'applicazione.


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo di progettazione della barra multifunzione](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 