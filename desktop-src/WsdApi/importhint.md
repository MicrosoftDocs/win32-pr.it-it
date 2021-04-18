---
description: 'Specifica il percorso di download per un <WSDL: Import> direttiva che non specifica in modo esplicito una posizione.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310301"
---
# <a name="importhint-element"></a>elemento importHint

Specifica il percorso di download per un <WSDL: Import> direttiva che non specifica in modo esplicito una posizione.

## <a name="usage"></a>Utilizzo

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**percorso**](location.md)<br/>   | Percorso del file da importare. Il percorso può essere un percorso relativo, un percorso assoluto o un URL HTTP.<br/> <br/> |
| [**nameSpace**](namespace.md)<br/> | Spazio dei nomi da importare. Deve corrispondere allo spazio dei nomi specificato nell'elemento <WSDL: Import>.<br/> <br/>     |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**WSDL**](wsdl.md)<br/> | Specifica un file WSDL da elaborare per le informazioni sul contratto.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




