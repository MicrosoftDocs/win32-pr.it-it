---
description: Genera una dichiarazione per una funzione che crea un host tipizzato.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: elemento hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316980"
---
# <a name="hostbuilderdeclaration-element"></a>elemento hostBuilderDeclaration

Genera una dichiarazione per una funzione che crea un host tipizzato.

## <a name="usage"></a>Utilizzo

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**interfaccia**](interface.md)<br/> | Nome dell'interfaccia del servizio da includere per l'host. Il valore di questo elemento deve corrispondere al valore dell'elemento figlio dell' [**interfaccia**](interface.md) di [**servizio ospitato**](hostedservice.md). <br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
interface+
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



 

 




