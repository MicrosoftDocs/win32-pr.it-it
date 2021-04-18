---
description: L'azione UnregisterClassInfo gestisce la rimozione delle informazioni della classe COM dal registro di sistema. Usa la tabella AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Azione UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319423"
---
# <a name="unregisterclassinfo-action"></a>Azione UnregisterClassInfo

L'azione UnregisterClassInfo gestisce la rimozione delle informazioni della classe COM dal registro di sistema. Usa la [tabella AppID](appid-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione UnregisterClassInfo deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) e prima dell'azione [registerClassInfo](registerclassinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) deve precedere UnregisterClassInfo nella sequenza.

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che si trovino nella stessa sequenza relativa, come illustrato nella tabella seguente:

-   UnregisterClassInfo
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, [RegisterExtensionInfo](registerextensioninfo-action.md) deve precedere UnregisterClassInfo nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione      |
|-------|---------------------------------|
| \[1\] | GUID della classe COM non registrata. |



 

## <a name="remarks"></a>Commenti

Il programma di installazione imposta la proprietà [**OLEAdvtSupport**](oleadvtsupport.md) su true quando il sistema dell'utente corrente è stato aggiornato per funzionare con l'installazione su richiesta tramite com. Se il sistema non supporta l'installazione su richiesta tramite COM, UnregisterClassInfo rimuove tutte le classi COM elencate nella tabella della [classe](class-table.md) associata alle funzionalità o funzionalità disinstallate installate come pubblicizzate dal registro di sistema. In caso contrario, questa azione rimuove solo le classi COM associate alle funzionalità selezionate per la disinstallazione dal registro di sistema.

 

 



