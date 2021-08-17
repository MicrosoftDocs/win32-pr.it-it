---
description: Non è necessario un provider per supportare operazioni di istanza parziale. Tuttavia, un provider deve supportare tutta la semantica di un'operazione a istanza parziale, elaborare un'istanza completa o restituire WBEM \_ E \_ UNSUPPORTED \_ PARAMETER.
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Supporto di Partial-Instance operazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2043c09ca129acab6976cabda2b854be464d26036cb5b9df1bc5b82989ccc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922851"
---
# <a name="supporting-partial-instance-operations"></a>Supporto di Partial-Instance operazioni

Non è necessario un provider per supportare operazioni di istanza parziale. Tuttavia, un provider deve supportare tutta la semantica di un'operazione a istanza parziale, elaborare un'istanza completa o restituire **WBEM \_ E \_ UNSUPPORTED \_ PARAMETER**.

Quando si crea un provider che supporta operazioni a istanza parziale, è necessario osservare le regole seguenti:

-   Riutilizzare lo stesso oggetto contesto inviato da WMI al provider. WMI usa il valore denominato \_ \_ "GET EXT CLIENT REQUEST" per evitare deadlock e rimuove il client prima di inoltrare l'oggetto \_ \_ contesto a un \_ provider.
-   Per le chiamate rientranti a WMI che non richiedono un'operazione di istanza parziale, assicurarsi di passare nuovamente lo stesso oggetto di contesto senza alcuna modifica. WMI riceve l'oggetto contesto senza il set di valori denominati \_ \_ "GET \_ EXT \_ CLIENT REQUEST" ed elimina tutti i valori denominati associati alle operazioni di istanza parziale dall'oggetto contesto prima di passarlo ad \_ altri provider. La non modifica dell'oggetto contesto impedisce ad altri provider di ricevere operazioni di recupero di istanze parziali destinate a un oggetto diverso e non correlato.
-   Per eseguire un'operazione di istanza parziale rientrante durante l'esecuzione di una richiesta, impostare il valore denominato "GET EXT CLIENT REQUEST" mancante e \_ \_ \_ \_ \_ deselezionare la proprietà. Facoltativamente, è possibile modificare le proprietà nel valore denominato "GET EXT PROPERTIES" prima di inviare nuovamente l'oggetto contesto a WMI con \_ \_ la chiamata \_ \_ rientrante.
-   Non accedere all'oggetto contesto dopo che è stato restituito a WMI durante una chiamata rientrante; altri provider possono modificare gli elenchi di proprietà o altri valori durante la reentrancy. È possibile esaminare o modificare l'oggetto contesto solo per la durata della chiamata [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) implementata.

 

 



