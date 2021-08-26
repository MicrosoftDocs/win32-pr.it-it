---
description: L'azione RegisterMIMEInfo registra le informazioni del Registro di sistema relative a MIME con il sistema.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Azione RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369f35eab4e6d4228167bfbeda48cf21249ea6a63297f5a9e893b84dcc4ed5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041741"
---
# <a name="registermimeinfo-action"></a>Azione RegisterMIMEInfo

L'azione RegisterMIMEInfo registra le informazioni del Registro di sistema relative a MIME con il sistema.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione RegisterMIMEInfo deve essere eseguita dopo l'azione [InstallFiles,](installfiles-action.md) [l'azione UnregisterMIMEInfo,](unregistermimeinfo-action.md) [l'azione RegisterClassInfo](registerclassinfo-action.md) e l'azione [RegisterExtensionInfo.](registerextensioninfo-action.md)

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, deve avere lo stesso ordine di sequenza relativo come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Annullare la registrazione diMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   RegisterMIMEInfo

Ad esempio, RegisterMIMEInfo deve essere successivo [a UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                   |
|-------|----------------------------------------------|
| \[1\] | Identificatore del tipo di contenuto MIME registrato.  |
| \[2\] | Estensione associata al tipo di contenuto MIME. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterMIMEInfo registra tutte le informazioni MIME per i server della tabella [MIME](mime-table.md) per cui è stato selezionato il server di classi o il server di estensione corrispondente per l'installazione.

 

 



