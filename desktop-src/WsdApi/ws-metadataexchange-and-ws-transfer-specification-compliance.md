---
description: Prima di agosto 2006, WS-MetadataExchange definito il proprio metodo di scambio dei metadati Get, che è stato usato da Profilo dispositivi per servizi Web (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: WS-MetadataExchange e WS-Transfer conformità alle specifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bec29d96b4ba3671f176349a56b891cd4d642762670fd16cf582da53208c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793971"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>WS-MetadataExchange e WS-Transfer conformità alle specifiche

Prima di agosto 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) ha definito il proprio metodo di scambio dei metadati [Get,](get--metadata-exchange--http-request-and-message.md) che è stato usato da [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). La WS-MetadataExchange specifica 1.1 ha sostituito questo metodo con il metodo Get definito nella WS-Transfer specificata.

Nel modello corrente, WS-Transfer il [metodo Get](get--metadata-exchange--http-request-and-message.md) e non fa riferimento al tipo del corpo. WS-MetadataExchange descrive il formato del corpo e un meccanismo per la creazione di pacchetti di più parti di metadati in una singola risposta e DPWS descrive parti specifiche di metadati che un servizio deve includere in una risposta ai metadati.

WSDAPI non supporta completamente la WS-Transfer specifica. Poiché per i dispositivi è necessario solo il metodo [Get,](get--metadata-exchange--http-request-and-message.md) non sono state WS-Transfer altre parti di dati. WSDAPI non implementa inoltre il metodo GetMetadata facoltativo descritto in WS-MetadataExchange.

 

 



