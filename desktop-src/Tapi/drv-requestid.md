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
# <a name="drv_requestid"></a>DRV \_ RequestId

Il tipo di dati **drv \_ RequestId** viene usato per fornire un identificatore univoco per una richiesta al provider di servizi. Un valore di questo tipo viene passato come parametro a ogni funzione che consente l'operazione asincrona. Se l'operazione è asincrona, il provider di servizi restituisce questo valore come valore restituito della funzione. Ogni volta che il provider di servizi contrassegna una richiesta come asincrona in questo modo, deve infine segnalare che l'operazione è stata completata chiamando la funzione di callback [*\_ proc di completamento*](/windows/win32/api/tspi/nc-tspi-async_completion) .

TAPI garantisce che i **valori \_ RequestId di DRV** che fornisce siano strettamente positivi, ovvero tra i valori di 0x00000001 e 0x7FFFFFFF, inclusi. Inoltre, i valori sono univoci in quanto nessun valore restituito da una funzione per contrassegnare la richiesta come asincrona verrà riutilizzato prima del completamento dell'operazione.

 

 
