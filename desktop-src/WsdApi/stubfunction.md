---
description: Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni unidirezionali e bidirezionali.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7282e7280c8d701710094b70b84a65756f7230ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233107"
---
# <a name="stubfunction-element"></a>elemento stubFunction

Specifica se i riferimenti alle funzioni Stub devono essere inclusi nelle strutture dell'operazione nelle definizioni dei tipi di porta per le operazioni unidirezionali e bidirezionali.

## <a name="usage"></a>Utilizzo

``` syntax
<stubFunction/>
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

I riferimenti alle funzioni stub vengono utilizzati negli scenari di hosting per operazioni unidirezionali e bidirezionali.

I valori validi per questo elemento sono 1 (i riferimenti alle funzioni TRUE/stub sono inclusi) e 0 (FALSE/nessun riferimento di funzione stub incluso).

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




