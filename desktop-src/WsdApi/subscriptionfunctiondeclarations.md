---
description: Genera dichiarazioni di implementazione per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: subscriptionFunctionDeclarations - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995458"
---
# <a name="subscriptionfunctiondeclarations-element"></a>subscriptionFunctionDeclarations - elemento

Genera dichiarazioni di implementazione per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
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



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
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



 

 




