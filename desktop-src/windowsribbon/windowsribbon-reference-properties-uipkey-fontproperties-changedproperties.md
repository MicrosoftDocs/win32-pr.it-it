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
# <a name="ui_pkey_fontproperties_changedproperties"></a><span data-ttu-id="27b92-103">Interfaccia utente \_ pkey \_ FontProperties \_ ChangedProperties</span><span class="sxs-lookup"><span data-stu-id="27b92-103">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>

<span data-ttu-id="27b92-104">Identifica la \_ \_ Proprietà ChangedProperties FontProperties di pkey dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="27b92-104">Identifies the UI\_PKEY\_FontProperties\_ChangedProperties property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a><span data-ttu-id="27b92-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="27b92-105">Remarks</span></span>

<span data-ttu-id="27b92-106">L'interfaccia utente \_ pkey \_ FontProperties \_ ChangedProperties viene utilizzata da un'applicazione per eseguire una query solo sulle proprietà modificate dall' [interfaccia utente \_ pkey \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span><span class="sxs-lookup"><span data-stu-id="27b92-106">UI\_PKEY\_FontProperties\_ChangedProperties is used by an application to query only changed properties from [UI\_PKEY\_FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span></span>

<span data-ttu-id="27b92-107">La chiamata al metodo [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) su questo oggetto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) restituisce un [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="27b92-107">Calling the [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method on this [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object returns an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

<span data-ttu-id="27b92-108">UI \_ pkey \_ FontProperties \_ ChangedProperties viene passato come ultimo parametro della chiamata [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) all'applicazione host della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="27b92-108">UI\_PKEY\_FontProperties\_ChangedProperties is passed as the last parameter of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) call to the Ribbon host application.</span></span>

<span data-ttu-id="27b92-109">Questa chiave di proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="27b92-109">This property key is read-only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27b92-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27b92-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27b92-111">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="27b92-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="27b92-112">**IUISimplePropertySet**</span><span class="sxs-lookup"><span data-stu-id="27b92-112">**IUISimplePropertySet**</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[<span data-ttu-id="27b92-113">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="27b92-113">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 