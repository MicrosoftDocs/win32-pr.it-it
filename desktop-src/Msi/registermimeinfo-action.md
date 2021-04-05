---
description: L'azione RegisterMIMEInfo registra le informazioni del registro di sistema correlate a MIME con il sistema.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Azione RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756467"
---
# <a name="registermimeinfo-action"></a>Azione RegisterMIMEInfo

L'azione RegisterMIMEInfo registra le informazioni del registro di sistema correlate a MIME con il sistema.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RegisterMIMEInfo deve provenire dopo l'azione [InstallFiles](installfiles-action.md) , l'azione [UnregisterMIMEInfo](unregistermimeinfo-action.md) , l'azione [registerClassInfo](registerclassinfo-action.md) e l'azione [RegisterExtensionInfo](registerextensioninfo-action.md) .

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   RegisterMIMEInfo

Ad esempio, RegisterMIMEInfo deve essere seguito da [UnregisterMIMEInfo](unregistermimeinfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                   |
|-------|----------------------------------------------|
| \[1\] | Identificatore del tipo di contenuto MIME registrato.  |
| \[2\] | Estensione associata al tipo di contenuto MIME. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterMIMEInfo registra tutte le informazioni MIME per i server dalla [tabella MIME](mime-table.md) per cui è stato selezionato il server di classe o il server di estensione corrispondente da installare.

 

 



