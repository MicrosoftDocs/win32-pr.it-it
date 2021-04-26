---
description: Genera implementazioni per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: subscriptionProxyFunctionImplementations - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995318"
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
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




