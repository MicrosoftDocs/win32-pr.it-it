---
title: UI_PKEY_FontProperties_Underline
description: Identifica la \_ proprietà di \_ sottolineatura pkey FontProperties dell'interfaccia utente \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473587"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="98a04-103">\_ \_ Sottolineato FontProperties pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="98a04-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="98a04-104">Identifica la \_ proprietà di \_ sottolineatura pkey FontProperties dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="98a04-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="98a04-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="98a04-105">Remarks</span></span>

<span data-ttu-id="98a04-106">L'interfaccia utente \_ pkey \_ FontProperties \_ Underline viene utilizzata da un'applicazione per eseguire una query sullo stato del pulsante **sottolineato** .</span><span class="sxs-lookup"><span data-stu-id="98a04-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="98a04-107">Il valore della proprietà è dall' [**enumerazione \_ FONTUNDERLINE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .</span><span class="sxs-lookup"><span data-stu-id="98a04-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="98a04-108">Il valore predefinito è `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="98a04-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="98a04-109">Lo screenshot seguente mostra il pulsante **sottolineato** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="98a04-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="98a04-111">Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="98a04-111">The following table describes the properties and the UI result.</span></span>



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="98a04-112">Il pulsante **sottolineato** è disabilitato e può essere impostato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="98a04-112">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="98a04-113">Il pulsante **sottolineato** non è selezionato.</span><span class="sxs-lookup"><span data-stu-id="98a04-113">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="98a04-114">Il pulsante **sottolineatura** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="98a04-114">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="98a04-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="98a04-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a04-116">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="98a04-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="98a04-117">**interfaccia utente \_ FONTUNDERLINE**</span><span class="sxs-lookup"><span data-stu-id="98a04-117">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="98a04-118">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="98a04-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 