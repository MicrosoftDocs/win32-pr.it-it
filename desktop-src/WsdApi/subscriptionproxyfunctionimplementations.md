---
description: Genera implementazioni per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: subscriptionProxyFunctionImplementations - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0abc98e0e9bebd4ff2185d669402c0dae025c07bc4af84be3116dda97b6657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991571"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a>subscriptionProxyFunctionImplementations - elemento

Genera implementazioni per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a>Attributi



| Attributo                 | Type               | Obbligatoria      | Descrizione                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Extensible**<br/> | boolean<br/> | No<br/> | Possibilità di aggiungere punti di estendibilità a funzioni e interfacce. Questo valore è sempre impostato su true.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                           | Descrizione                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | Specifica il nome dell'interfaccia di notifica utilizzata con le sottoscrizioni di eventi.<br/> <br/> |
| [**Operazione**](operation.md)<br/>                         | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                       |
| [**Porttype**](porttype.md)<br/>                           | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/>                      |
| [**classe proxy**](proxyclass.md)<br/>                       | Specifica il nome della classe proxy lato client.<br/> <br/>                              |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
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



 

 




