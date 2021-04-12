---
description: L'azione UnregisterMIMEInfo Annulla la registrazione delle informazioni del registro di sistema correlate a MIME dal sistema. L'azione annulla la registrazione delle informazioni MIME per i server dalla tabella MIME per cui è attualmente selezionata la funzionalità corrispondente per la disinstallazione.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Azione UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234177"
---
# <a name="unregistermimeinfo-action"></a>Azione UnregisterMIMEInfo

L'azione UnregisterMIMEInfo Annulla la registrazione delle informazioni del registro di sistema correlate a MIME dal sistema. L'azione annulla la registrazione delle informazioni MIME per i server dalla [tabella MIME](mime-table.md) per cui è attualmente selezionata la funzionalità corrispondente per la disinstallazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione UnregisterMIMEInfo deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) , [UnregisterClassInfo](unregisterclassinfo-action.md) Action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) Action e before the [RegisterMIMEInfo](registermimeinfo-action.md) Action.

[RemoveRegistryValues](removeregistryvalues-action.md) deve precedere UnregisterMIMEInfo nella sequenza.

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   UnregisterMIMEInfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, UnregisterMIMEInfo deve precedere [RegisterExtensionInfo](registerextensioninfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                    |
|-------|-----------------------------------------------|
| \[1\] | Identificatore del tipo di contenuto MIME non registrato. |
| \[2\] | Estensione associata al tipo di contenuto MIME.  |



 

 

 



