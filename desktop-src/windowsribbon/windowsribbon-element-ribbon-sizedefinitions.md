---
title: Ribbon.SizeDefinitions - proprietà
description: Rappresenta un contenitore per i modelli di layout personalizzati dei controlli barra multifunzione.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- Proprietà Ribbon.SizeDefinitions Windows Ribbon
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f3109c7e9f709267310415b48238b24050c7531bc0f784290876ab47706d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202257"
---
# <a name="ribbonsizedefinitions-property"></a>Ribbon.SizeDefinitions - proprietà

Rappresenta un contenitore per i modelli di layout personalizzati dei controlli barra multifunzione.

## <a name="usage"></a>Utilizzo

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                   | Descrizione                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Barra multifunzione**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni [**barra multifunzione.**](windowsribbon-element-ribbon.md)

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra un modello personalizzato di base.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> </dl>

 

 





