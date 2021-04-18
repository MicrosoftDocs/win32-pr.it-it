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
# <a name="refreshing-a-dynamic-object"></a><span data-ttu-id="2fe81-103">Aggiornamento di un oggetto dinamico</span><span class="sxs-lookup"><span data-stu-id="2fe81-103">Refreshing a Dynamic Object</span></span>

<span data-ttu-id="2fe81-104">Un client può aggiornare la durata (TTL) di una determinata voce di directory per mantenerla attiva in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2fe81-104">A client can refresh the Time To Live (TTL) of a given directory entry to keep it alive in one of two ways:</span></span>

-   <span data-ttu-id="2fe81-105">Esecuzione di un aggiornamento LDAP al valore dell'attributo **entryTTL** prima che la voce venga sottoposta a Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="2fe81-105">Performing an LDAP update to the value of its **entryTTL** attribute before the entry is garbage collected.</span></span> <span data-ttu-id="2fe81-106">Questo metodo di aggiornamento di una voce dinamica nella directory è una funzionalità aggiuntiva (facoltativa) di Active Directory Domain Services non specificata dallo standard RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="2fe81-106">This method of refreshing a dynamic entry in the directory is an additional (optional) feature of Active Directory Domain Services that is not specified by RFC 2589.</span></span>
-   <span data-ttu-id="2fe81-107">Esecuzione di un'operazione LDAP estesa con un OID di 1.3.6.1.4.1.1466.101.119.1 per l'aggiornamento TTL, come specificato nella RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="2fe81-107">Performing an LDAP extended operation with an OID of 1.3.6.1.4.1.1466.101.119.1 for TTL refresh, as stipulated in the RFC 2589.</span></span> <span data-ttu-id="2fe81-108">Questo OID viene definito come **OID di operatore \_ \_ Extended \_ \_ TTL LDAP** in WINLDAP. H.</span><span class="sxs-lookup"><span data-stu-id="2fe81-108">This OID is defined as **LDAP\_TTL\_EXTENDED\_OP\_OID** in WINLDAP.H.</span></span>

 
<span data-ttu-id="2fe81-109">\* \* Remark \* \* \*: gli oggetti dinamici vengono rimossi dal Garbage Collector quando sono scaduti, non è presente alcuna fase dell'oggetto che è un oggetto contrassegnato per la rimozione definitiva quando è scaduto.</span><span class="sxs-lookup"><span data-stu-id="2fe81-109">\*\*Remark\*\*\*: Dynamic objects are removed by Garbage Collector when they have expired, there is no phase of the object being a tombstone when it has expired.</span></span> <span data-ttu-id="2fe81-110">Quando si aggiornano gli oggetti, è necessario prestare attenzione alla latenza di replica di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2fe81-110">You need to be careful with the AD replication latency when you refresh objects.</span></span> <span data-ttu-id="2fe81-111">È necessario assicurarsi che l'aggiornamento per aggiornare la durata (TTL) sia abbastanza presto, in modo che tutte le repliche del contesto dei nomi (catalogo completo e globale) vedano la transazione di aggiornamento prima della scadenza locale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2fe81-111">You have to ensure that the update to refresh the TTL arrives early enough so all replicas of the naming context (full and global catalog) see the refresh transaction before the object expires locally.</span></span>

 




