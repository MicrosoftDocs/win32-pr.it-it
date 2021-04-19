---
description: URI che rappresenta l'identificatore del servizio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318486"
---
# <a name="serviceid-element"></a>Elemento ServiceID

URI che rappresenta l'identificatore del servizio.

## <a name="usage"></a>Utilizzo

``` syntax
<ServiceID/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                             | Descrizione                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**host**](host.md)<br/>     | Definisce gli elementi **ServiceID** e [**types**](types.md) per l'host del servizio. Se non viene specificato in modo esplicito, WSDAPI non fornirà dati predefiniti in risposta alle richieste di metadati.<br/> <br/>                                                                                                                     |
| [**ospitato**](hosted.md)<br/> | Definisce gli elementi **ServiceID** e [**types**](types.md) per i servizi forniti da questo host del servizio. Ogni servizio fornito da questo host del servizio deve disporre di informazioni relative all'elemento [**ospitato**](hosted.md) per garantire che il servizio venga pubblicato correttamente nelle risposte alle richieste di metadati.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




