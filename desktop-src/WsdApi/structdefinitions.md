---
description: Genera definizioni della struttura C per i tipi noti.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313664"
---
# <a name="structdefinitions-element"></a>elemento structDefinitions

Genera definizioni della struttura C per i tipi noti.

## <a name="usage"></a>Utilizzo

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Alla maggior parte del codice generato e del codice dell'applicazione viene fatto riferimento a strutture per i tipi noti. Questo elemento viene utilizzato per generare file di inclusione. Questo elemento deve essere eseguito dopo un elemento [**structDeclarations**](structdeclarations.md) in modo che i riferimenti tra le strutture vengano gestiti correttamente.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




