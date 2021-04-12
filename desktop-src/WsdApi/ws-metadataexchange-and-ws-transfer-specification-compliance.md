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
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a><span data-ttu-id="45d9b-103">Conformità delle specifiche WS-MetadataExchange e WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="45d9b-103">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>

<span data-ttu-id="45d9b-104">Prima del 2006 agosto, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) definisce il proprio metodo [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange, utilizzato dal [profilo Devices per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="45d9b-104">Before August 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) defined its own [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange method, which was used by [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="45d9b-105">La specifica WS-MetadataExchange versione 1,1 ha sostituito questo metodo con il metodo Get definito nella specifica WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="45d9b-105">The WS-MetadataExchange specification version 1.1 replaced this method with the Get method defined in the WS-Transfer specification.</span></span>

<span data-ttu-id="45d9b-106">Nel modello corrente WS-Transfer fornisce il metodo [Get](get--metadata-exchange--http-request-and-message.md) e non fa riferimento al tipo del corpo.</span><span class="sxs-lookup"><span data-stu-id="45d9b-106">In the current model, WS-Transfer provides the [Get](get--metadata-exchange--http-request-and-message.md) method and makes no reference to the type of the body.</span></span> <span data-ttu-id="45d9b-107">WS-MetadataExchange descrive il formato del corpo e un meccanismo per la creazione di pacchetti di più parti di metadati in una singola risposta e DPWS descrive parti specifiche di metadati che un servizio deve includere in una risposta ai metadati.</span><span class="sxs-lookup"><span data-stu-id="45d9b-107">WS-MetadataExchange describes the format of the body and a mechanism for packaging multiple pieces of metadata in a single response, and DPWS describes specific pieces of metadata that a service should include in a metadata response.</span></span>

<span data-ttu-id="45d9b-108">WSDAPI non supporta completamente la specifica WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="45d9b-108">WSDAPI does not fully support the WS-Transfer specification.</span></span> <span data-ttu-id="45d9b-109">Poiché per i dispositivi è necessario solo il metodo [Get](get--metadata-exchange--http-request-and-message.md) , non sono state implementate altre parti di WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="45d9b-109">Because only the [Get](get--metadata-exchange--http-request-and-message.md) method is required for devices, no other portions of WS-Transfer have been implemented.</span></span> <span data-ttu-id="45d9b-110">Inoltre, WSDAPI non implementa il metodo GetMetadata facoltativo descritto in WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="45d9b-110">Also, WSDAPI does not implement the optional GetMetadata method described in WS-MetadataExchange.</span></span>

 

 



