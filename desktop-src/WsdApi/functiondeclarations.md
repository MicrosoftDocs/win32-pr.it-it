---
description: Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: Elemento functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508cbac6d220c0ebdee0c6306d5f8a8ab5f26770
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998818"
---
# <a name="functiondeclarations-element"></a>Elemento functionDeclarations

Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.

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
| [**async**](async.md)<br/>         | Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.<br/> <br/>         |
| [**Eventi**](events.md)<br/>       | Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.<br/> <br/> |
| [**Operazione**](operation.md)<br/> | Specifica un'operazione per cui deve essere generato il codice.<br/> <br/>                                        |
| [**Porttype**](porttype.md)<br/>   | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/>                                       |



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
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento genera dichiarazioni di funzioni membro corrispondenti alle operazioni chiamate dal contratto. Queste dichiarazioni sono in un formato appropriato per l'utilizzo da parte di un compilatore C++ e vengono in genere usate nei file con estensione cpp.

Esempio:

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




