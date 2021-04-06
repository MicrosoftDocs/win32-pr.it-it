---
title: Elemento ScalingPolicy
description: Rappresenta un contenitore per le specifiche di ridimensionamento.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Barra multifunzione Windows elemento ScalingPolicy
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f0d0f484ebded1233e3c64f6c7830882395b90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718802"
---
# <a name="scalingpolicy-element"></a>Elemento ScalingPolicy

Rappresenta un contenitore per le specifiche di ridimensionamento.

## <a name="usage"></a>Utilizzo

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                       | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Scalabilità**](windowsribbon-element-scale.md)<br/>                                       | Può essere presente una o più volte<br/> <br/> |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>      |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Tab. ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve essere presente una sola volta per ogni [**Tab. ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).

L'elemento **ScalingPolicy** contiene un manifesto di [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e le dichiarazioni di [**scala**](windowsribbon-element-scale.md) che specificano le preferenze di layout adattivo per uno o più elementi [**Group**](windowsribbon-element-group.md) quando la barra multifunzione viene ridimensionata.

L'elenco delle dichiarazioni di [**scala**](windowsribbon-element-scale.md) deve essere in ordine decrescente di dimensioni valide (large, medium, Small, popup) per il [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associato all'elemento del [**gruppo**](windowsribbon-element-group.md) .

> [!Note]  
> È consigliabile specificare i dettagli dei criteri di scalabilità adeguati in modo che una barra multifunzione sia in grado di eseguire il rendering senza barre di scorrimento se ridimensionato a una larghezza di 300 pixel a 96 punti per pollice (dpi).

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come è possibile personalizzare l'aspetto dei controlli in un [**gruppo**](windowsribbon-element-group.md) tramite la funzionalità di layout adattivo dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) della barra multifunzione.

Il manifesto **ScalingPolicy** in questo esempio specifica una preferenza [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una scheda **Home** . Inoltre, gli elementi di [**scala**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di ridimensionamento decrescente, di ogni gruppo.


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | No        |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md)
</dt> </dl>

 

 





