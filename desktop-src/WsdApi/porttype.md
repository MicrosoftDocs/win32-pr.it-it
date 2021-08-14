---
description: Specifica il tipo di porta per cui deve essere generato il codice.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: elemento portType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7fc502b2d899998a7f3e0f199c7804856317744ec8d127fb712a3f98c3bd0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991651"
---
# <a name="porttype-element"></a>elemento portType

Specifica il tipo di porta per cui deve essere generato il codice.

## <a name="usage"></a>Utilizzo

``` syntax
<portType/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                                 | Descrizione                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/>                                    |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/>                                               |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Genera definizioni di struttura C per i tipi di messaggio.<br/> <br/>                                                                   |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Genera dichiarazioni di costanti C per le tabelle di XML Schema per i tipi di messaggio.<br/> <br/>                                             |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Genera costanti C per le tabelle di XML Schema per i tipi di messaggio.<br/> <br/>                                                         |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Genera dichiarazioni di costanti C per i tipi di porta.<br/> <br/>                                                                      |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Genera costanti C per i tipi di porta.<br/> <br/>                                                                                  |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.<br/> <br/>                                                |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Genera dichiarazioni per le funzioni stub per le operazioni sul tipo di porta.<br/> <br/>                                                    |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.<br/> <br/>                                                 |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Genera dichiarazioni di implementazione per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Genera dichiarazioni IDL per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Genera implementazioni per le funzioni proxy subscribe/unsubscribe per le operazioni di notifica del tipo di porta.<br/> <br/>             |



## <a name="remarks"></a>Commenti

Per impostazione predefinita, il codice viene generato per tutti i tipi di porta nei file di input WSDL.

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




