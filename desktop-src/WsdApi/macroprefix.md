---
description: Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi .
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: Elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 970232b86aa226f16fa06cf2d3c9de40c156702c802c6f6254e45157e1df58ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130713"
---
# <a name="macroprefix-element"></a>Elemento macroPrefix

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
| [**Namespace**](namespace.md)<br/> | Spazio dei nomi da utilizzare per la generazione del codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento esegue l'override del prefisso URI predefinito usato per le macro generate. Ad esempio, se il prefisso della macro è "AV" e il nome è "Tuner", la macro generata per il nome completo \_ sarà "AV \_ Tuner".

Per impostazione predefinita, il codice generato crea un prefisso di macro preferito dall'URI.

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




