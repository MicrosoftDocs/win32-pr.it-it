---
description: Un'operazione è un'azione computer di basso livello.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Operazioni e attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8e60923e9631e37087a28a6a19747dc63249ff2f1ae8224c20e859e1f13c25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912407"
---
# <a name="operations-and-tasks"></a>Operazioni e attività

Un'operazione è un'azione computer di basso livello. Nell'API di Gestione autorizzazioni un'operazione è rappresentata da un [**oggetto IAzOperation.**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) In generale, le operazioni sono troppe in numero e di livello troppo basso per facilitare l'amministrazione. Raggruppare le operazioni in attività per semplificare l'amministrazione dei criteri di autorizzazione.

Un'attività è rappresentata da un [**oggetto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) e può contenere uno o più [**oggetti IAzOperation.**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) Un **oggetto IAzTask** può contenere anche altri **oggetti IAzTask,** in modo che le attività possano essere annidate. Per facilitare l'amministrazione, un **oggetto IAzTask** deve rappresentare un'attività che un utente reale vuole eseguire.

L'accesso alle operazioni contenute in un'attività può essere qualificato in fase di esecuzione da uno script della regola business associato [**all'oggetto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) che rappresenta tale attività. Per altre informazioni sugli script delle regole business, [vedere Business Rules](business-rules.md).

Un [**oggetto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) può anche rappresentare una definizione di ruolo impostandone la proprietà [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) su **TRUE.** **L'interfaccia utente** dello snap-in MMC di Gestione autorizzazioni visualizza quindi **l'oggetto IAzTask** come ruolo. Per altre informazioni sulle definizioni dei ruoli, vedere [Ruoli](roles.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Definizione di operazioni in C++](defining-operations-in-c--.md)
</dt> <dt>

[Raggruppamento di operazioni in attività in C++](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[Raggruppamento di attività in ruoli in C++](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[Utenti e gruppi](users-and-groups.md)
</dt> </dl>

 

 



