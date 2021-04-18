---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica la proprietà QuickAccessToolbarDock dell'interfaccia utente \_ pkey \_ .
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ae48cb9ef2ee665739de2f3aacab197b461665
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399107"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>Interfaccia utente \_ pkey \_ QuickAccessToolbarDock

Identifica la proprietà QuickAccessToolbarDock dell'interfaccia utente \_ pkey \_ .

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

L'interfaccia utente \_ pkey \_ QuickAccessToolbarDock viene usata da un'applicazione per eseguire una query sullo stato di ancoraggio della barra di accesso rapido (QAT).

Il valore della proprietà è dall' [**enumerazione \_ CONTROLDOCK dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) .



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| interfaccia utente \_ CONTROLDOCK \_ Top    | Il QAT è ancorato nell'area non client dell'applicazione host della barra multifunzione, come illustrato nella schermata seguente.![screenshot della barra di accesso rapido ancorata sopra la barra multifunzione nell'area non client.](images/properties/qat-docktop.png)<br/> |
| interfaccia utente \_ CONTROLDOCK in \_ basso | Il QAT è ancorato come una banda integrale visiva sotto la barra multifunzione, come illustrato nella schermata seguente. ![screenshot della barra di accesso rapido ancorata sotto la barra multifunzione.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà della barra multifunzione](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

