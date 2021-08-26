---
description: L'azione RegisterClassInfo gestisce la registrazione delle informazioni sulla classe COM con il sistema. Usa la tabella AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Azione RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a0983b77c517cb2084b21d6d1500ec9b2a54b45d403c43f65bcc29505e2afe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912891"
---
# <a name="registerclassinfo-action"></a>Azione RegisterClassInfo

L'azione RegisterClassInfo gestisce la registrazione delle informazioni sulla classe COM con il sistema. Usa la [tabella AppId](appid-table.md).

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione RegisterClassInfo deve essere eseguita dopo [l'azione InstallFiles](installfiles-action.md) e [l'azione UnregisterClassInfo.](unregisterclassinfo-action.md)

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, deve avere lo stesso ordine di sequenza relativo come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Annullare la registrazione diMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, RegisterClassInfo deve essere successivo [a UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                          |
|-------|-----------------------------------------------------|
| \[1\] | Identificatore di classe GUID del server COM registrato. |



 

## <a name="remarks"></a>Commenti

Se il sistema supporta l'installazione su richiesta per i server OLE, RegisterClassInfo registra tutte le classi COM nella tabella [Class](class-table.md) associata a una funzionalità selezionata per l'installazione o l'annuncio. In caso contrario, questa azione registra solo le classi COM associate a una funzionalità selezionata per l'installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**OLEAdvtSupport - proprietà**](oleadvtsupport.md)
</dt> </dl>

 

 



