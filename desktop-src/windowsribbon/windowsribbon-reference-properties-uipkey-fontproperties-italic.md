---
title: UI_PKEY_FontProperties_Italic
description: Identifica la \_ Proprietà pkey \_ FontProperties corsivo dell'interfaccia utente \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399166"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="7c22b-103">Interfaccia utente \_ pkey \_ FontProperties \_ corsivo</span><span class="sxs-lookup"><span data-stu-id="7c22b-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="7c22b-104">Identifica la \_ Proprietà pkey \_ FontProperties corsivo dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="7c22b-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="7c22b-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c22b-105">Remarks</span></span>

<span data-ttu-id="7c22b-106">L'interfaccia utente \_ pkey \_ FontProperties \_ corsivo viene utilizzata da un'applicazione per eseguire una query sullo stato del pulsante **corsivo** .</span><span class="sxs-lookup"><span data-stu-id="7c22b-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="7c22b-107">Il valore della proprietà è dall' [**enumerazione \_ FONTPROPERTIES dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="7c22b-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="7c22b-108">Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="7c22b-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="7c22b-109">Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="7c22b-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="7c22b-110">Il pulsante **corsivo** è disabilitato e può essere impostato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c22b-110">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="7c22b-111">Il pulsante **corsivo** non è selezionato.</span><span class="sxs-lookup"><span data-stu-id="7c22b-111">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="7c22b-112">Il pulsante **corsivo** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="7c22b-112">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="7c22b-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c22b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c22b-114">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="7c22b-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="7c22b-115">**interfaccia utente \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="7c22b-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="7c22b-116">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="7c22b-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 