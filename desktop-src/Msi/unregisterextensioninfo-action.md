---
description: L'azione UnregisterExtensionInfo gestisce la rimozione delle informazioni relative all'estensione dal Registro di sistema.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Azione UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8dae707bc4dd517402d8a85fb64402637a815f8249d4677f18818c855ba4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810231"
---
# <a name="unregisterextensioninfo-action"></a>Azione UnregisterExtensionInfo

L'azione UnregisterExtensionInfo gestisce la rimozione delle informazioni relative all'estensione dal Registro di sistema.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione UnregisterExtensionInfo deve essere eseguita dopo [l'azione InstallInitialize](installinitialize-action.md) e prima [dell'azione RegisterExtensionInfo.](registerextensioninfo-action.md)

[RemoveRegistryValues](removeregistryvalues-action.md) deve essere prima di UnregisterExtensionInfo nella sequenza.

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenze, deve avere lo stesso ordine di sequenza relativo illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   UnregisterExtensionInfo
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, UnregisterExtensionInfo deve essere prima [di UnregisterProgIdInfo](unregisterprogidinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Estensione rimossa.         |



 

## <a name="remarks"></a>Commenti

Se il sistema non supporta l'installazione su richiesta dei server di estensione, [](extension-table.md) UnregisterExtensionInfo rimuove tutti i server di estensione nella tabella delle estensioni associata a una funzionalità disinstallata o a una funzionalità installata come annunciato dal Registro di sistema. In caso contrario, questa azione rimuove i server di estensione associati a una funzionalità selezionata per la rimozione dal Registro di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



