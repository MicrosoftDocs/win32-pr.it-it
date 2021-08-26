---
description: L'azione RegisterProgIdInfo gestisce la registrazione delle informazioni progId OLE con il sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Azione RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cebf5ddb3bf8b9c98ebea0364b685016d343afa283b937400360f31bbcebd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912831"
---
# <a name="registerprogidinfo-action"></a>Azione RegisterProgIdInfo

L'azione RegisterProgIdInfo gestisce la registrazione delle informazioni progId OLE con il sistema.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione RegisterProgIdInfo deve essere eseguita dopo l'azione [InstallFiles,](installfiles-action.md) [l'azione UnregisterProgIdInfo,](unregisterprogidinfo-action.md) [l'azione RegisterClassInfo](registerclassinfo-action.md) e l'azione [RegisterExtensionInfo.](registerextensioninfo-action.md)

La sequenziazione delle azioni nel gruppo seguente è limitata. Se un subset di queste azioni si verifica insieme in una tabella di sequenza, deve avere lo stesso ordine di sequenza relativo come illustrato:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Annullare la registrazione diMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Ad esempio, RegisterProgIdInfo deve essere successivo a [RegisterExtensionInfo](registerextensioninfo-action.md) nella tabella di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                |
|-------|-------------------------------------------|
| \[1\] | Identificatore di programma del programma registrato. |



 

## <a name="remarks"></a>Commenti

L'azione RegisterProgIdInfo registra tutte le informazioni ProgId per i server specificati nella tabella [ProgId](progid-table.md) e per i quali è stato selezionato il server di classi o il server di estensione corrispondente per l'installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella delle classi](class-table.md)
</dt> <dt>

[Tabella delle estensioni](extension-table.md)
</dt> </dl>

 

 



