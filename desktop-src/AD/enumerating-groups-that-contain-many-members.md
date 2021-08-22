---
title: Enumerazione di gruppi che contengono molti membri
description: Informazioni sull'enumerazione Azure Active Directory che contengono molti membri usando il recupero incrementale dei dati (recupero di intervalli).
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Enumerazione dei gruppi che contengono molti membri di Active Directory
- groups Active Directory , enumerazione di gruppi con molti membri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550ec2f4a77938b26e2273d468d3f9740d637249501aa2396fef3744cd105060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695139"
---
# <a name="enumerating-groups-that-contain-many-members"></a>Enumerazione di gruppi che contengono molti membri

I membri di un gruppo vengono archiviati in un attributo multivalore denominato **member**. **L'attributo** member può contenere un numero elevato di valori. L'enumerazione dei membri può risultare inefficiente quando il numero di valori in un attributo multivalore diventa elevato. Il server limiterà anche il numero massimo di valori che possono essere recuperati in una singola query. Ciò significa che se un gruppo può avere più membri di quelli che possono essere forniti dal server, l'unico modo per enumerare tutti i membri è usare il recupero incrementale dei dati, noto come recupero di *intervalli.*

Il recupero di intervalli comporta la richiesta di un numero limitato di valori di attributo in una singola query. Il numero di valori richiesti deve essere minore o uguale al numero massimo di valori supportati dal server. Per ridurre il numero di volte in cui la query deve contattare il server, il numero di valori richiesti deve essere il più vicino possibile a questo valore massimo. Per consentire a un'applicazione di funzionare correttamente con tutti i server, è necessario usare un numero massimo di 1000.

La versione del server che fornisce i dati richiesti determina il numero massimo di valori che possono essere recuperati in una singola query. Nella tabella seguente sono elencati la versione del server e il numero massimo di valori che è possibile recuperare in una singola query.



| Versione del sistema operativo del server | Valori massimi recuperati |
|---------------------------------|--------------------------|
| Windows 2000                    | 1000                     |
| Windows Server 2003             | 1500                     |



 

Per altre informazioni sul recupero di intervalli di valori di attributo con ADSI, vedere [Recupero di intervalli di attributi](/windows/desktop/ADSI/attribute-range-retrieval).

Per altre informazioni sul recupero di intervalli di valori di attributo [con System.DirectoryServices](/dotnet/api/system.directoryservices), vedere [Enumerazione dei membri in un gruppo di grandi dimensioni](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).

 

 