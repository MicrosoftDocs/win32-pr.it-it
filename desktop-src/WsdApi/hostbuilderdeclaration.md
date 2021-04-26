---
description: Genera una dichiarazione per una funzione che crea un host tipidato.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: elemento hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf3ddd474b4000b053b49157f1fc4b2eb399d34
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994908"
---
# <a name="hostbuilderdeclaration-element"></a>elemento hostBuilderDeclaration

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
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




