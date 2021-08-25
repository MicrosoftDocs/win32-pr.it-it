---
title: SplitButton.ButtonItem - proprietà
description: Rappresenta un contenitore per un pulsante o un interruttore che espone il comando predefinito di un pulsante di divisione.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Proprietà SplitButton.ButtonItem Windows ribbon
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f49f316f7c740b434f761bbe4c00906c8f76b5027af9fcc87317af2a51960dab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840691"
---
# <a name="splitbuttonbuttonitem-property"></a>SplitButton.ButtonItem - proprietà

Rappresenta un contenitore per [un pulsante o](windowsribbon-controls-button.md) un [interruttore che](windowsribbon-controls-togglebutton.md) espone il comando predefinito di un pulsante di [divisione.](windowsribbon-controls-splitbutton.md)

## <a name="usage"></a>Utilizzo

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Descrizione                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>             | Può verificarsi al massimo una volta<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni controllo SplitButton.**](windowsribbon-element-splitbutton.md)

Ogni **elemento SplitButton.ButtonItem** può contenere un solo [**elemento figlio Button**](windowsribbon-element-button.md) o [**ToggleButton.**](windowsribbon-element-togglebutton.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per [il pulsante di divisione](windowsribbon-controls-splitbutton.md).

Questa sezione di codice illustra le dichiarazioni di comando [**SplitButton**](windowsribbon-element-splitbutton.md) **e SplitButton.ButtonItem,** con un oggetto [**Group**](windowsribbon-element-group.md) associato che funziona come contenitore padre per **l'elemento SplitButton.**


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



Questa sezione di codice illustra le [**dichiarazioni dei controlli SplitButton**](windowsribbon-element-splitbutton.md) **e SplitButton.ButtonItem.**


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Pulsante di divisione](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





