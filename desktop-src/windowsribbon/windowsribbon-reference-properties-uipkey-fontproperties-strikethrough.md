---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la \_ \_ proprietà barrata pkey FontProperties dell'interfaccia utente \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399561"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="47d4b-103">Barra dell'interfaccia utente \_ pkey \_ FontProperties \_</span><span class="sxs-lookup"><span data-stu-id="47d4b-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="47d4b-104">Identifica la \_ \_ proprietà barrata pkey FontProperties dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="47d4b-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="47d4b-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="47d4b-105">Remarks</span></span>

<span data-ttu-id="47d4b-106">UI \_ pkey \_ FontProperties \_ barrato viene usato da un'applicazione per eseguire una query sullo stato del pulsante **barrato** .</span><span class="sxs-lookup"><span data-stu-id="47d4b-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="47d4b-107">Il valore della proprietà è dall' [**enumerazione \_ FONTPROPERTIES dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="47d4b-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="47d4b-108">Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="47d4b-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="47d4b-109">Lo screenshot seguente mostra il pulsante **barrato** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="47d4b-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="47d4b-111">Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="47d4b-111">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="47d4b-112">Il pulsante **barrato** è disabilitato e può essere impostato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47d4b-112">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="47d4b-113">Il pulsante **barrato** non è selezionato.</span><span class="sxs-lookup"><span data-stu-id="47d4b-113">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="47d4b-114">Il pulsante **barrato** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="47d4b-114">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="47d4b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47d4b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47d4b-116">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="47d4b-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="47d4b-117">**interfaccia utente \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="47d4b-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="47d4b-118">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="47d4b-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 