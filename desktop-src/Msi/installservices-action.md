---
description: L'azione InstallServices registra un servizio per il sistema. Questa azione esegue una query sulla tabella ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Azione InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317758"
---
# <a name="installservices-action"></a>Azione InstallServices

L'azione InstallServices registra un servizio per il sistema. Questa azione esegue una query sulla [tabella ServiceInstall](serviceinstall-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione servizi deve essere utilizzata nella sequenza seguente.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

Una delle azioni seguenti: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) .

InstallServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Per questa azione è necessario che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per installare i servizi o che l'applicazione faccia parte di un'installazione gestita.

 

 



