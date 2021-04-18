---
description: Specifica il deallocatore del tipo che deve essere utilizzato da una funzione stub delle operazioni.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312684"
---
# <a name="operationdeallocator-element"></a>elemento operationDeallocator

Specifica il deallocatore di tipo che deve essere utilizzato dalla funzione stub di un'operazione.

## <a name="usage"></a>Utilizzo

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Attributi



| Attributo                  | Type                         | Obbligatoria       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **deallocatore**<br/> | stringa di caratteri \_<br/> | Sì<br/> | Il deallocatore da utilizzare per l'operazione.<br/> <br/> Le stringhe seguenti sono valori validi.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span>* * * * <dt>Nessuna *</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> * * * * * * * <dt>WSDFreeLinkedMemory *</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> * * * * * * * <dt>CoTaskMemFree *</dt> <span id="free"></span> <span id="FREE"></span> * * * * * * * * * * * * * * * * * <dt></dt> <span id="delete"></span> <span id="DELETE"></span> * * * * <dt>Elimina * *</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> * * * * * * <dt>deleteArray *</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> * * * * * * * <dt>Versione *</dt> * * * </dl> |
| **operation**<br/>   | stringa di caratteri \_<br/> | Sì<br/> | Nome dell'operazione.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                               | Descrizione                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




