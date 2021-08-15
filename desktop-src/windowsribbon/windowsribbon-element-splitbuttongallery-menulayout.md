---
title: SplitButtonGallery.MenuLayout - proprietà
description: Rappresenta un contenitore per i layout del menu a discesa Della raccolta di pulsanti di menu suddivisi.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- Proprietà SplitButtonGallery.MenuLayout Windows barra multifunzione
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40cf184d6122fc40041cfb77953bba2b7950d9d1a957d99aae659633ee5c194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706899"
---
# <a name="splitbuttongallerymenulayout-property"></a>SplitButtonGallery.MenuLayout - proprietà

Rappresenta un contenitore per [i](windowsribbon-controls-splitbuttongallery.md) layout del menu a discesa Della raccolta di pulsanti di menu suddivisi.

## <a name="usage"></a>Uso

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Descrizione                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Deve verificarsi esattamente una volta<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Deve verificarsi esattamente una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni elemento SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

> [!Note]  
> È consentito un massimo di un elemento figlio ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) [**o FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per [la raccolta di pulsanti di menu suddivisi.](windowsribbon-controls-splitbuttongallery.md)

Questa sezione di codice illustra la **dichiarazione del controllo SplitButtonGallery.MenuLayout.**


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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Raccolta di pulsanti di menu suddivisi](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Uso delle raccolte](ribbon-controls-galleries.md)
</dt> </dl>

 

 





