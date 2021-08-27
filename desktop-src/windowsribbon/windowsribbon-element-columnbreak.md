---
title: ColumnBreak - elemento
description: Rappresenta un separatore verticale (visibile o nascosto) nei modelli di layout SizeDefinition personalizzati.
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- Elemento ColumnBreak Windows barra multifunzione
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b5b5982b5348cef7a2dbaa3b60d639beabaf9d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630499"
---
# <a name="columnbreak-element"></a>ColumnBreak - elemento

Rappresenta un separatore verticale (visibile o nascosto) nei modelli di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizzati.

## <a name="usage"></a>Utilizzo

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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
<td><strong>ShowSeparator</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                             |
|-------------------------------------------------------------------------------------|
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per ogni [**elemento GroupSizeDefinition.**](windowsribbon-element-groupsizedefinition.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per **un elemento ColumnBreak** in un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) a quattro pulsanti personalizzato. ColumnBreak **viene** specificato solo per il `Large` modello.


```XML
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
```



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** Sì



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





