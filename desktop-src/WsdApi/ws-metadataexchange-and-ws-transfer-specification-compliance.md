---
description: Prima del 2006 agosto WS-MetadataExchange definito il proprio metodo Get Metadata Exchange, utilizzato dal profilo Devices per i servizi Web (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Conformità delle specifiche WS-MetadataExchange e WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130955"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>Conformità delle specifiche WS-MetadataExchange e WS-Transfer

Prima del 2006 agosto, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) definisce il proprio metodo [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange, utilizzato dal [profilo Devices per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). La specifica WS-MetadataExchange versione 1,1 ha sostituito questo metodo con il metodo Get definito nella specifica WS-Transfer.

Nel modello corrente WS-Transfer fornisce il metodo [Get](get--metadata-exchange--http-request-and-message.md) e non fa riferimento al tipo del corpo. WS-MetadataExchange descrive il formato del corpo e un meccanismo per la creazione di pacchetti di più parti di metadati in una singola risposta e DPWS descrive parti specifiche di metadati che un servizio deve includere in una risposta ai metadati.

WSDAPI non supporta completamente la specifica WS-Transfer. Poiché per i dispositivi è necessario solo il metodo [Get](get--metadata-exchange--http-request-and-message.md) , non sono state implementate altre parti di WS-Transfer. Inoltre, WSDAPI non implementa il metodo GetMetadata facoltativo descritto in WS-MetadataExchange.

 

 



