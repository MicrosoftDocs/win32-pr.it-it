---
title: Elemento GroupSizeDefinition
description: Rappresenta le dimensioni di un layout per un gruppo di controlli in un modello personalizzato.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- Elemento GroupSizeDefinition Windows Ribbon
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc3184f18bf692c333d7088ade79ff4ac5360f1a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631359"
---
# <a name="groupsizedefinition-element"></a>Elemento GroupSizeDefinition

Rappresenta le dimensioni di un layout per un gruppo di controlli in un modello personalizzato.

## <a name="usage"></a>Utilizzo

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
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
<td><strong>Size</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (Media)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Piccola)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                 | Descrizione                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ColumnBreak**](windowsribbon-element-columnbreak.md)<br/>                     | Può verificarsi una o più volte<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                   | Può verificarsi una o più volte<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Può verificarsi una o più volte<br/> <br/> |
| [**Riga**](windowsribbon-element-row.md)<br/>                                     | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                   |
|---------------------------------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi fino a tre volte per ogni [**elemento SizeDefinition**](windowsribbon-element-sizedefinition.md) (una volta per *ogni size*).

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra un modello personalizzato di base che include le tre dimensioni di layout dei gruppi che devono essere definite con l'elemento **GroupSizeDefinition** durante la creazione di un modello personalizzato.


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
* **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





