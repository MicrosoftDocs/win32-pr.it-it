---
title: ScalingPolicy.IdealSizes - proprietà
description: Rappresenta un contenitore di specifiche di ridimensionamento per il modello SizeDefinition preferito, in base alle dimensioni della barra multifunzione.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- Proprietà ScalingPolicy.IdealSizes Windows barra multifunzione
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500f6193411ed72b8858506816d9af4f82b1219680fa0537bf54b3daa7735211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439526"
---
# <a name="scalingpolicyidealsizes-property"></a>ScalingPolicy.IdealSizes - proprietà

Rappresenta un contenitore di specifiche di ridimensionamento per il modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferito, in base alle dimensioni della barra multifunzione.

## <a name="usage"></a>Uso

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
| [**Scalabilità**](windowsribbon-element-scale.md)<br/> | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                 |
|-------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni oggetto ScalingPolicy.**](windowsribbon-element-scalingpolicy.md)

Se **viene definito ScalingPolicy.IdealSizes,** deve essere presente una voce [**Scale**](windowsribbon-element-scale.md) per ogni [**elemento Group**](windowsribbon-element-group.md) in un elemento [**Tab.**](windowsribbon-element-tab.md)

**ScalingPolicy.IdealSizes è** il layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferito per un [**gruppo**](windowsribbon-element-group.md) di controlli.

## <a name="examples"></a>Esempio

L'esempio seguente illustra come personalizzare l'aspetto dei controlli in un oggetto [**Group**](windowsribbon-element-group.md) tramite la funzionalità di layout adattivo dei modelli [**SizeDefinition della**](windowsribbon-element-sizedefinition.md) barra multifunzione.

Il [**manifesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) in questo esempio specifica una preferenza **ScalingPolicy.IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una **scheda Home.** Inoltre, gli [**elementi Scale**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di dimensione decrescente, di ogni gruppo.


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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





