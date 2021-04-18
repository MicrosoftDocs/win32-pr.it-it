---
title: Aggiornamento di un oggetto dinamico
description: Un client può aggiornare la durata (TTL) di una determinata voce di directory per mantenerla attiva in uno dei due modi in cui viene eseguito un aggiornamento LDAP al valore dell'attributo entryTTL prima che la voce venga sottoposta a Garbage Collection.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7866c423fcb715289793a7beefa564150954257
ms.sourcegitcommit: 4d6ff888fd5825e78bc8fd5cdb21d4b542205039
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "106300716"
---
# <a name="refreshing-a-dynamic-object"></a>Aggiornamento di un oggetto dinamico

Un client può aggiornare la durata (TTL) di una determinata voce di directory per mantenerla attiva in uno dei due modi seguenti:

-   Esecuzione di un aggiornamento LDAP al valore dell'attributo **entryTTL** prima che la voce venga sottoposta a Garbage Collection. Questo metodo di aggiornamento di una voce dinamica nella directory è una funzionalità aggiuntiva (facoltativa) di Active Directory Domain Services non specificata dallo standard RFC 2589.
-   Esecuzione di un'operazione LDAP estesa con un OID di 1.3.6.1.4.1.1466.101.119.1 per l'aggiornamento TTL, come specificato nella RFC 2589. Questo OID viene definito come **OID di operatore \_ \_ Extended \_ \_ TTL LDAP** in WINLDAP. H.

 
* * Remark * * *: gli oggetti dinamici vengono rimossi dal Garbage Collector quando sono scaduti, non è presente alcuna fase dell'oggetto che è un oggetto contrassegnato per la rimozione definitiva quando è scaduto. Quando si aggiornano gli oggetti, è necessario prestare attenzione alla latenza di replica di Active Directory. È necessario assicurarsi che l'aggiornamento per aggiornare la durata (TTL) sia abbastanza presto, in modo che tutte le repliche del contesto dei nomi (catalogo completo e globale) vedano la transazione di aggiornamento prima della scadenza locale dell'oggetto.

 




