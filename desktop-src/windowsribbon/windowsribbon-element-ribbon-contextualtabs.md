---
title: Ribbon. ContextualTabs, proprietà
description: Rappresenta un contenitore per le schede contestuali.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. ContextualTabs
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740535"
---
# <a name="ribboncontextualtabs-property"></a>Ribbon. ContextualTabs, proprietà

Rappresenta un contenitore per le schede contestuali.

## <a name="usage"></a>Utilizzo

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                       | Descrizione                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/> | Deve essere presente almeno una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Barra multifunzione**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente al massimo una volta per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).

Le schede contestuali sono utili per visualizzare le funzionalità rilevanti solo per un contesto dell'applicazione specifico, ad esempio una scheda formattazione immagine in un editor di testo visualizzato solo quando viene evidenziata un'immagine. In genere, le schede contestuali non sono visibili fino a quando non si verifica un contesto di applicazione specifico e l'applicazione invia una notifica al framework della barra multifunzione.

Quando vengono visualizzate, le schede contestuali sono codificate con colori per distinguerle dalle schede normali.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per l'elemento **Ribbon. ContextualTabs** .

Questa sezione di codice mostra una dichiarazione di comando [**TabGroup**](windowsribbon-element-tabgroup.md) e due dichiarazioni di comando per [**schede**](windowsribbon-element-tab.md) contestuali.


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



Questa sezione di codice mostra la dichiarazione di controllo **Ribbon. ContextualTabs** con un [**TabGroup**](windowsribbon-element-tabgroup.md) e due controlli della [**scheda**](windowsribbon-element-tab.md) contestuale.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ribbon. Tabs**](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





