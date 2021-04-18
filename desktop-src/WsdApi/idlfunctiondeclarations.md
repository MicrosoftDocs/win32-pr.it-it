---
description: Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afa43676898231f739804185b8bf5d6e2b4faf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310302"
---
# <a name="idlfunctiondeclarations-element"></a>elemento idlFunctionDeclarations

Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>         | Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.<br/> <br/>         |
| [**eventArg**](eventarg.md)<br/>   | Specifica se gli argomenti dell'evento correlati sono inclusi nelle funzioni generate.<br/> <br/>               |
| [**eventi**](events.md)<br/>       | Specifica se gli eventi correlati sono inclusi nelle funzioni generate.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.<br/> <br/> |
| [**operazione**](operation.md)<br/> | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
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

Questo elemento genera dichiarazioni di funzioni membro corrispondenti alle operazioni chiamate dal contratto. Queste dichiarazioni sono in un formato appropriato per l'utilizzo da parte del compilatore MIDL e vengono in genere utilizzate nei file IDL.

Esempio:

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




