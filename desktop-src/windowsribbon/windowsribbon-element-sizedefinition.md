---
title: Elemento SizeDefinition
description: Rappresenta un modello di layout personalizzato dei controlli barra multifunzione.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Barra multifunzione di Windows per l'elemento SizeDefinition
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc68ac032459bed77d402ebd860886398748c874
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444802"
---
# <a name="sizedefinition-element"></a>Elemento SizeDefinition

Rappresenta un modello di layout personalizzato dei controlli barra multifunzione.

## <a name="usage"></a>Utilizzo

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
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
<td><strong>Nome</strong><br/></td>
<td>xs:positiveInteger o xs:string o xs:token<br/></td>
<td>Sì<br/></td>
<td>Quando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions è</strong></a> l'elemento padre, in caso contrario facoltativo.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string o xs:token)<br/> </dt> <dd> Stringa o valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                             | Descrizione                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [**ControlNameMap**](windowsribbon-element-controlnamemap.md)<br/>           | Può verificarsi al massimo una volta<br/> <br/>   |
| [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md)<br/> | Deve verificarsi almeno una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Gruppo**](windowsribbon-element-group.md)<br/>                                   |
| [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni [**elemento**](windowsribbon-element-group.md) Group.

Può verificarsi una o più volte per [**ogni elemento Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)

I modelli di layout predefiniti del framework [della](windowsribbon-templates.md) barra multifunzione vengono specificati con *l'attributo SizeDefinition* dell'elemento [**Group.**](windowsribbon-element-group.md)

Se un elemento [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) corrispondente non viene dichiarato per ogni [**elemento Group**](windowsribbon-element-group.md) in un elemento [**Tab,**](windowsribbon-element-tab.md) si verificherà un errore di convalida.

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra un modello personalizzato di base.


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


- **Sistema minimo supportato:** Windows 7 
- **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





