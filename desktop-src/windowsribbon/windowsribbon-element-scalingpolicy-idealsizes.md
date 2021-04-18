---
title: Proprietà ScalingPolicy. IdealSizes
description: Rappresenta un contenitore di specifiche di ridimensionamento per il modello SizeDefinition preferito, in base alle dimensioni della barra multifunzione.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- Barra multifunzione di Windows ScalingPolicy. IdealSizes
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302306"
---
# <a name="scalingpolicyidealsizes-property"></a>Proprietà ScalingPolicy. IdealSizes

Rappresenta un contenitore di specifiche di ridimensionamento per il modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferito, in base alle dimensioni della barra multifunzione.

## <a name="usage"></a>Utilizzo

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                 | Descrizione                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Scalabilità**](windowsribbon-element-scale.md)<br/> | Può essere presente una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                 |
|-------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente al massimo una volta per ogni [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).

Se è definito **ScalingPolicy. IdealSizes** , deve essere presente una voce di [**scala**](windowsribbon-element-scale.md) per ogni elemento di [**gruppo**](windowsribbon-element-group.md) in un elemento [**Tab**](windowsribbon-element-tab.md) .

**ScalingPolicy. IdealSizes** sono i layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferiti per un [**gruppo**](windowsribbon-element-group.md) di controlli.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come è possibile personalizzare l'aspetto dei controlli in un [**gruppo**](windowsribbon-element-group.md) tramite la funzionalità di layout adattivo dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) della barra multifunzione.

Il manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) in questo esempio specifica una preferenza **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una scheda **Home** . Inoltre, gli elementi di [**scala**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di ridimensionamento decrescente, di ogni gruppo.


```C++
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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md)
</dt> </dl>

 

 





