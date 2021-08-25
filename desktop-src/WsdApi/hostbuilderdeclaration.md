---
description: Genera una dichiarazione per una funzione che crea un host tipidato.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: Elemento hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172181313f4cc95500fe61a922b119bba1fc02515d0e912289eb6d9ac8f8fc86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794221"
---
# <a name="hostbuilderdeclaration-element"></a>Elemento hostBuilderDeclaration

Genera una dichiarazione per una funzione che crea un host tipidato.

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
| [**interfaccia**](interface.md)<br/> | Nome dell'interfaccia del servizio da includere per l'host. Il valore di questo elemento deve corrispondere al valore [**dell'elemento**](interface.md) figlio dell'interfaccia di [**hostedService.**](hostedservice.md) <br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
interface+
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**File**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




