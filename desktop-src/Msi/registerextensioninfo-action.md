---
description: L'azione RegisterExtensionInfo gestisce la registrazione delle informazioni relative all'estensione con il sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Azione RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311710"
---
# <a name="registerextensioninfo-action"></a>Azione RegisterExtensionInfo

L'azione RegisterExtensionInfo gestisce la registrazione delle informazioni relative all'estensione con il sistema.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RegisterExtensionInfo deve essere successiva all'azione [InstallFiles](installfiles-action.md) e [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, RegisterExtensionInfo deve essere seguito da [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Estensione registrata.      |



 

## <a name="remarks"></a>Commenti

Se il sistema supporta l'installazione su richiesta per i server di estensione, RegisterExtensionInfo registra tutti i server di estensione nella [tabella di estensione](extension-table.md) associata alle funzionalità impostate per l'installazione o l'annuncio. In caso contrario, questa azione registra solo i server di estensione associati alle funzionalità impostate sull'installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



