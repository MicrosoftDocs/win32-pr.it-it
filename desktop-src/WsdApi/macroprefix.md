---
description: Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi .
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998748"
---
# <a name="macroprefix-element"></a>macroPrefix - elemento

Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi .

## <a name="usage"></a>Utilizzo

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                   | Descrizione                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**Namespace**](namespace.md)<br/> | Spazio dei nomi da utilizzare per la generazione di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento esegue l'override del prefisso URI predefinito usato per le macro generate. Ad esempio, se il prefisso della macro è "AV " e il nome è "Tuner", la macro generata per il nome completo sarà \_ "AV \_ Tuner".

Per impostazione predefinita, il codice generato crea un prefisso di macro preferito dall'URI.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




