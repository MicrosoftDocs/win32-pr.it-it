---
title: Creazione di una clausola WHERE per il provider del Registro di sistema
description: Il punto principale da considerare quando si crea una clausola WHERE appropriata per il provider del Registro di sistema è che ogni query di eventi deve essere completa ed esplicita. Il mancato completamento e l'esplicito restituiranno un messaggio di errore.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0fc037b746233bd9eb2f9bdd4afad942d07dc832b4dfd60cd9ca6ae9f273efca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679831"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Creazione di una clausola WHERE per il provider del Registro di sistema

Il punto principale da considerare quando si crea una clausola WHERE appropriata per il provider del Registro di sistema è che ogni query di eventi deve essere completa ed esplicita. Il mancato completamento e l'esplicito restituiranno un messaggio di errore.

Per essere completate, ogni query di eventi nel parametro *bstrQuery* di [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) deve contenere una clausola WHERE che include ognuna delle proprietà nella classe di evento specificata.

L'esempio seguente illustra come impostare *bstrQuery per* la registrazione per gli eventi di modifica dell'albero nell'albero "HKEY \_ LOCAL MACHINE \_ \\ Software".


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Per essere esplicito, il provider deve essere in grado di dedurre dalla query un elenco di valori possibili per ogni proprietà nella classe di evento.

Nell'esempio seguente viene illustrata la query di eventi che esegue correttamente la registrazione per gli eventi di modifica dell'albero.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



Di seguito è riportato un esempio di registrazione non corretta.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Poiché non è possibile valutare i valori possibili per ognuna delle proprietà, WMI rifiuta con l'errore WBEM E TOO BROAD qualsiasi query che non dispone di una clausola WHERE o se la clausola WHERE è troppo ampia per essere \_ \_ \_ utilizzata.

 

 



