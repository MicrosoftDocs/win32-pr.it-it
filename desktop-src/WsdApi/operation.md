---
description: Specifica un'operazione per la quale deve essere generato il codice.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: Operation-elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049806"
---
# <a name="operation-element"></a>Operation-elemento

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
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/>                                    |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/>                                               |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Genera definizioni della struttura C per i tipi di messaggio.<br/> <br/>                                                                   |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Genera dichiarazioni di costanti C per XML Schema tabelle per i tipi di messaggio.<br/> <br/>                                             |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Genera costanti C per XML Schema tabelle per i tipi di messaggio.<br/> <br/>                                                         |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Genera dichiarazioni di costanti C per i tipi di porta.<br/> <br/>                                                                      |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Genera costanti C per i tipi di porta.<br/> <br/>                                                                                  |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/>                                                |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.<br/> <br/>                                                    |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.<br/> <br/>                                                 |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Genera dichiarazioni di implementazione per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Genera dichiarazioni IDL per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Genera implementazioni per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.<br/> <br/>             |



## <a name="remarks"></a>Commenti

È possibile specificare un numero qualsiasi di operazioni. Se non viene specificata alcuna operazione, il codice viene generato per tutte le operazioni in tutti i tipi di porta pertinenti. Se si usa l'elemento **Operation** , i metodi generati verranno limitati a quelli contenuti nell'operazione.

Una stampante, ad esempio, supporta queste operazioni tra le altre:

-   **PrintJobByPost**
-   **PrintJobByReference**
-   **CancelJob**
-   **GetJobElements**
-   **GetActiveJobs**
-   **GetJobHistory**
-   **SubscribeToPrinterConfigChange**
-   **UnsubscribeToPrinterConfigChange**

Tuttavia, per includere solo i metodi correlati alle operazioni **PrintJobByPost** e **GetJobElements** , lo script di generazione del codice utilizzerà gli elementi [**idlFunctionDeclarations**](idlfunctiondeclarations.md) come indicato di seguito:

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

Vengono generate le dichiarazioni di funzione IDL per tutti i metodi associati alle due operazioni, ad esempio **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** e **EndGetJobElements**.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




