---
description: Il tipo di dati DRV \_ RequestId viene usato per fornire un identificatore univoco per una richiesta al provider di servizi.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311901"
---
# <a name="drv_requestid"></a><span data-ttu-id="2d1c7-103">DRV \_ RequestId</span><span class="sxs-lookup"><span data-stu-id="2d1c7-103">DRV\_REQUESTID</span></span>

<span data-ttu-id="2d1c7-104">Il tipo di dati **drv \_ RequestId** viene usato per fornire un identificatore univoco per una richiesta al provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-104">The **DRV\_REQUESTID** datatype is used to supply a unique identifier for a request to the service provider.</span></span> <span data-ttu-id="2d1c7-105">Un valore di questo tipo viene passato come parametro a ogni funzione che consente l'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-105">A value of this type is passed as a parameter to every function that allows for asynchronous operation.</span></span> <span data-ttu-id="2d1c7-106">Se l'operazione è asincrona, il provider di servizi restituisce questo valore come valore restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-106">If the operation is asynchronous, the service provider returns this value as the return value of the function.</span></span> <span data-ttu-id="2d1c7-107">Ogni volta che il provider di servizi contrassegna una richiesta come asincrona in questo modo, deve infine segnalare che l'operazione è stata completata chiamando la funzione di callback [*\_ proc di completamento*](/windows/win32/api/tspi/nc-tspi-async_completion) .</span><span class="sxs-lookup"><span data-stu-id="2d1c7-107">Whenever the service provider flags a request as asynchronous in this way, it must eventually report the operation is complete by calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function.</span></span>

<span data-ttu-id="2d1c7-108">TAPI garantisce che i **valori \_ RequestId di DRV** che fornisce siano strettamente positivi, ovvero tra i valori di 0x00000001 e 0x7FFFFFFF, inclusi.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-108">TAPI ensures that the **DRV\_REQUESTID** values it supplies are strictly positive, that is, between the values of 0x00000001 and 0x7FFFFFFF, inclusive.</span></span> <span data-ttu-id="2d1c7-109">Inoltre, i valori sono univoci in quanto nessun valore restituito da una funzione per contrassegnare la richiesta come asincrona verrà riutilizzato prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-109">Furthermore, the values are unique in that no value returned from a function to flag the request as asynchronous will be re-used before the operation is reported complete.</span></span>

 

 
