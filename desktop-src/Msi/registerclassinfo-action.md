---
description: L'azione RegisterClassInfo gestisce la registrazione delle informazioni della classe COM con il sistema. Usa la tabella AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Azione RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311712"
---
# <a name="registerclassinfo-action"></a>Azione RegisterClassInfo

L'azione RegisterClassInfo gestisce la registrazione delle informazioni della classe COM con il sistema. Usa la [tabella AppID](appid-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RegisterClassInfo deve essere successiva all'azione [InstallFiles](installfiles-action.md) e [UnregisterClassInfo](unregisterclassinfo-action.md) .

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, RegisterClassInfo deve essere seguito da [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                          |
|-------|-----------------------------------------------------|
| \[1\] | Identificatore di classe GUID del server COM registrato. |



 

## <a name="remarks"></a>Commenti

Se il sistema supporta l'installazione su richiesta per i server OLE, RegisterClassInfo registra tutte le classi COM nella [tabella della classe](class-table.md) associata a una funzionalità selezionata per l'installazione o l'annuncio. In caso contrario, questa azione registra solo le classi COM associate a una funzionalità selezionata per l'installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà OLEAdvtSupport**](oleadvtsupport.md)
</dt> </dl>

 

 



