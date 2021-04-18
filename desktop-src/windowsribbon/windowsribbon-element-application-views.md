---
title: Proprietà Application. views
description: Rappresenta un contenitore per ogni visualizzazione del Framework della barra multifunzione, in particolare la barra multifunzione e l'ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Proprietà Application. views-barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301712"
---
# <a name="applicationviews-property"></a>Proprietà Application. views

Rappresenta un contenitore per ogni visualizzazione del Framework della barra multifunzione, in particolare la [**barra multifunzione**](windowsribbon-element-ribbon.md) e l' [**ContextPopup**](windowsribbon-element-contextpopup.md).

## <a name="usage"></a>Utilizzo

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Descrizione                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [**ContextPopup**](windowsribbon-element-contextpopup.md)<br/> | Può essere presente una o più volte<br/> <br/> |
| [**Barra multifunzione**](windowsribbon-element-ribbon.md)<br/>             | Deve verificarsi esattamente una volta<br/> <br/>     |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**Applicazione**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve essere eseguita esattamente una volta per ogni elemento [**dell'applicazione**](windowsribbon-element-application.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato un elemento **Application. views** che contiene un manifesto di controlli della barra multifunzione, ognuno con un riferimento a un comando dichiarato nell'elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Application. Commands**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





