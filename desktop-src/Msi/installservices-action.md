---
description: L'azione InstallServices registra un servizio per il sistema. Questa azione esegue una query sulla tabella ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Azione InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e37ea0a80050d6e9ab624ff878a352f96bbc0854fd64d6a1f563f277f1ea6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787021"
---
# <a name="installservices-action"></a>Azione InstallServices

L'azione InstallServices registra un servizio per il sistema. Questa azione esegue una query [sulla tabella ServiceInstall](serviceinstall-table.md).

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione dei servizi deve essere usata nella sequenza seguente.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

Una delle azioni seguenti: [InstallFiles,](installfiles-action.md) [RemoveFiles,](removefiles-action.md) [DuplicateFiles,](duplicatefiles-action.md) [MoveFiles,](movefiles-action.md) [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles.](removeduplicatefiles-action.md)

InstallServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

Questa azione richiede che l'utente sia un amministratore o abbia privilegi elevati con l'autorizzazione per installare i servizi o che l'applicazione sia parte di un'installazione gestita.

 

 



