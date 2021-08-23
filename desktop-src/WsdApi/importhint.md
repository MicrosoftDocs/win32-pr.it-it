---
description: Specifica il percorso di download per una direttiva wsdl:import che non specifica in modo esplicito un percorso.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: Elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bff41d5f58e8e3041873d6283afc032409855a53013e721efad6c5986c6c6ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732241"
---
# <a name="importhint-element"></a>Elemento importHint

Specifica il percorso di download per una \<wsdl:import> direttiva che non specifica in modo esplicito un percorso.

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
| [**Posizione**](location.md)<br/>   | Percorso del file da importare. Il percorso può essere un percorso relativo, un percorso assoluto o un URL HTTP.<br/> <br/> |
| [**Namespace**](namespace.md)<br/> | Spazio dei nomi da importare. Deve corrispondere allo spazio dei nomi specificato \<wsdl:import> nell'elemento .<br/> <br/>     |



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
| [**Wsdl**](wsdl.md)<br/> | Specifica un file WSDL da elaborare per le informazioni sul contratto.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




