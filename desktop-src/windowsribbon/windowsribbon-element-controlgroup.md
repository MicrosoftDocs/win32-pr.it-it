---
title: Elemento ControlGroup
description: Rappresenta un gruppo di controlli in un modello di layout SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Elemento ControlGroup Windows ribbon
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1777bd469b6bf07530881f9c20888d69fe98117ecbdeba4f3f5557f01ced172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117851027"
---
# <a name="controlgroup-element"></a>Elemento ControlGroup

Rappresenta un gruppo di controlli in un modello di layout [**SizeDefinition.**](windowsribbon-element-sizedefinition.md)

## <a name="usage"></a>Utilizzo

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
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
<td><strong>Sequencenumber</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Valido solo quando <a href="windowsribbon-element-group.md"><strong>Group</strong></a> è l'elemento padre.<br/> Ogni <em>SequenceNumber deve</em> essere univoco all'interno di un <a href="windowsribbon-element-group.md"><strong>elemento Group.</strong></a> I valori di <em>SequenceNumber</em> devono aumentare per ogni <strong>elemento Group,</strong> ma non devono essere sequenziali. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1000 e 59999, inclusi.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                 | Descrizione                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                               | Può verificarsi una o più volte<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                           | Può verificarsi una o più volte<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                           | Può verificarsi una o più volte<br/> <br/> |
| [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)<br/> | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>               | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>     | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>             | Può verificarsi una o più volte<br/> <br/> |
| [**Controllo FontControl**](windowsribbon-element-fontcontrol.md)<br/>                     | Può verificarsi al massimo una volta<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>             | Può verificarsi una o più volte<br/> <br/> |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                             | Può verificarsi una o più volte<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                     | Può verificarsi una o più volte<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>       | Può verificarsi una o più volte<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                   | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                             |
|-------------------------------------------------------------------------------------|
| **ControlGroup**<br/>                                                         |
| [**Group**](windowsribbon-element-group.md)<br/>                             |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> |
| [**Riga**](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per ogni [**elemento Group**](windowsribbon-element-group.md) **o ControlGroup.**

Se non vengono forniti numeri di sequenza, il rendering degli elementi viene eseguito nell'ordine specificato nel markup della barra multifunzione.

Se [](windowsribbon-element-group.md) Group o **ControlGroup** è l'elemento padre, **ControlGroup** è vincolato ai seguenti possibili elementi figlio: [**Button,**](windowsribbon-element-button.md) [**CheckBox,**](windowsribbon-element-checkbox.md) [**ComboBox,**](windowsribbon-element-combobox.md) [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**FontControl,**](windowsribbon-element-fontcontrol.md) [**InRibbonGallery,**](windowsribbon-element-inribbongallery.md) [**Spinner,**](windowsribbon-element-spinner.md) [**SplitButton,**](windowsribbon-element-splitbutton.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md)

In caso contrario, [**quando Row**](windowsribbon-element-row.md) o [**GroupSizeDefinition è**](windowsribbon-element-groupsizedefinition.md) l'elemento padre, [**Group**](windowsribbon-element-group.md) è vincolato all'elemento figlio seguente: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra il markup di base per un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) a quattro pulsanti personalizzato con vari [**elementi Group.**](windowsribbon-element-group.md)


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

[Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





