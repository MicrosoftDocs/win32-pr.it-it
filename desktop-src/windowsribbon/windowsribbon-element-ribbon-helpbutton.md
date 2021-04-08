---
title: Ribbon. HelpButton, proprietà
description: Rappresenta un contenitore per il pulsante della guida.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. HelpButton
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742295"
---
# <a name="ribbonhelpbutton-property"></a>Ribbon. HelpButton, proprietà

Rappresenta un contenitore per il [pulsante della Guida](windowsribbon-controls-helpbutton.md).

## <a name="usage"></a>Utilizzo

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                           | Descrizione                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [**HelpButton**](windowsribbon-element-helpbutton.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Barra multifunzione**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente al massimo una volta per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base necessario per implementare un pulsante della guida della barra multifunzione.

Questa sezione di codice mostra la dichiarazione del comando **Ribbon. HelpButton** .


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



Questa sezione di codice mostra la dichiarazione di controllo **Ribbon. HelpButton** .


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





