---
description: Specifica un'operazione per la quale deve essere generato il codice.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: elemento operation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab38721d1eb0d32c2ed7209dde872a83b29a523942ac7b91ca76f479ce5d51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502191"
---
# <a name="operation-element"></a>elemento operation

Specifica un'operazione per la quale deve essere generato il codice.

## <a name="usage"></a>Utilizzo

``` syntax
<operation/>
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

È possibile che venga specificato un numero qualsiasi di operazioni. Se non viene specificata alcuna operazione, viene generato codice per tutte le operazioni in tutti i tipi di porta pertinenti. **L'uso dell'elemento** operation limiterà i metodi generati a quelli contenuti nell'operazione.

Ad esempio, una stampante supporta queste operazioni, tra le altre:

-   **PrintJobByPost**
-   **PrintJobByReference**
-   **CancelJob**
-   **GetJobElements**
-   **GetActiveJobs**
-   **GetJobHistory**
-   **SubscribeToPrinterConfigChange**
-   **UnsubscribeToPrinterConfigChange**

Tuttavia, per includere solo i metodi correlati alle operazioni **PrintJobByPost** e **GetJobElements,** lo script di generazione del codice userà gli elementi [**idlFunctionDeclarations**](idlfunctiondeclarations.md) come indicato di seguito:

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

Vengono generate dichiarazioni di funzione idl per tutti i metodi associati alle due operazioni , ad esempio **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** e **EndGetJobElements**.

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




