---
title: Partizioni di directory applicative
description: In Windows Server 2003 Active Directory Domain Services supportano le partizioni di directory applicative.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Active Directory partizioni di Active Directory
- Active Directory per le partizioni di directory applicative usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046559"
---
# <a name="application-directory-partitions"></a>Partizioni di directory applicative

In Windows Server 2003 Active Directory Domain Services supportano le partizioni di directory applicative. Una partizione di directory applicativa può contenere una gerarchia di qualsiasi tipo di oggetti, ad eccezione delle entità di sicurezza, e può essere configurata per la replica in qualsiasi set di controller di dominio nella foresta. A differenza di una partizione di dominio, non è necessario eseguire la replica di una partizione di directory applicativa a tutti i controller di dominio in un dominio e la partizione può essere replicata nei controller di dominio in domini diversi della foresta. Per ulteriori informazioni sulle partizioni di directory applicative, vedere [informazioni sulle partizioni di directory applicative](about-application-directory-partitions.md).

È possibile creare una partizione di directory applicativa. modificato ed eliminato mediante le operazioni standard ADSI, LDAP e [System. DirectoryServices](/dotnet/api/system.directoryservices) . Il contesto di sicurezza necessario per creare e modificare una partizione di directory applicativa è identico a quello per la creazione di una partizione di dominio.

Negli argomenti seguenti viene descritto come utilizzare le partizioni di directory applicative:

-   [Replica della partizione di directory applicativa](application-directory-partition-replication.md)
-   [Sicurezza della partizione di directory applicativa](application-directory-partition-security.md)
-   [Creazione di una partizione di directory applicativa](creating-an-application-directory-partition.md)
-   [Eliminazione di una partizione di directory applicativa](deleting-an-application-directory-partition.md)
-   [Enumerazione delle partizioni di directory applicative in una foresta](enumerating-application-directory-partitions-in-a-forest.md)
-   [Individuazione di un server host partizione di directory applicativa](locating-an-application-directory-partition-host-server.md)
-   [Aggiunta o eliminazione di una replica della partizione di directory applicativa](adding-or-deleting-an-application-directory-partition-replica.md)
-   [Enumerazione delle repliche di una partizione di directory applicativa](enumerating-replicas-of-an-application-directory-partition.md)
-   [Modifica della configurazione della partizione di directory applicativa](modifying-application-directory-partition-configuration.md)

 

 