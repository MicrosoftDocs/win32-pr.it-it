---
title: QuickAccessToolbar.ApplicationDefaults - proprietà
description: Rappresenta un contenitore per i comandi predefiniti nella barra di accesso rapido.
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- Proprietà QuickAccessToolbar.ApplicationDefaults Windows ribbon
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701a7c72e40b1efe9104d6794fa739c556b0fb4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473747"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>QuickAccessToolbar.ApplicationDefaults - proprietà

Rappresenta un contenitore per i comandi predefiniti nella barra [di accesso rapido .](windowsribbon-controls-quickaccesstoolbar.md)

## <a name="usage"></a>Utilizzo

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio




| Elemento | Descrizione | 
|---------|-------------|
| <a href="windowsribbon-element-button.md"><strong>Button</strong></a><br /> | È necessaria almeno una occorrenza.<br /><br /> | 
| <a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a><br /> | È necessaria almeno una occorrenza.<br /><br /> | 
| <a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br /> | È necessaria almeno una occorrenza.<br /><blockquote>[!Note]<br />Windows 8 e più recente.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br /> | È necessaria almeno una occorrenza.<br /><blockquote>[!Note]<br />Windows 8 e più recente.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br /> | È necessaria almeno una occorrenza.<br /><blockquote>[!Note]<br />Windows 8 e più recente.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br /> | È necessaria almeno una occorrenza.<br /><blockquote>[!Note]<br />Windows 8 e più recente.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br /> | È necessaria almeno una occorrenza.<br /><br /> | 




## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

È necessario specificare almeno un elemento figlio.

È possibile specificare un massimo di 20 elementi figlio.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

Questa sezione di codice illustra la dichiarazione del controllo **QuickAccessToolbar.ApplicationDefaults.**


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





