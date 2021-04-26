---
description: Genera funzioni per creare proxy tipiati.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: Elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996468"
---
# <a name="proxybuilderimplementations-element"></a>Elemento proxyBuilderImplementations

Genera funzioni per creare proxy tipiati.

## <a name="usage"></a>Utilizzo

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                     | Descrizione                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>     | Nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.<br/> <br/> |
| [**Porttype**](porttype.md)<br/>     | Tipo di porta per cui deve essere generato il codice.<br/> <br/>                                                                                             |
| [**proxyClass**](proxyclass.md)<br/> | Nome della classe da generare dalla funzione del generatore di proxy.<br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
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



 

 




