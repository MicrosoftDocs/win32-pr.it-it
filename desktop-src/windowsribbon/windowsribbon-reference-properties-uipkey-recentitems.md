---
title: UI_PKEY_RecentItems
description: Identifica la proprietà \_ RecentItems PKEY \_ dell'interfaccia utente.
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04e18400f297edae1f9a1eda54bccbcd6c31c9f1d9b40408e243b6c275a83ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437957"
---
# <a name="ui_pkey_recentitems"></a>UI \_ PKEY \_ RecentItems

Identifica la proprietà \_ RecentItems PKEY \_ dell'interfaccia utente.

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a>Commenti

[Interfaccia utente \_ PKEY \_ Pinned viene](windowsribbon-reference-properties-uipkey-pinned.md) usato da un'applicazione per eseguire una query sulla matrice di elementi nella raccolta di elementi usati più di recente del menu [dell'applicazione](windowsribbon-controls-applicationmenu.md). Le informazioni per ogni elemento MRU sono incapsulate in un [**oggetto IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) e includono le tre chiavi di proprietà seguenti:

-   [Etichetta \_ PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md)
-   [UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [CHIAVE \_ PKEY \_ dell'interfaccia utente bloccata](windowsribbon-reference-properties-uipkey-pinned.md)

L'elenco di elementi MRU viene passato all'applicazione host della barra multifunzione come **SAFEARRAY** di puntatori [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) alle rispettive implementazioni nell'applicazione host.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà di stato](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 