---
title: Elemento ScalingPolicy
description: Rappresenta un contenitore per le specifiche di ridimensionamento.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Elemento ScalingPolicy barra multifunzione di Windows
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 812256b0ff329073eb516c6ab2eb7501db8de40d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444992"
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
| [**Scalabilità**](windowsribbon-element-scale.md)<br/>                                       | Può verificarsi una o più volte<br/> <br/> |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>      |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                         |
|---------------------------------------------------------------------------------|
| [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve verificarsi una sola volta per [**ogni Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).

**L'elemento ScalingPolicy** contiene un manifesto di [**dichiarazioni ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e [**Scale**](windowsribbon-element-scale.md) che specificano le preferenze di layout adattive per uno o più elementi [**Group**](windowsribbon-element-group.md) quando la barra multifunzione viene ridimensionata.

L'elenco [**di dichiarazioni Scale**](windowsribbon-element-scale.md) deve essere in ordine decrescente di dimensioni valide (Large, Medium, Small, Popup) per l'elemento [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associato all'elemento [**Group.**](windowsribbon-element-group.md)

> [!Note]  
> È consigliabile che siano specificati dettagli adeguati dei criteri di ridimensionamento in modo che una barra multifunzione sia in grado di eseguire il rendering senza barre di scorrimento quando viene ridimensionata a una larghezza di 300 pixel a 96 punti per pollice (dpi).

 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come personalizzare l'aspetto dei controlli in [**un**](windowsribbon-element-group.md) gruppo tramite la funzionalità di layout adattivo dei modelli [**SizeDefinition della**](windowsribbon-element-sizedefinition.md) barra multifunzione.

Il **manifesto ScalingPolicy** in questo esempio specifica una preferenza [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una **scheda** Home. Inoltre, gli [**elementi Scale**](windowsribbon-element-scale.md) vengono specificati per influire sul comportamento di compressione, in ordine decrescente, di ogni gruppo.


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

- **Sistema minimo supportato:** Windows 7 
- **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





