---
description: Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: elemento functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231672"
---
# <a name="functiondeclarations-element"></a>elemento functionDeclarations

Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>         | Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.<br/> <br/>         |
| [**eventi**](events.md)<br/>       | Specifica se gli eventi correlati sono inclusi nelle funzioni generate.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.<br/> <br/> |
| [**operazione**](operation.md)<br/> | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento genera dichiarazioni di funzioni membro corrispondenti alle operazioni chiamate dal contratto. Queste dichiarazioni sono in un formato appropriato per l'utilizzo da un compilatore C++ e vengono in genere utilizzate nei file con estensione cpp.

Esempio:

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




