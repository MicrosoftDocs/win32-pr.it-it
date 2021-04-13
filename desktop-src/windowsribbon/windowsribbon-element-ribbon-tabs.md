---
title: Proprietà Ribbon. Tabs
description: Rappresenta un contenitore per tutte le schede principali in una barra multifunzione.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. Tabs
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475418"
---
# <a name="ribbontabs-property"></a>Proprietà Ribbon. Tabs

Rappresenta un contenitore per tutte le schede principali in una barra multifunzione.

## <a name="usage"></a>Utilizzo

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                             | Descrizione                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**Scheda**](windowsribbon-element-tab.md)<br/> | Deve essere presente almeno una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Barra multifunzione**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Può verificarsi una o più volte per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per un elemento **Ribbon. Tabs** con una dichiarazione di [**scheda**](windowsribbon-element-tab.md) **Home** .


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





