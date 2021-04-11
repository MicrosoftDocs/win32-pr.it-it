---
title: Proprietà SplitButtonGallery. MenuGroups
description: Rappresenta un contenitore per un set di voci di menu a discesa in un controllo SplitButtonGallery.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- Barra multifunzione di Windows SplitButtonGallery. MenuGroups
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119746"
---
# <a name="splitbuttongallerymenugroups-property"></a>Proprietà SplitButtonGallery. MenuGroups

Rappresenta un contenitore per un set di voci di menu a discesa in un controllo [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="usage"></a>Utilizzo

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                         | Descrizione                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Deve essere presente almeno una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve essere eseguita esattamente una volta per ogni elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per l'elemento **SplitButtonGallery. MenuGroups** .

Questa sezione di codice mostra la dichiarazione di controllo **SplitButtonGallery. MenuGroups** .


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo raccolta pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Uso delle raccolte](ribbon-controls-galleries.md)
</dt> </dl>

 

 





