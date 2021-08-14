---
title: Ribbon.QuickAccessToolbar - proprietà
description: Rappresenta un contenitore per la barra di accesso rapido.
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Proprietà Ribbon.QuickAccessToolbar Windows barra multifunzione
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e1fa4cb5de43be2b7316d4ed1786c2a1325fa4468538e2ffea41d5d8c9ef0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202318"
---
# <a name="ribbonquickaccesstoolbar-property"></a>Ribbon.QuickAccessToolbar - proprietà

Rappresenta un contenitore per la barra di accesso rapido.

## <a name="usage"></a>Utilizzo

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Descrizione                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> | Deve verificarsi esattamente una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Barra multifunzione**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Può verificarsi una o più volte per ogni barra [**multifunzione.**](windowsribbon-element-ribbon.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per **l'elemento Ribbon.QuickAccessToolbar.**


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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





