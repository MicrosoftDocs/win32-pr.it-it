---
description: L'azione UnregisterProgIdInfo gestisce l'annullamento della registrazione delle informazioni del ProgId OLE con il sistema.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Azione UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885681"
---
# <a name="unregisterprogidinfo-action"></a>Azione UnregisterProgIdInfo

L'azione UnregisterProgIdInfo gestisce l'annullamento della registrazione delle informazioni del ProgId OLE con il sistema.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione UnregisterProgIdInfo deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) , [UnregisterClassInfo](unregisterclassinfo-action.md) Action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) Action e before the [RegisterProgIdInfo](registerprogidinfo-action.md) Action.

[RemoveRegistryValues](removeregistryvalues-action.md) deve precedere UnregisterProgIdInfo nella sequenza.

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensioninfo](unregisterextensioninfo-action.md)
-   UnregisterProgIdInfo
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, UnregisterProgIdInfo deve precedere [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                |
|-------|-------------------------------------------|
| \[1\] | Identificatore del programma registrato. |



 

## <a name="remarks"></a>Commenti

L'azione UnregisterProgIdInfo rimuove le informazioni sul ProgId dal registro di sistema ([tabella ProgId](progid-table.md)) per le funzionalità connesse alle informazioni sull'estensione ([tabella di estensione](extension-table.md)) o alle informazioni sulla classe ([tabella delle classi](class-table.md)) e attualmente selezionate per la disinstallazione.

 

 



