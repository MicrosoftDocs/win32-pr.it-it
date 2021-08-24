---
description: L'azione UnregisterMIMEInfo annulla la registrazione delle informazioni del Registro di sistema relative a MIME dal sistema. L'azione annulla la registrazione delle informazioni MIME per i server della tabella MIME per cui la funzionalità corrispondente è attualmente selezionata per la disinstallazione.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Azione UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e03ea1c50aa543615edc0ed875bd83b3338cdb261d09e01232e0fe76f7aa51ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810141"
---
# <a name="unregistermimeinfo-action"></a>Azione UnregisterMIMEInfo

L'azione UnregisterMIMEInfo annulla la registrazione delle informazioni del Registro di sistema relative a MIME dal sistema. L'azione annulla la registrazione delle informazioni MIME per i server della [tabella MIME](mime-table.md) per cui la funzionalità corrispondente è attualmente selezionata per la disinstallazione.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione UnregisterMIMEInfo deve essere eseguita dopo l'azione [InstallInitialize,](installinitialize-action.md) [UnregisterClassInfo,](unregisterclassinfo-action.md) [UnregisterExtensionInfo](unregisterextensioninfo-action.md) e prima dell'azione [RegisterMIMEInfo.](registermimeinfo-action.md)

[RemoveRegistryValues](removeregistryvalues-action.md) deve essere prima di UnregisterMIMEInfo nella sequenza.

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenze, deve avere lo stesso ordine di sequenza relativo illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   UnregisterMIMEInfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, UnregisterMIMEInfo deve essere prima [di RegisterExtensionInfo](registerextensioninfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                    |
|-------|-----------------------------------------------|
| \[1\] | Identificatore del tipo di contenuto MIME non registrato. |
| \[2\] | Estensione associata al tipo di contenuto MIME.  |



 

 

 



