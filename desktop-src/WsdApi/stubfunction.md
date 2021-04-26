---
description: Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture operative nelle definizioni dei tipi di porta per le operazioni unidirezionale e bidirezionale.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: Elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f37aed20dae4f04eea087e3d1eac2d23369af
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994148"
---
# <a name="stubfunction-element"></a>Elemento stubFunction

Specifica se i riferimenti alle funzioni stub devono essere inclusi nelle strutture operative nelle definizioni dei tipi di porta per le operazioni unidirezionale e bidirezionale.

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

I riferimenti alle funzioni stub vengono usati negli scenari di hosting per operazioni unidireivi e bidireivi.

I valori validi per questo elemento sono 1 (riferimenti alle funzioni TRUE/stub inclusi) e 0 (false/nessun riferimento a funzioni stub incluse).

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




