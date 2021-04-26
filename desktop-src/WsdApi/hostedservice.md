---
description: Definisce un servizio da ospitare in una funzione del generatore di host.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994788"
---
# <a name="hostedservice-element"></a>elemento hostedService

Definisce un servizio da ospitare in una funzione del generatore di host.

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
| [**Codename**](codename.md)<br/>     | Specifica il nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome in codice viene generato dal nome completo del tipo di porta.<br/> <br/> |
| [**Porttype**](porttype.md)<br/>     | Tipo di porta per cui deve essere generato il codice.<br/> <br/>                                                                                                       |
| [**classe proxy**](proxyclass.md)<br/> | Nome della classe da generare dalla funzione del generatore.<br/> <br/>                                                                                                      |
| [**SERVICEID**](serviceid.md)<br/>   | URI che rappresenta l'identificatore del servizio.<br/> <br/>                                                                                                      |



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
| [**ﬁle**](file.md)<br/> | Specifica del file di output per il generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




