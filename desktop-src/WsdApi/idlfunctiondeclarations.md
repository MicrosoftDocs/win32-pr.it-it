---
description: Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: Elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994738"
---
# <a name="idlfunctiondeclarations-element"></a>Elemento idlFunctionDeclarations

Genera dichiarazioni IDL per le funzioni proxy per le operazioni sul tipo di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                   | Descrizione                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>         | Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.<br/> <br/>         |
| [**eventArg**](eventarg.md)<br/>   | Specifica se gli argomenti dell'evento correlati vengono inclusi nelle funzioni generate.<br/> <br/>               |
| [**Eventi**](events.md)<br/>       | Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.<br/> <br/> |
| [**Operazione**](operation.md)<br/> | Specifica un'operazione per cui deve essere generato il codice.<br/> <br/>                                        |
| [**Porttype**](porttype.md)<br/>   | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento genera dichiarazioni di funzioni membro corrispondenti alle operazioni chiamate dal contratto. Queste dichiarazioni sono in un formato appropriato per l'utilizzo da parte del compilatore MIDL e vengono in genere usate nei file con estensione idl.

Esempio:

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




