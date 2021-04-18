---
title: Proprietà QuickAccessToolbar. ApplicationDefaults
description: Rappresenta un contenitore per i comandi predefiniti nella barra di accesso rapido (QAT).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- Barra multifunzione di Windows QuickAccessToolbar. ApplicationDefaults
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301189"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>Proprietà QuickAccessToolbar. ApplicationDefaults

Rappresenta un contenitore per i comandi predefiniti nella [barra di accesso rapido (QAT)](windowsribbon-controls-quickaccesstoolbar.md).

## <a name="usage"></a>Utilizzo

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-button.md"><strong>Button</strong></a><br/></td>
<td>È necessaria almeno una occorrenza.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-checkbox.md"><strong>Casella</strong></a><br/></td>
<td>È necessaria almeno una occorrenza.<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br/></td>
<td>È necessaria almeno una occorrenza.<br/>
<blockquote>
[!Note]<br />
Windows 8 e versioni successive.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br/></td>
<td>È necessaria almeno una occorrenza.<br/>
<blockquote>
[!Note]<br />
Windows 8 e versioni successive.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-inribbongallery.md"><strong>Inribbongallery</strong></a><br/></td>
<td>È necessaria almeno una occorrenza.<br/>
<blockquote>
[!Note]<br />
Windows 8 e versioni successive.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br/></td>
<td>È necessaria almeno una occorrenza.<br/>
<blockquote>
[!Note]<br />
Windows 8 e versioni successive.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br/></td>
<td>È necessaria almeno una occorrenza.<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente al massimo una volta per ogni [**QuickAccessToolBar**](windowsribbon-element-quickaccesstoolbar.md).

È necessario specificare almeno un elemento figlio.

È possibile specificare un massimo di 20 elementi figlio.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per [**QuickAccessToolBar**](windowsribbon-element-quickaccesstoolbar.md).

Questa sezione di codice mostra la dichiarazione di controllo **QuickAccessToolBar. ApplicationDefaults** .


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



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo della barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





