---
title: Elemento Scale
description: Rappresenta le dimensioni e la preferenza di layout di un gruppo di controlli tramite una coppia Group, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Barra multifunzione di Windows per l'elemento Scale
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3ba922b65525b92189673020f7155275bdf49f9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445012"
---
# <a name="scale-element"></a>Elemento Scale

Rappresenta le dimensioni e la preferenza di layout [**di un gruppo**](windowsribbon-element-group.md) di controlli tramite una coppia {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.

## <a name="usage"></a>Utilizzo

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
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
<td><strong>Gruppo</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>Sì<br/></td>
<td>Deve corrispondere a un oggetto <a href="windowsribbon-element-group.md"><strong>CommandName</strong></a> <em>di gruppo esistente.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa o valore intero compreso tra 2 e 59999, inclusi o 0x2 e 0xea5f in formato esadecimale, inclusivo. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Dimensioni</strong><br/></td>
<td>xs:string<br/></td>
<td>Sì<br/></td>
<td>Questo valore deve corrispondere a una delle dimensioni valide per <em>l'attributo SizeDefinition</em> del gruppo <a href="windowsribbon-element-group.md"><strong>di</strong></a> controlli associato specificato in <em>Group.</em> <br/> Limitato a uno dei valori seguenti: <br/> <br/>
<dt><span></span><span></span><strong></strong> (Popup)<br/> </dt> <dd> Layout di controllo identico <code>Large</code> a ma ospitato in un riquadro popup o a discesa.<br/> </dd> <dt><span></span><span></span><strong></strong> (Small)<br/> </dt> <dd> Modello <a href="windowsribbon-element-sizedefinition.md"><strong>Small SizeDefinition.</strong></a><br/> </dd> <dt><span></span><span></span><strong></strong> (Media)<br/> </dt> <dd> Modello <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> medio.<br/> </dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd> Modello <a href="windowsribbon-element-sizedefinition.md"><strong>Large SizeDefinition.</strong></a><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per [**ogni oggetto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) [**o ScalingPolicy.IdealSizes.**](windowsribbon-element-scalingpolicy-idealsizes.md)

Ogni coppia di attributi (*Group*, *Size*) deve essere univoca.

## <a name="examples"></a>Esempio

L'esempio seguente illustra come personalizzare l'aspetto dei controlli in un oggetto [**Group**](windowsribbon-element-group.md) tramite la funzionalità di layout adattivo dei modelli [**SizeDefinition della**](windowsribbon-element-sizedefinition.md) barra multifunzione.

Il [**manifesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) in questo esempio specifica una preferenza [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una **scheda Home.** Inoltre, gli **elementi Scale** vengono specificati per influenzare il comportamento di compressione, in ordine di dimensione decrescente, di ogni gruppo.


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a>Informazioni sull'elemento



* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** Sì



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





