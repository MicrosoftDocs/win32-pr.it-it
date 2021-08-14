---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica la proprietà \_ PKEY \_ QuickAccessToolbarDock dell'interfaccia utente.
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9011cceb9b2ec96680ea3badd0ad40ae6121c14a70e065cfbfff5f5fe8e1f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201381"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>UI \_ PKEY \_ QuickAccessToolbarDock

Identifica la proprietà \_ PKEY \_ QuickAccessToolbarDock dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a>Commenti

UI \_ PKEY QuickAccessToolbarDock viene usato da un'applicazione per eseguire query sullo stato di ancoraggio della \_ barra di accesso rapido.

Il valore della proprietà deriva [**dall'enumerazione \_ CONTROLDOCK dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) utente.



|    Enumerazione                     |    Descrizione                                                                                                                                                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONTROLLO \_ DELL'INTERFACCIA UTENTEDOCK \_ TOP    | L'interfaccia della riga di comando è ancorata nell'area non client dell'applicazione host della barra multifunzione, come illustrato nello screenshot seguente.![Screenshot della barra degli strumenti di accesso rapido ancorata sopra la barra multifunzione nell'area non client.](images/properties/qat-docktop.png)<br/> |
| CONTROLLO INTERFACCIA \_ UTENTEDOCK \_ BOTTOM | QAT è ancorato come banda visivamente integrale sotto la barra multifunzione, come illustrato nello screenshot seguente. ![screenshot della barra degli strumenti di accesso rapido ancorata sotto la barra multifunzione.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà della barra multifunzione](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

