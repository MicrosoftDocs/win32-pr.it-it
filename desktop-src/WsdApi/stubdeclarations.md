---
description: Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: Elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 846cea00438a5e2571e0e5c6a2b4af2a5ec519071ece2fa3570e0281fc9a22b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991591"
---
# <a name="stubdeclarations-element"></a>Elemento stubDeclarations

Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Eventi**](events.md)<br/>       | Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.<br/> <br/> |
| [**Operazione**](operation.md)<br/> | Specifica un'operazione per cui deve essere generato il codice.<br/> <br/>                 |
| [**Porttype**](porttype.md)<br/>   | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/>                |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**File**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




