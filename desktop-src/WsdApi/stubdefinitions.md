---
description: Genera implementazioni per funzioni stub per operazioni di tipo porta.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: Elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42c60b071c901538122751f6e92cfd7049f7be88
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994688"
---
# <a name="stubdefinitions-element"></a>Elemento stubDefinitions

Genera implementazioni per funzioni stub per operazioni di tipo porta.

## <a name="usage"></a>Utilizzo

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                         | Descrizione                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**deallocatore**](deallocator.md)<br/>                   | Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.<br/> <br/>                                 |
| [**eventArg**](eventarg.md)<br/>                         | Specifica se gli argomenti di evento correlati vengono inclusi nelle funzioni generate.<br/> <br/>               |
| [**Eventi**](events.md)<br/>                             | Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>                       | Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.<br/> <br/> |
| [**Operazione**](operation.md)<br/>                       | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                        |
| [**operationDeallocator**](operationdeallocator.md)<br/> | Specifica il tipo di deallocatore che deve essere usato dalla funzione stub di un'operazione.<br/> <br/>                    |
| [**Porttype**](porttype.md)<br/>                         | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/>                                       |
| [**classe server**](serverclass.md)<br/>                   | Specifica il nome della classe server sul lato host.<br/> <br/>                                                |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




