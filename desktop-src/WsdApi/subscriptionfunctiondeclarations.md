---
description: Genera dichiarazioni di implementazione per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: elemento subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8957dcec6133d98830659fa76e2b7939079d3c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234315"
---
# <a name="subscriptionfunctiondeclarations-element"></a>elemento subscriptionFunctionDeclarations

Genera dichiarazioni di implementazione per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.

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
| **Extensible**<br/> | boolean<br/> | No<br/> | Possibilità di aggiungere punti di estensibilità alle funzioni e alle interfacce. Questo valore è sempre impostato su true.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                           | Descrizione                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | Specifica il nome dell'interfaccia di notifica utilizzata con le sottoscrizioni di eventi.<br/> <br/> |
| [**operazione**](operation.md)<br/>                         | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                       |
| [**portType**](porttype.md)<br/>                           | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/>                      |



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
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




