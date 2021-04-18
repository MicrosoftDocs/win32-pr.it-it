---
description: Un'operazione è un'azione del computer di basso livello.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Operazioni e attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314728"
---
# <a name="operations-and-tasks"></a>Operazioni e attività

Un'operazione è un'azione del computer di basso livello. Nell'API di gestione autorizzazioni un'operazione è rappresentata da un oggetto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . In generale, le operazioni sono troppo numerose e di basso livello per facilitare l'amministrazione. Raggruppare le operazioni nelle attività per semplificare l'amministrazione dei criteri di autorizzazione.

Un'attività è rappresentata da un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) e può contenere uno o più oggetti [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . Un oggetto **IAzTask** può inoltre contenere altri oggetti **IAzTask** , in modo che le attività possano essere annidate. Per semplificare l'amministrazione, un oggetto **IAzTask** deve rappresentare un'attività che un utente reale vuole eseguire.

L'accesso alle operazioni contenute in un'attività può essere qualificato in fase di esecuzione da uno script della regola di business associato all'oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) che rappresenta tale attività. Per ulteriori informazioni sugli script delle regole business, vedere [regole business](business-rules.md).

Un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) può anche rappresentare una definizione di ruolo impostando la relativa proprietà [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) su **true**. L'interfaccia utente dello snap-in MMC di **Gestione autorizzazioni** Visualizza quindi l'oggetto **IAzTask** come ruolo. Per ulteriori informazioni sulle definizioni di ruolo, vedere [ruoli](roles.md).

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

 

 



