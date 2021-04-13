---
title: Elemento SplitButtonGallery
description: Rappresenta un controllo raccolta di pulsanti di menu combinato con un menu a discesa basato sulla raccolta.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Barra multifunzione Windows elemento SplitButtonGallery
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68e90137325c16af6942f9f3929f8abfdf795660
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473782"
---
# <a name="splitbuttongallery-element"></a>Elemento SplitButtonGallery

Rappresenta un controllo [raccolta di pulsanti](windowsribbon-controls-splitbuttongallery.md) di menu combinato con un menu a discesa basato sulla raccolta.

## <a name="usage"></a>Utilizzo

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.<br/> Gli spazi vuoti sono validi e vengono ignorati.<br/> Lunghezza massima: 250 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o xs: String<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Determina se la risorsa immagine grande o piccola del comando viene visualizzata nel controllo raccolta. <br/>
<blockquote>
[!Note]<br />
Si applica solo alle raccolte in cui il valore dell'attributo <em>Type</em> è uguale a <code>Command</code> .
</blockquote>
<br/> Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: Integer)<br/> </dt> <dd> Il valore predefinito è -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: Integer)<br/> </dt> <dd> Il valore predefinito è -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> Parte inferiore<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Nascondere<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Sinistra<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Sovrapposizione<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Destra<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Top<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Tipo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> Elementi<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Comandi<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                 | Descrizione                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                                               | Può essere presente una o più volte<br/> <br/> |
| [**Casella**](windowsribbon-element-checkbox.md)<br/>                                           | Può essere presente una o più volte<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                     | Può essere presente una o più volte<br/> <br/> |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | Deve verificarsi esattamente una volta<br/> <br/>     |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>      |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                                   | Può essere presente una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



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
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Group</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a><br/></td>
<td>Quando è contenuto in un <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>. Questo elemento è supportato solo al primo livello e non deve avere elementi figlio.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 e versioni successive.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButton**](windowsribbon-element-splitbutton.md) .

**SplitButtonGallery** supporta le [modalità di applicazione](ribbon-applicationmodes.md).

[Interfaccia utente \_ PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) viene usato da un'applicazione per eseguire una query sullo stato di attivazione/disattivazione per il controllo Button di un **SplitButtonGallery**.

Lo screenshot seguente illustra il controllo raccolta dei [pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md) della barra multifunzione in Microsoft Paint per Windows 7.

![Screenshot di un controllo raccolta di pulsanti di suddivisione in Microsoft Paint per Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per la [raccolta dei pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md).

In questa sezione del codice vengono illustrate le dichiarazioni di comando **SplitButtonGallery** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButtonGallery** .


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



In questa sezione del codice vengono illustrate le dichiarazioni di controllo **SplitButtonGallery** .


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | No        |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Controllo raccolta pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Uso delle raccolte](ribbon-controls-galleries.md)
</dt> <dt>

[**Modalità selettore**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Esempio di raccolta](windowsribbon-gallerysample.md)
</dt> </dl>

 

