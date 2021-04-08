---
description: Definisce un servizio da ospitare in una funzione del generatore host.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento servizio ospitato
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880634"
---
# <a name="hostedservice-element"></a>elemento servizio ospitato

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
| [**codeName**](codename.md)<br/>     | Specifica il nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Tipo di porta per il quale deve essere generato il codice.<br/> <br/>                                                                                                       |
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
| [**file**](file.md)<br/> | Specifica del file di output per il generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




