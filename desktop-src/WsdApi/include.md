---
description: Include il contenuto di una macro o di un file nell'output generato.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8029f58d9d1627a315fcfd02aa4f311d0a717361abf587aa92c52134b78e5958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856591"
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
| **file**<br/>  | stringa di \_ caratteri<br/> | No<br/> | Percorso del file da includere.<br/> <br/>  |
| **macro**<br/> | stringa di \_ caratteri<br/> | No<br/> | Nome della macro da includere.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**File**](file.md)<br/> | Indica al generatore di codice di generare un file e specifica il nome del file di output.<br/> <br/> |



## <a name="remarks"></a>Commenti

È necessario **specificare l'attributo macro** o **l'attributo** file. Non specificare entrambi gli attributi.

WsdCodeGen definisce una macro denominata **DoNotModify**. Quando questa macro è inclusa, il codice generato contiene un blocco di commenti ad alta visibilità che indica agli sviluppatori di non modificare il codice generato.

## <a name="examples"></a>Esempio

Il codice XML seguente illustra come includere la macro **DoNotModify.** Questo codice XML può essere aggiunto a un file di configurazione XML per WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




