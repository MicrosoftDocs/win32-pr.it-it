---
title: UI_PKEY_RecentItems
description: Identifica la proprietà RecentItems dell'interfaccia utente \_ pkey \_ .
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07410d3152fb49b55460ec15c6914c53f3b6850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299970"
---
# <a name="ui_pkey_recentitems"></a>Interfaccia utente \_ pkey \_ RecentItems

Identifica la proprietà RecentItems dell'interfaccia utente \_ pkey \_ .

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

[Interfaccia utente \_ PKEY \_ aggiunto](windowsribbon-reference-properties-uipkey-pinned.md) viene usato da un'applicazione per eseguire una query sulla matrice di elementi della raccolta di elementi usati di recente (MRU) del [menu dell'applicazione](windowsribbon-controls-applicationmenu.md). Le informazioni per ogni elemento MRU sono incapsulate in un oggetto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) e includono le tre chiavi di proprietà seguenti:

-   [\_Etichetta pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-label.md)
-   [Interfaccia utente \_ pkey \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [Interfaccia utente \_ pkey \_ bloccata](windowsribbon-reference-properties-uipkey-pinned.md)

L'elenco di elementi MRU viene passato all'applicazione host della barra multifunzione come **SAFEARRAY** di puntatori [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) alle rispettive implementazioni nell'applicazione host.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà stato](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 