---
description: I ruoli servono due scopi diversi in Gestione autorizzazioni.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Ruoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879662"
---
# <a name="roles"></a>Ruoli

I ruoli servono due scopi diversi in Gestione autorizzazioni. Un ruolo è un set di attività o operazioni a cui una categoria di utenti richiede l'accesso ed è anche un set di utenti e gruppi che rientrano in tale categoria.

-   [Ruoli come set di attività](#roles-as-sets-of-tasks)
-   [Ruoli come set di utenti e gruppi](#roles-as-sets-of-users-and-groups)
-   [Argomenti correlati](#related-topics)

## <a name="roles-as-sets-of-tasks"></a>Ruoli come set di attività

Un criterio di autorizzazione assegna oggetti [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) a un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) per creare set di attività. Tutti gli utenti e i gruppi assegnati a tale oggetto **IAzRole** dispongono quindi dell'autorizzazione per accedere a tutte le operazioni contenute negli oggetti **IAzTask** .

Poiché un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) rappresenta un set di attività e un set di utenti e gruppi che hanno accesso a tali attività, gestione autorizzazioni fornisce un modo per creare definizioni di ruolo che possono essere assegnate a più di un oggetto **IAzRole** . Un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) può contenere altri oggetti **IAzTask** . È quindi possibile usare l'oggetto **IAzTask** come definizione di ruolo assegnando questo oggetto a uno o più oggetti **IAzRole** . Impostare la proprietà [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) dell'oggetto **IAzTask** su **true** per fare in modo che l'interfaccia utente dello snap-in MMC di **Gestione autorizzazioni** visualizzi l'oggetto **IAzTask** come ruolo.

## <a name="roles-as-sets-of-users-and-groups"></a>Ruoli come set di utenti e gruppi

Assegnare utenti e gruppi a un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) per concedere a tali utenti e gruppi l'accesso alle attività assegnate a tale oggetto **IAzRole** chiamando il metodo [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) o [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) . Assegnare i gruppi di applicazioni esistenti, rappresentati da oggetti [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , a un oggetto **IAzRole** chiamando il metodo [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) . Tutti gli utenti e i gruppi assegnati all'oggetto **IAzRole** hanno accesso alle attività e alle operazioni assegnate a tale ruolo. Per ulteriori informazioni sui gruppi di applicazioni, vedere [utenti e gruppi](users-and-groups.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raggruppamento di attività in ruoli in C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Definizione di gruppi di utenti in C++](defining-groups-of-users-in-c--.md)
</dt> <dt>

[Aggiunta di utenti a un gruppo di applicazioni in C++](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



