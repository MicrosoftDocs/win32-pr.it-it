---
title: UI_PKEY_FontProperties_Bold
description: Identifica la \_ \_ Proprietà FontProperties Bold dell'interfaccia utente pkey \_ .
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300234"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="7a85f-103">Interfaccia utente \_ pkey \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="7a85f-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="7a85f-104">Identifica la \_ \_ Proprietà FontProperties Bold dell'interfaccia utente pkey \_ .</span><span class="sxs-lookup"><span data-stu-id="7a85f-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="7a85f-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a85f-105">Remarks</span></span>

<span data-ttu-id="7a85f-106">L'interfaccia utente \_ pkey \_ FontProperties \_ Bold viene utilizzata da un'applicazione per eseguire una query sullo stato del pulsante in **grassetto** .</span><span class="sxs-lookup"><span data-stu-id="7a85f-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="7a85f-107">Il valore della proprietà è dall' [**enumerazione \_ FONTPROPERTIES dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="7a85f-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="7a85f-108">Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="7a85f-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="7a85f-109">Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7a85f-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="7a85f-110">Il pulsante **grassetto** è disabilitato e può essere impostato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7a85f-110">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="7a85f-111">Il pulsante **grassetto** non è selezionato.</span><span class="sxs-lookup"><span data-stu-id="7a85f-111">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="7a85f-112">Il pulsante **grassetto** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="7a85f-112">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="7a85f-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a85f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a85f-114">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="7a85f-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="7a85f-115">**interfaccia utente \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="7a85f-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="7a85f-116">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="7a85f-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 