---
title: Ribbon (elemento)
description: Rappresenta il controllo Ribbon nella visualizzazione della barra multifunzione.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Barra multifunzione di Windows elemento barra multifunzione
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76ce73735d05b3d8c8cfa686f53570fd08ae6f1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299037"
---
# <a name="ribbon-element"></a>Ribbon (elemento)

Rappresenta il controllo Ribbon nella visualizzazione della barra multifunzione.

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
<td><dt><span></span><span></span><strong></strong> Piccolo<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> Media<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Grandi dimensioni<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nome</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Utilizzato per annotare l'elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Qualsiasi sequenza di zero o più caratteri.<br/> La lunghezza massima è unbounded.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                         | Descrizione                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Ribbon. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Può verificarsi al massimo una volta<br/> <br/> |
| [**Ribbon. Tabs**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Application. views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve essere eseguita esattamente una volta per ogni elemento [**Application. views**](windowsribbon-element-application-views.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per una visualizzazione della **barra multifunzione** .


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | No        |



 

 





