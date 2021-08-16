---
description: Definisce un servizio da ospitare in una funzione del generatore host.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08479e88214e5fe6d1fbbb6ff5a3fffb7bb2047e8b7ca08cde92d64dd7dd6b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130793"
---
# <a name="hostedservice-element"></a>elemento hostedService

Definisce un servizio da ospitare in una funzione del generatore host.

## <a name="usage"></a>Utilizzo

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                     | Descrizione                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>     | Specifica il nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.<br/> <br/> |
| [**Porttype**](porttype.md)<br/>     | Tipo di porta per cui deve essere generato il codice.<br/> <br/>                                                                                                       |
| [**proxyClass**](proxyclass.md)<br/> | Nome della classe da generare dalla funzione del generatore.<br/> <br/>                                                                                                      |
| [**ServiceID**](serviceid.md)<br/>   | URI che rappresenta l'identificatore del servizio.<br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**File**](file.md)<br/> | Specifica del file di output per il generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




