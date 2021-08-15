---
title: Aggiornamento di un oggetto dinamico
description: 'Un client può aggiornare la durata (TTL) di una voce di directory specificata per mantenerla attiva in uno dei due modi seguenti: Eseguire un aggiornamento LDAP al valore del relativo attributo entryTTL prima che la voce venga garbage collection.'
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c351b559da8d08ccca3346f7126a9bbe47fcd3774486ea64a8dff29ac7e799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025179"
---
# <a name="refreshing-a-dynamic-object"></a>Aggiornamento di un oggetto dinamico

Un client può aggiornare la durata (TTL) di una voce di directory specificata per mantenerla attiva in uno dei due modi seguenti:

-   Esecuzione di un aggiornamento LDAP al valore del relativo **attributo entryTTL** prima che la voce venga garbage collection. Questo metodo di aggiornamento di una voce dinamica nella directory è una funzionalità aggiuntiva (facoltativa) di Active Directory Domain Services non specificata da RFC 2589.
-   Esecuzione di un'operazione ldap estesa con un OID di 1.3.6.1.4.1.1466.101.119.1 per l'aggiornamento TTL, come stabilito nella RFC 2589. Questo OID è definito come **LDAP \_ TTL \_ EXTENDED OP \_ \_ OID** in WINLDAP.H.

 
**Osservazioni***: gli oggetti dinamici vengono rimossi dal Garbage Collector quando sono scaduti. Non esiste alcuna fase dell'oggetto che viene contrassegnato per la rimozione definitiva quando è scaduto. Quando si aggiornano gli oggetti, è necessario prestare attenzione alla latenza di replica di Active Directory. È necessario assicurarsi che l'aggiornamento per aggiornare la durata (TTL) arrivi abbastanza presto in modo che tutte le repliche del contesto dei nomi (catalogo completo e globale) vedano la transazione di aggiornamento prima della scadenza locale dell'oggetto.

 




