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
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Creazione di una clausola WHERE per il provider del registro di sistema

I punti principali da considerare durante la creazione di una clausola WHERE corretta per il provider del registro di sistema sono il fatto che ogni query di evento deve essere completa ed esplicita. Il mancato completamento e l'esplicito comporteranno un messaggio di errore.

Per essere completa, ogni query di evento nel parametro *bstrQuery* di [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) deve contenere una clausola WHERE che include ognuna delle proprietà nella classe di evento specificata.

Nell'esempio seguente viene illustrato come impostare *bstrQuery* per la registrazione degli eventi di modifica della struttura ad albero nell'albero "HKEY \_ Local \_ Machine \\ software".


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Per essere esplicito, il provider deve essere in grado di dedurre dalla query un elenco di valori possibili per ogni proprietà nella classe di evento.

Nell'esempio seguente viene illustrata la query di eventi che registra correttamente per gli eventi di modifica della struttura ad albero.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



Di seguito è riportato un esempio di registrazione non corretta.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Poiché non esiste alcun modo per valutare i valori possibili per ciascuna proprietà, WMI rifiuta con l'errore WBEM \_ E \_ troppo \_ ampio qualsiasi query che non dispone di una clausola WHERE o se la clausola WHERE è troppo ampia per essere utilizzata.

 

 



