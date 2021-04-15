---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifica la \_ \_ Proprietà ChangedProperties FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399477"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>Interfaccia utente \_ pkey \_ FontProperties \_ ChangedProperties

Identifica la \_ \_ Proprietà ChangedProperties FontProperties di pkey dell'interfaccia utente \_ .

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

L'interfaccia utente \_ pkey \_ FontProperties \_ ChangedProperties viene utilizzata da un'applicazione per eseguire una query solo sulle proprietà modificate dall' [interfaccia utente \_ pkey \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).

La chiamata al metodo [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) su questo oggetto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) restituisce un [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).

UI \_ pkey \_ FontProperties \_ ChangedProperties viene passato come ultimo parametro della chiamata [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) all'applicazione host della barra multifunzione.

Questa chiave di proprietà è di sola lettura.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 