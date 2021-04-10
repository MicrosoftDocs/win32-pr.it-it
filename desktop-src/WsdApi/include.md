---
description: Include il contenuto di una macro o di un file nell'output generato.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057951"
---
# <a name="include-element"></a>include - elemento

Include il contenuto di una macro o di un file nell'output generato.

## <a name="usage"></a>Utilizzo

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a>Attributi



| Attributo            | Type                         | Obbligatoria      | Descrizione                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| **file**<br/>  | stringa di caratteri \_<br/> | No<br/> | Percorso del file da includere.<br/> <br/>  |
| **macro**<br/> | stringa di caratteri \_<br/> | No<br/> | Nome della macro da includere.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**file**](file.md)<br/> | Indica al generatore di codice di generare un file e di specificare il nome del file di output.<br/> <br/> |



## <a name="remarks"></a>Commenti

È necessario specificare l'attributo **macro** o l'attributo **file** . Non specificare entrambi gli attributi.

WsdCodeGen definisce una macro denominata **DoNotModify**. Quando questa macro è inclusa, il codice generato contiene un blocco di commento con visibilità elevata che indica agli sviluppatori di non modificare il codice generato.

## <a name="examples"></a>Esempio

Nel codice XML seguente viene illustrato come includere la macro **DoNotModify** . Questo XML può essere aggiunto a un file di configurazione XML per WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




