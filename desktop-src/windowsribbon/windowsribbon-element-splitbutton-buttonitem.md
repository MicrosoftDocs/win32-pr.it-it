---
title: Proprietà SplitButton. ButtonItem
description: Rappresenta un contenitore per un pulsante o interruttore che espone il comando predefinito di un pulsante di suddivisione.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Barra multifunzione di Windows SplitButton. ButtonItem
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475766"
---
# <a name="splitbuttonbuttonitem-property"></a>Proprietà SplitButton. ButtonItem

Rappresenta un contenitore per un [pulsante](windowsribbon-controls-button.md) o [interruttore](windowsribbon-controls-togglebutton.md) che espone il comando predefinito di un pulsante di [suddivisione](windowsribbon-controls-splitbutton.md).

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

Può essere presente al massimo una volta per ogni [**SplitButton**](windowsribbon-element-splitbutton.md).

Ogni **SplitButton. ButtonItem** può contenere solo un [**pulsante**](windowsribbon-element-button.md) o un elemento figlio [**ToggleButton**](windowsribbon-element-togglebutton.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per il [pulsante di suddivisione](windowsribbon-controls-splitbutton.md).

In questa sezione del codice vengono illustrate le dichiarazioni di comando [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. ButtonItem** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButton** .


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



In questa sezione del codice vengono illustrate le dichiarazioni di controllo [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. ButtonItem** .


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo pulsante combinato](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





