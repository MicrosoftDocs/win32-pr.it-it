---
description: I ruoli hanno due scopi diversi in Gestione autorizzazioni.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Ruoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f884475589bc8ecef945c1fd89d1ffab647258c01d3c83a2c9b96df53300501d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911965"
---
# <a name="roles"></a>Ruoli

I ruoli hanno due scopi diversi in Gestione autorizzazioni. Un ruolo è un set di attività o operazioni a cui una categoria di utenti richiede l'accesso ed è anche un set di utenti e gruppi che rientrano in tale categoria.

-   [Ruoli come set di attività](#roles-as-sets-of-tasks)
-   [Ruoli come set di utenti e gruppi](#roles-as-sets-of-users-and-groups)
-   [Argomenti correlati](#related-topics)

## <a name="roles-as-sets-of-tasks"></a>Ruoli come set di attività

I criteri di autorizzazione [**assegnano oggetti IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) a un [**oggetto IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) per creare set di attività. Tutti gli utenti e i gruppi assegnati a tale **oggetto IAzRole** hanno quindi l'autorizzazione per accedere a tutte le operazioni contenute in **tali oggetti IAzTask.**

Poiché un [**oggetto IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) rappresenta sia un set di attività che un set di utenti e gruppi che hanno accesso a tali attività, Gestione autorizzazioni consente di creare definizioni di ruolo che possono essere assegnate a più oggetti **IAzRole.** Un [**oggetto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) può contenere altri **oggetti IAzTask.** È quindi possibile usare **l'oggetto IAzTask** come definizione del ruolo assegnandolo a uno o più **oggetti IAzRole.** Impostare la [**proprietà IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) dell'oggetto **IAzTask** su **TRUE** per fare in modo che l'interfaccia utente dello snap-in MMC di **Gestione** autorizzazioni visualizza l'oggetto **IAzTask** come ruolo.

## <a name="roles-as-sets-of-users-and-groups"></a>Ruoli come set di utenti e gruppi

Assegnare utenti e gruppi a un oggetto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) per concedere a tali utenti e gruppi l'accesso alle attività assegnate a tale **oggetto IAzRole** chiamando il [**metodo AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) o [**AddMemberName.**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) Assegnare gruppi di applicazioni esistenti, rappresentati da [**oggetti IAzApplicationGroup,**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) a un **oggetto IAzRole** chiamando il [**metodo AddAppMember.**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) Tutti gli utenti e i gruppi assegnati **all'oggetto IAzRole** hanno accesso alle attività e alle operazioni assegnate a tale ruolo. Per altre informazioni sui gruppi di applicazioni, vedere [Utenti e gruppi](users-and-groups.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raggruppamento di attività in ruoli in C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Definizione di gruppi di utenti in C++](defining-groups-of-users-in-c--.md)
</dt> <dt>

[Aggiunta di utenti a un gruppo di applicazioni in C++](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



