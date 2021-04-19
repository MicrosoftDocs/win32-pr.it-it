---
description: Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310292"
---
# <a name="macroprefix-element"></a>elemento macroPrefix

Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi.

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
| [**nameSpace**](namespace.md)<br/> | Spazio dei nomi da utilizzare per la generazione del codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento sostituisce il prefisso URI predefinito usato per le macro generate. Se, ad esempio, il prefisso della macro è "AV \_ " e il nome è "Tuner", la macro generata per il nome completo sarà " \_ Tuner AV".

Per impostazione predefinita, il codice generato crea un prefisso di macro preferito dall'URI.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




