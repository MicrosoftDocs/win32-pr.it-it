---
description: URI che rappresenta l'identificatore del servizio.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995108"
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



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




