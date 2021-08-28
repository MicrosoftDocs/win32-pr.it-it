---
description: Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento deallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2617ce92dcd0c2763f77b0bc6f0fb5c1beea1c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881054"
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

Il tipo di deallocatore deve essere racchiuso in una coppia di &lt; tag &gt; </deallocator> deallocator. Le stringhe seguenti sono valori deallocatori validi:

-   Nessuno
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   free
-   eliminare
-   deleteArray
-   Versione

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




