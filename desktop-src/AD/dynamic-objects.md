---
title: Oggetti dinamici
description: In Windows Server 2003 e versioni successive di Windows, Active Directory Domain Services supporto per l'archiviazione di voci dinamiche nella directory.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- oggetti dinamici AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74660728179365f6585bce2462cd22f2508e68318eb84312d039a431330329b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191719"
---
# <a name="dynamic-objects"></a>Oggetti dinamici

In Windows Server 2003 e versioni successive di Windows, Active Directory Domain Services supporto per l'archiviazione di voci dinamiche nella directory. Una voce dinamica è un oggetto nella directory a cui è associato un valore time-to-live (TTL). La durata (TTL) per una voce viene impostata al momento della creazione della voce. La durata viene automaticamente decrementata e alla scadenza la voce dinamica scompare. Il client può far sì che una voce dinamica rimanga più lunga della durata rimanente corrente aggiornando (modificando) il valore TTL. I client che archiviano dati dinamici nella directory devono aggiornare periodicamente i dati per evitare che scompaiano.

Molte applicazioni e servizi che usano LDAP per archiviare e accedere a dati relativamente statici e interessanti a livello globale da un server Active Directory preferiscono anche continuare a usare l'accesso LDAP per le proprie esigenze di dati dinamici. Inoltre, per alcune applicazioni può essere preferibile eseguire l'off-load dell'attività di Garbage Collection degli oggetti nel servizio directory che hanno una durata utile limitata per il servizio directory. Le partizioni di directory applicative (con la possibilità di posizionamento controllato delle repliche) e i TTTL per oggetto insieme offriranno la possibilità di ospitare dati dinamici in Active Directory Domain Services, consentendo così l'accesso LDAP ad esso.

Una nuova classe di oggetti ausiliari denominata **dynamicObject** con OID = 1.3.6.1.4.1.1.1466.101.119.2 verrà definita nello schema ad Active Directory di base che verrà usato dalle voci dinamiche. Questa classe ausiliaria contiene l'attributo **denominato entryTTL** con OID = 1.3.6.1.4.1.1466.101.119.3 come attributo system-may-contain. Il valore di questo attributo è il "tempo in secondi" in cui la voce di directory corrispondente continuerà a esistere prima di scomparire dalla directory. Se il client non fornisce un valore per questo attributo in modo esplicito al momento della creazione dell'oggetto, il DS fornisce un valore predefinito come specificato in un secondo momento.

Una nuova operazione LDAP estesa con OID = 1.3.6.1.4.1.1466.101.119.1 per l'aggiornamento client di una voce dinamica nella directory verrà definita e pubblicata nell'attributo **supportedExtension** dell'oggetto DSE radice.

Nell'implementazione effettiva, **entryTTL** è un attributo costruito. L'ora di scadenza dell'oggetto reale viene archiviata come ora assoluta in cui l'oggetto può essere eliminato in un attributo solo di sistema denominato **ms-DS-Entry-Time-To-Live.**

Tutti gli oggetti dinamici presentano le limitazioni seguenti:

-   Un oggetto dinamico eliminato a causa della scadenza del TTL non lascia un oggetto contrassegnato per la rimozione definitiva.
-   Tutti i controller di dominio che eseguono repliche di oggetti dinamici devono essere eseguiti Windows Server 2003.
-   Le voci dinamiche con valori TTL sono supportate in tutte le partizioni, ad eccezione della partizione di configurazione e della partizione dello schema.
-   Active Directory Domain Services pubblicare l'attributo **facoltativo dynamicSubtrees,** come descritto in RFC 2589, nell'oggetto DSE radice.
-   Le voci dinamiche vengono gestite in modo simile alle voci non dinamiche durante l'elaborazione di operazioni di ricerca, confronto, aggiunta, eliminazione, modifica e modificaDN.
-   Non è possibile modificare una voce statica in una voce dinamica e viceversa.
-   Non è possibile aggiungere una voce non dinamica come subordinata a una voce dinamica.

 

 




