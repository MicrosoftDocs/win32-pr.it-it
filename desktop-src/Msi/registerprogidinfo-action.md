---
description: L'azione RegisterProgIdInfo gestisce la registrazione delle informazioni OLE ProgId con il sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Azione RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311707"
---
# <a name="registerprogidinfo-action"></a>Azione RegisterProgIdInfo

L'azione RegisterProgIdInfo gestisce la registrazione delle informazioni OLE ProgId con il sistema.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RegisterProgIdInfo deve provenire dopo l'azione [InstallFiles](installfiles-action.md) , l'azione [UnregisterProgIdInfo](unregisterprogidinfo-action.md) , l'azione [registerClassInfo](registerclassinfo-action.md) e l'azione [RegisterExtensionInfo](registerextensioninfo-action.md) .

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, è necessario che disponga dello stesso ordine di sequenza relativo, come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, RegisterProgIdInfo deve essere seguito da [RegisterExtensionInfo](registerextensioninfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                |
|-------|-------------------------------------------|
| \[1\] | Identificatore del programma registrato. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterProgIdInfo registra tutte le informazioni sul ProgId per i server specificati nella [tabella ProgId](progid-table.md) e per cui è stato selezionato il server di classe o il server di estensione corrispondente da installare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella classi](class-table.md)
</dt> <dt>

[Tabella di estensione](extension-table.md)
</dt> </dl>

 

 



