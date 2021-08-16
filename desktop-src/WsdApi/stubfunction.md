---
description: Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni unidirezionale e bidirezionale.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: Elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9304aa33bd193edc631949a93e1d770a1fade3d0c5726a9f2d897ea1862476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552412"
---
# <a name="stubfunction-element"></a>Elemento stubFunction

Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture delle operazioni nelle definizioni dei tipi di porta per le operazioni unidirezionale e bidirezionale.

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

I riferimenti alle funzioni stub vengono usati negli scenari di hosting per le operazioni unidirevi e bidire utente.

I valori validi per questo elemento sono 1 (sono inclusi riferimenti a funzioni TRUE/stub) e 0 (false/nessun riferimento alla funzione stub incluso).

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




