---
description: Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni di notifica.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: eventStubFunction - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e0b42416adc29c75fcafffedabf558bf6455df6cecf2bfebc344f747fff971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856721"
---
# <a name="eventstubfunction-element"></a>eventStubFunction - elemento

Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni di notifica.

## <a name="usage"></a>Utilizzo

``` syntax
<eventStubFunction/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                       | Descrizione                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [**portTypeDefinitions**](porttypedefinitions.md)<br/> | Genera costanti C per i tipi di porta.<br/> <br/> |



## <a name="remarks"></a>Commenti

I riferimenti alle funzioni stub si verificano in scenari client per le operazioni di notifica (eventi).

I valori validi per questo elemento sono 1 (sono inclusi riferimenti a funzioni TRUE/stub) e 0 (false/nessun riferimento alla funzione stub incluso).

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




