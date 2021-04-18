---
description: Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni di notifica.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: elemento eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe353f43d02eec68f29f3075cc445c1314c9762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313666"
---
# <a name="eventstubfunction-element"></a>elemento eventStubFunction

Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni di notifica.

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

I riferimenti alle funzioni stub si trovano in scenari client per le operazioni di notifica (eventi).

I valori validi per questo elemento sono 1 (i riferimenti alle funzioni TRUE/stub sono inclusi) e 0 (FALSE/nessun riferimento di funzione stub incluso).

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




