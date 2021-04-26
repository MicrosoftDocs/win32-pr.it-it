---
description: Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento deallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994938"
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
| [**stubDefinitions**](stubdefinitions.md)<br/> | Genera implementazioni per funzioni stub per operazioni di tipo porta.<br/> <br/> |



## <a name="remarks"></a>Commenti

Il tipo di deallocatore deve essere racchiuso in una coppia di <deallocator></deallocator> tag. Le stringhe seguenti sono valori deallocatori validi:

-   Nessuno
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   free
-   eliminare
-   deleteArray
-   Versione

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




