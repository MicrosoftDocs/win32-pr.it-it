---
description: URI che rappresenta l'identificatore del servizio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dc6ac1da57109f4f5671caf16a49b3a6174e7bfb63335d5ba15a548d7135990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756741"
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
| [**Host**](host.md)<br/>     | Definisce gli elementi **ServiceID** e [**Types per**](types.md) l'host del servizio. Se non viene specificato in modo esplicito, WSDAPI non fornisce dati predefiniti in risposta alle richieste di metadati.<br/> <br/>                                                                                                                     |
| [**Ospitato da**](hosted.md)<br/> | Definisce gli elementi **ServiceID** e [**Types**](types.md) per i servizi forniti da questo host del servizio. Ogni servizio fornito da questo host [](hosted.md) del servizio deve avere le proprie informazioni sugli elementi ospitati per garantire che il servizio venga pubblicato correttamente in risposta alle richieste di metadati.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




