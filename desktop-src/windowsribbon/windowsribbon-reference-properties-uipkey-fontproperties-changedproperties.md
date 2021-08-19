---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifica la proprietà \_ Ui PKEY \_ FontProperties \_ ChangedProperties.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36262a9acf217e448956f108b68cb0716b5b5080c71f6a2a8e305c9e59478c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028659"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>UI \_ PKEY \_ FontProperties \_ ChangedProperties

Identifica la proprietà \_ Ui PKEY \_ FontProperties \_ ChangedProperties.

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>Commenti

UI PKEY FontProperties ChangedProperties viene usato da un'applicazione per eseguire query solo su \_ proprietà modificate da UI \_ \_ [ \_ PKEY \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).

La chiamata [**al metodo IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) su questo [**oggetto IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) restituisce un [oggetto IPropertyStore.](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Ui PKEY FontProperties ChangedProperties viene passato come ultimo parametro della chiamata \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) all'applicazione host della barra multifunzione.

Questa chiave di proprietà è di sola lettura.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Controllo Font](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 