---
description: Specifica il deallocatore di tipo che deve essere utilizzato da una funzione stub delle operazioni.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ce2902bbfac16cb096da334cf3f22a12c68e3720d575fa303b8f3b133c9328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991691"
---
# <a name="operationdeallocator-element"></a>elemento operationDeallocator

Specifica il deallocatore di tipo che deve essere usato dalla funzione stub di un'operazione.

## <a name="usage"></a>Utilizzo

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Attributi



| Attributo                  | Type                         | Obbligatoria       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **deallocatore**<br/> | stringa di \_ caratteri<br/> | Sì<br/> | Deallocatore da utilizzare per l'operazione.<br/> <br/> Le stringhe seguenti sono valori validi.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span><dt>***Nessuno****</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> <dt>***WSDFreeLinkedMemory***</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> <dt>****CoTaskMemFree****</dt> <span id="free"></span> <span id="FREE"></span> <dt>***Gratuito****</dt> <span id="delete"></span> <span id="DELETE"></span> <dt>****elimina****</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> <dt>****deleteArray****</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> <dt>****Versione****</dt> </dl> |
| **operation**<br/>   | stringa di \_ caratteri<br/> | Sì<br/> | Nome dell'operazione.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                               | Descrizione                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Genera implementazioni per le funzioni stub per le operazioni sul tipo di porta.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




