---
title: Oggetti dinamici
description: In Windows Server 2003 e versioni successive di Windows Active Directory Domain Services fornire supporto per l'archiviazione di voci dinamiche nella directory.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- Active Directory di oggetti dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d521dabda8f82cbdcd46c00b3041f150f390d60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707708"
---
# <a name="dynamic-objects"></a>Oggetti dinamici

In Windows Server 2003 e versioni successive di Windows Active Directory Domain Services fornire supporto per l'archiviazione di voci dinamiche nella directory. Una voce dinamica è un oggetto nella directory a cui è associato un valore TTL (time-to-Live). Il valore TTL per una voce viene impostato al momento della creazione della voce. Il time-to-Live viene decrementato automaticamente e quando scade la voce dinamica scompare. Il client può causare la permanenza di una voce dinamica più lunga rispetto alla durata rimanente aggiornando (modificando) il valore TTL. I client che archiviano i dati dinamici nella directory devono aggiornare periodicamente tali dati per impedirne la visualizzazione.

Molti servizi e applicazioni che usano LDAP per archiviare e accedere a dati relativamente statici e interessanti a livello globale da un server di Active Directory preferiscono anche continuare a usare l'accesso LDAP per le proprie esigenze di Dynamic Data. Per alcune applicazioni, inoltre, potrebbe essere opportuno non caricare l'attività di Garbage Collection di oggetti in DS che hanno una vita utile limitata al servizio directory. Le partizioni di directory applicative (con la possibilità di posizionare le repliche controllate) e TTLs per oggetto offrono la possibilità di ospitare dati dinamici in Active Directory Domain Services, consentendo in tal modo l'accesso LDAP.

Una nuova classe di oggetti ausiliaria denominata **DynamicObject** con OID = 1.3.6.1.4.1.1466.101.119.2 verrà definita nello schema ad di base per l'uso da parte delle voci dinamiche. Questa classe ausiliaria contiene l'attributo denominato **entryTTL** con OID = 1.3.6.1.4.1.1466.101.119.3 come attributo di sistema-può contenere. Il valore di questo attributo è il "tempo in secondi" durante il quale la voce di directory corrispondente continuerà a esistere prima di scomparire dalla directory. Se il client non fornisce un valore per questo attributo in modo esplicito al momento della creazione dell'oggetto, DS fornisce un valore predefinito come specificato in un secondo momento.

Una nuova operazione LDAP estesa con OID = 1.3.6.1.4.1.1466.101.119.1 per l'aggiornamento client di una voce dinamica nella directory verrà definita e pubblicata nell'attributo **supportedExtension** dell'oggetto DSE radice.

Nell'implementazione effettiva, **entryTTL** è un attributo costruito. L'ora di scadenza dell'oggetto reale viene archiviata come tempo assoluto quando l'oggetto può essere eliminato in un attributo solo di sistema denominato **ms-DS-entry-time-to-Live**.

Tutti gli oggetti dinamici presentano le limitazioni seguenti:

-   Un oggetto dinamico eliminato a causa della scadenza del valore TTL non lascia un oggetto contrassegnato per la rimozione definitiva.
-   Tutti i controller di dominio che dispongono di repliche di oggetti dinamici devono essere eseguiti in Windows Server 2003.
-   Le voci dinamiche con valori TTL sono supportate in tutte le partizioni eccetto la partizione di configurazione e la partizione dello schema.
-   Active Directory Domain Services non pubblicare l'attributo facoltativo **dynamicSubtrees** , come descritto nella RFC 2589, nell'oggetto DSE radice.
-   Le voci dinamiche vengono gestite in modo simile alle voci non dinamiche durante l'elaborazione delle operazioni di ricerca, confronto, aggiunta, eliminazione, modifica e MODIFYDN del.
-   Non è possibile modificare una voce statica in una voce dinamica e viceversa.
-   Non è possibile aggiungere una voce non dinamica a una voce dinamica.

 

 




