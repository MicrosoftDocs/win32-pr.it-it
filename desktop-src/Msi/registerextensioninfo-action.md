---
description: L'azione RegisterExtensionInfo gestisce la registrazione delle informazioni correlate all'estensione con il sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Azione RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0541fc512c2300b0cb37f4a23305a3d312a4e60208890507fb7c6112e00c94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519381"
---
# <a name="registerextensioninfo-action"></a>Azione RegisterExtensionInfo

L'azione RegisterExtensionInfo gestisce la registrazione delle informazioni correlate all'estensione con il sistema.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione RegisterExtensionInfo deve essere eseguita dopo [l'azione InstallFiles](installfiles-action.md) e [l'azione UnregisterExtensionInfo.](unregisterextensioninfo-action.md)

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, deve avere lo stesso ordine di sequenza relativo come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Annullare la registrazione diMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, RegisterExtensionInfo deve essere presente dopo [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Estensione registrata.      |



 

## <a name="remarks"></a>Commenti

Se il sistema supporta l'installazione su richiesta per i server di estensione, RegisterExtensionInfo registra tutti i server di estensione nella tabella [delle](extension-table.md) estensioni associata alle funzionalità impostate per l'installazione o l'annuncio. In caso contrario, questa azione registra solo i server di estensione associati alle funzionalità impostate per l'installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ShellAdvtSupport - proprietà**](shelladvtsupport.md)
</dt> </dl>

 

 



