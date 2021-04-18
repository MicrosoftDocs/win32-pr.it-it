---
description: Genera una funzione che crea un host tipizzato.
ms.assetid: 2b4a4016-cc5d-4912-8e08-ce3a11ab0a06
title: elemento hostBuilderImplementation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9cfabb9ab4193162044420fc3980f0bbeeb55a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310304"
---
# <a name="hostbuilderimplementation-element"></a>elemento hostBuilderImplementation

Genera una funzione che crea un host tipizzato.

## <a name="usage"></a>Utilizzo

``` syntax
<hostBuilderImplementation>
  child elements
</hostBuilderImplementation>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                           | Descrizione                                                      |
|---------------------------------------------------|------------------------------------------------------------------|
| [**Servizio ospitato**](hostedservice.md)<br/> | Servizio da includere per l'host. <br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
hostedService+
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




