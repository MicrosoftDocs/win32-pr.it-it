---
title: Ribbon. QuickAccessToolbar, proprietà
description: Rappresenta un contenitore per la barra di accesso rapido (QAT).
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. QuickAccessToolbar
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400264"
---
# <a name="ribbonquickaccesstoolbar-property"></a>Ribbon. QuickAccessToolbar, proprietà

Rappresenta un contenitore per la barra di accesso rapido (QAT).

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

Può verificarsi una o più volte per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per l'elemento **Ribbon. QuickAccessToolBar** .


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



 

 





