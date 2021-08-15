---
title: InRibbonGallery.MenuLayout - proprietà
description: Rappresenta un contenitore per In-Ribbon menu a discesa raccolta.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Proprietà InRibbonGallery.MenuLayout Windows barra multifunzione
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3748e35280972f115ae22792f28847df675b3aafe8ac91d29d930c9fd15bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850764"
---
# <a name="inribbongallerymenulayout-property"></a>InRibbonGallery.MenuLayout - proprietà

Rappresenta un contenitore per [i](windowsribbon-controls-inribbongallery.md) layout del menu a discesa Raccolta nella barra multifunzione.

## <a name="usage"></a>Utilizzo

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Descrizione                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Deve verificarsi esattamente una volta<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Deve verificarsi esattamente una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni elemento InRibbonGallery.**](windowsribbon-element-inribbongallery.md)

> [!Note]  
> È consentito un massimo di un elemento figlio ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) [**o FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).

 

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per [la raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md).

Questa sezione di codice illustra la **dichiarazione del controllo InRibbonGallery.MenuLayout.**


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Uso delle raccolte](ribbon-controls-galleries.md)
</dt> </dl>

 

 





