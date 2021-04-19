---
description: Non è necessario un provider per supportare le operazioni di istanza parziale. Tuttavia, un provider deve supportare tutta la semantica di un'operazione di istanza parziale, elaborare un'istanza completa o restituire il parametro WBEM \_ E non \_ supportato \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Supporto di Partial-Instance operazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309874"
---
# <a name="supporting-partial-instance-operations"></a>Supporto di Partial-Instance operazioni

Non è necessario un provider per supportare le operazioni di istanza parziale. Tuttavia, un provider deve supportare tutta la semantica di un'operazione di istanza parziale, elaborare un'istanza completa o restituire il **parametro WBEM \_ E non \_ supportato \_**.

Quando si crea un provider che supporta operazioni di istanza parziale, è necessario rispettare le regole seguenti:

-   Riutilizzare lo stesso oggetto di contesto inviato da WMI al provider. WMI utilizza il \_ \_ \_ valore denominato "Get ext \_ client \_ Request" per evitare deadlock e rimuove il client prima di inviare l'oggetto di contesto a un provider.
-   Per le chiamate rientranti in WMI che non richiedono un'operazione di istanza parziale, assicurarsi di passare di nuovo lo stesso oggetto di contesto senza alcuna modifica. WMI riceve l'oggetto di contesto senza il \_ \_ \_ valore denominato "Get ext \_ client \_ Request" impostato ed Elimina tutti i valori denominati associati a operazioni di istanze parziali dall'oggetto context prima di passarli ad altri provider. La mancata modifica dell'oggetto context impedisce ad altri provider di ricevere operazioni di recupero di istanze parziali destinate a un oggetto diverso e non correlato.
-   Per eseguire un'operazione di istanza parziale rientrante durante l'esecuzione di una richiesta, impostare il \_ \_ \_ valore denominato "Get ext \_ client \_ Request" e la proprietà Clear. Facoltativamente, è possibile modificare le proprietà nel \_ \_ \_ valore denominato "Get ext \_ Properties" prima di inviare di nuovo l'oggetto context a WMI con la chiamata rientrante.
-   Non accedere all'oggetto di contesto dopo che è stato restituito a WMI durante una chiamata rientrante. è possibile che altri provider modifichino gli elenchi di proprietà o altri valori durante la rientranza. È possibile esaminare o modificare l'oggetto contesto solo per la durata della chiamata [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) implementata.

 

 



