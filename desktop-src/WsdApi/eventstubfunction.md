---
description: Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni di notifica.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: elemento eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80777a53d37e7651559a09b8e8445d4314aaca63
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995888"
---
# <a name="eventstubfunction-element"></a>elemento eventStubFunction

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

I riferimenti alle funzioni stub si verificano negli scenari client per le operazioni di notifica (eventi).

I valori validi per questo elemento sono 1 (riferimenti alle funzioni TRUE/stub inclusi) e 0 (false/nessun riferimento a funzioni stub incluse).

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




