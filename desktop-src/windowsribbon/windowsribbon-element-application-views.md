---
title: Application.Views - proprietà
description: Rappresenta un contenitore per ogni visualizzazione del framework della barra multifunzione, in particolare la barra multifunzione e ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Proprietà Application.Views Windows ribbon
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe063397698a74da0421cf0c9c3b2ef46861f1477e0f4ac99fe5d6e6063c7251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964310"
---
# <a name="applicationviews-property"></a>Application.Views - proprietà

Rappresenta un contenitore per ogni visualizzazione del framework della barra multifunzione, in particolare [**la barra multifunzione**](windowsribbon-element-ribbon.md) e [**ContextPopup.**](windowsribbon-element-contextpopup.md)

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
| [**ContextPopup**](windowsribbon-element-contextpopup.md)<br/> | Può verificarsi una o più volte<br/> <br/> |
| [**Barra multifunzione**](windowsribbon-element-ribbon.md)<br/>             | Deve verificarsi esattamente una volta<br/> <br/>     |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**Applicazione**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve verificarsi esattamente una volta per ogni [**elemento Application.**](windowsribbon-element-application.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra un **elemento Application.Views** che contiene un manifesto dei controlli barra multifunzione, ognuno con un riferimento a un oggetto Command dichiarato nell'elemento [**Application.Commands.**](windowsribbon-element-application-commands.md)


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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Application.Commands**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





