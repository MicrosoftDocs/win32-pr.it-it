---
title: Elemento Ribbon
description: Rappresenta il controllo della barra multifunzione nella visualizzazione della barra multifunzione.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Barra multifunzione - Windows barra multifunzione
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5dd422013bdaf81d5d6aac6d0a34f4c9479af26cd79f64b854299caa3cac3f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202202"
---
# <a name="ribbon-element"></a>Elemento Ribbon

Rappresenta il controllo della barra multifunzione nella visualizzazione della barra multifunzione.

## <a name="usage"></a>Utilizzo

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Type</th>
<th>Obbligatoria</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GroupSpacing</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (Small)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (Media)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nome</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Usato per annotare l'elemento di comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Qualsiasi sequenza di zero o più caratteri.<br/> La lunghezza massima è illimitata.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                         | Descrizione                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Application.Views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve verificarsi esattamente una volta per [**ogni elemento Application.Views.**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per una **visualizzazione barra** multifunzione.


```XML
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
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a>Informazioni sull'elemento




* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** No



 

 





