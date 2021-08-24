---
description: L'azione UnregisterProgIdInfo gestisce l'annullamento della registrazione delle informazioni sul ProgId OLE con il sistema.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Azione UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6666e5648cba220dbb9bbc6e2d50c3959c1d73c98f97dcfd8c45cb3de8d94c82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786961"
---
# <a name="unregisterprogidinfo-action"></a>Azione UnregisterProgIdInfo

L'azione UnregisterProgIdInfo gestisce l'annullamento della registrazione delle informazioni sul ProgId OLE con il sistema.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione UnregisterProgIdInfo deve essere eseguita dopo l'azione [InstallInitialize,](installinitialize-action.md) [UnregisterClassInfo,](unregisterclassinfo-action.md) [UnregisterExtensioninfo](unregisterextensioninfo-action.md) e prima dell'azione [RegisterProgIdInfo.](registerprogidinfo-action.md)

[RemoveRegistryValues](removeregistryvalues-action.md) deve essere prima di UnregisterProgIdInfo nella sequenza.

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenze, deve avere lo stesso ordine di sequenza relativo illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensioninfo](unregisterextensioninfo-action.md)
-   UnregisterProgIdInfo
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, UnregisterProgIdInfo deve essere prima [di UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                |
|-------|-------------------------------------------|
| \[1\] | Identificatore di programma del programma registrato. |



 

## <a name="remarks"></a>Commenti

L'azione UnregisterProgIdInfo rimuove le informazioni progId dal Registro di sistema ( Tabella[ProgId](progid-table.md)) per le funzionalità connesse alle informazioni sull'estensione[(tabella](extension-table.md)di estensione ) o alle informazioni sulla classe[(tabella](class-table.md)class ) e attualmente selezionate per la disinstallazione.

 

 



