---
title: Proprietà DropDownGallery.MenuGroups
description: Rappresenta un contenitore per un set di voci di menu a discesa in un controllo Drop-Down Gallery.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- Proprietà DropDownGallery.MenuGroups Windows ribbon
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdc52877884ac3a6407a0c7ed9f511cf78f8bcb5c125beb5f2ed19e651b83da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393051"
---
# <a name="dropdowngallerymenugroups-property"></a>Proprietà DropDownGallery.MenuGroups

Rappresenta un contenitore per un set di voci di menu a discesa in [un controllo Raccolta a](windowsribbon-controls-dropdowngallery.md) discesa.

## <a name="usage"></a>Utilizzo

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                         | Descrizione                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/> | Deve verificarsi almeno una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve verificarsi esattamente una volta per [**ogni elemento DropDownGallery.**](windowsribbon-element-dropdowngallery.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per **l'elemento DropDownGallery.MenuGroups.**

Questa sezione di codice mostra la dichiarazione del controllo **DropDownGallery.MenuGroups** in uno spazio [dei comandi della raccolta](windowsribbon-controls-dropdowngallery.md) a discesa.


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controllo Raccolta a discesa**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Uso delle raccolte](ribbon-controls-galleries.md)
</dt> </dl>

 

 





