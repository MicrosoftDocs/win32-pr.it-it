---
description: L'azione UnregisterExtensionInfo gestisce la rimozione delle informazioni relative all'estensione dal registro di sistema.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Azione UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319419"
---
# <a name="unregisterextensioninfo-action"></a>Azione UnregisterExtensionInfo

L'azione UnregisterExtensionInfo gestisce la rimozione delle informazioni relative all'estensione dal registro di sistema.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione UnregisterExtensionInfo deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) e prima dell'azione [RegisterExtensionInfo](registerextensioninfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) deve precedere UnregisterExtensionInfo nella sequenza.

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   UnregisterExtensionInfo
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, UnregisterExtensionInfo deve precedere [UnregisterProgIdInfo](unregisterprogidinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Estensione rimossa.         |



 

## <a name="remarks"></a>Commenti

Se il sistema non supporta l'installazione su richiesta dei server di estensione, UnregisterExtensionInfo rimuove tutti i server di estensione nella [tabella di estensione](extension-table.md) associata a una funzionalità disinstallata o a una funzionalità installata come annunciato dal registro di sistema. In caso contrario, questa azione rimuoverà i server di estensione associati a una funzionalità selezionata per la rimozione dal registro di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



