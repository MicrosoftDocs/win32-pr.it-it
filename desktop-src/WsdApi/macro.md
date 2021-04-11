---
description: Definisce il testo o CDATA da riutilizzare nell'elemento include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: elemento macro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231814"
---
# <a name="macro-element"></a>elemento macro

Definisce il testo o CDATA da riutilizzare nell'elemento [**include**](include.md) .

## <a name="usage"></a>Utilizzo

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Attributi



| Attributo           | Type                         | Obbligatoria       | Descrizione                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **nome**<br/> | stringa di caratteri \_<br/> | Sì<br/> | Nome della macro.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

WsdCodeGen definisce una macro denominata **DoNotModify**. Quando questa macro è inclusa, il codice generato contiene un blocco di commento con visibilità elevata che indica agli sviluppatori di non modificare il codice generato.

Nel codice XML seguente viene illustrato come includere la macro **DoNotModify** . Questo XML può essere aggiunto a un file di configurazione XML per WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




