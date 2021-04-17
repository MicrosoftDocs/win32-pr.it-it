---
title: Creazione di una clausola WHERE per il provider del registro di sistema
description: I punti principali da considerare durante la creazione di una clausola WHERE corretta per il provider del registro di sistema sono il fatto che ogni query di evento deve essere completa ed esplicita. Il mancato completamento e l'esplicito comporteranno un messaggio di errore.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d1c7031d376fbd6b9d946fb9e41561ce4c4b1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485740"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a><span data-ttu-id="25ff9-104">Creazione di una clausola WHERE per il provider del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="25ff9-104">Creating a WHERE clause for the registry provider</span></span>

<span data-ttu-id="25ff9-105">I punti principali da considerare durante la creazione di una clausola WHERE corretta per il provider del registro di sistema sono il fatto che ogni query di evento deve essere completa ed esplicita.</span><span class="sxs-lookup"><span data-stu-id="25ff9-105">The main points to consider when creating a proper WHERE clause for the System Registry provider is that each event query must be complete and explicit.</span></span> <span data-ttu-id="25ff9-106">Il mancato completamento e l'esplicito comporteranno un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="25ff9-106">Failure to be complete and explicit will result in an error message.</span></span>

<span data-ttu-id="25ff9-107">Per essere completa, ogni query di evento nel parametro *bstrQuery* di [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) deve contenere una clausola WHERE che include ognuna delle proprietà nella classe di evento specificata.</span><span class="sxs-lookup"><span data-stu-id="25ff9-107">To be complete, each event query in the *bstrQuery* parameter of [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) must contain a WHERE clause that includes each of the properties in the specified event class.</span></span>

<span data-ttu-id="25ff9-108">Nell'esempio seguente viene illustrato come impostare *bstrQuery* per la registrazione degli eventi di modifica della struttura ad albero nell'albero "HKEY \_ Local \_ Machine \\ software".</span><span class="sxs-lookup"><span data-stu-id="25ff9-108">The following example shows how to set *bstrQuery* to register for tree change events in the "HKEY\_LOCAL\_MACHINE\\Software" tree.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



<span data-ttu-id="25ff9-109">Per essere esplicito, il provider deve essere in grado di dedurre dalla query un elenco di valori possibili per ogni proprietà nella classe di evento.</span><span class="sxs-lookup"><span data-stu-id="25ff9-109">To be explicit, the provider should be able to infer from the query a list of possible values for every property in the event class.</span></span>

<span data-ttu-id="25ff9-110">Nell'esempio seguente viene illustrata la query di eventi che registra correttamente per gli eventi di modifica della struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="25ff9-110">The following example shows the event query that correctly registers for tree change events.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



<span data-ttu-id="25ff9-111">Di seguito è riportato un esempio di registrazione non corretta.</span><span class="sxs-lookup"><span data-stu-id="25ff9-111">The following is an example of an incorrect registration.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



<span data-ttu-id="25ff9-112">Poiché non esiste alcun modo per valutare i valori possibili per ciascuna proprietà, WMI rifiuta con l'errore WBEM \_ E \_ troppo \_ ampio qualsiasi query che non dispone di una clausola WHERE o se la clausola WHERE è troppo ampia per essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="25ff9-112">Because there is no way to evaluate the possible values for each of the properties, WMI rejects with the error WBEM\_E\_TOO\_BROAD any query that either does not have a WHERE clause or if the WHERE clause is too broad to be of any use.</span></span>

 

 



