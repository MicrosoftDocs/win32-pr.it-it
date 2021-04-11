---
description: Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento deallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226928"
---
# <a name="deallocator-element"></a>elemento deallocator

Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.

## <a name="usage"></a>Utilizzo

``` syntax
<deallocator/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                               | Descrizione                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Genera implementazioni per le funzioni stub per le operazioni di tipo porta.<br/> <br/> |



## <a name="remarks"></a>Commenti

Il tipo di deallocatore deve essere racchiuso in una coppia di <deallocator></deallocator> tag. Le stringhe seguenti sono valori di deallocator validi:

-   Nessuno
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   free
-   eliminare
-   deleteArray
-   Versione

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




