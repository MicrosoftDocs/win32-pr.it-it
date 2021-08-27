---
description: Genera dichiarazioni di implementazione per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: Elemento subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1326750ece2f8dceff171890d107a7efad5f7432be2c201bf182e4406cb7fe6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097101"
---
# <a name="subscriptionfunctiondeclarations-element"></a>Elemento subscriptionFunctionDeclarations

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
| [**Operazione**](operation.md)<br/>                         | Specifica un'operazione per cui deve essere generato il codice.<br/> <br/>                       |
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
| [**File**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




