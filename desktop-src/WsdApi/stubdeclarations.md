---
description: Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319802"
---
# <a name="stubdeclarations-element"></a>elemento stubDeclarations

Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.

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
| [**eventi**](events.md)<br/>       | Specifica se gli eventi correlati sono inclusi nelle funzioni generate.<br/> <br/> |
| [**operazione**](operation.md)<br/> | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                 |
| [**portType**](porttype.md)<br/>   | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/>                |



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
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




