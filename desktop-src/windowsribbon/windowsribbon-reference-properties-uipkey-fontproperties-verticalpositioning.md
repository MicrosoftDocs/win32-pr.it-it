---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica la \_ \_ Proprietà VerticalPositioning FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047212"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="cd949-103">Interfaccia utente \_ pkey \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="cd949-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="cd949-104">Identifica la \_ \_ Proprietà VerticalPositioning FontProperties di pkey dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="cd949-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="cd949-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd949-105">Remarks</span></span>

<span data-ttu-id="cd949-106">L'interfaccia utente \_ pkey \_ FontProperties \_ VerticalPositioning viene utilizzata da un'applicazione per eseguire una query sul valore dei controlli **apice** e **pedice** .</span><span class="sxs-lookup"><span data-stu-id="cd949-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="cd949-107">Il valore della proprietà è dall' [**enumerazione \_ FONTVERTICALPOSITION dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) .</span><span class="sxs-lookup"><span data-stu-id="cd949-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="cd949-108">Il valore predefinito è `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="cd949-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="cd949-109">La schermata seguente mostra i pulsanti **apice e** **Indice** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="cd949-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="cd949-111">Nella tabella seguente vengono descritte le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="cd949-111">The following table describes the properties and the UI result.</span></span>



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="cd949-112">I pulsanti apice e **pedice** sono disabilitati **e possono** essere impostati solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd949-112">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="cd949-113">I pulsanti **apice e** **pedice** non sono selezionati.</span><span class="sxs-lookup"><span data-stu-id="cd949-113">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="cd949-114">Il pulsante **apice** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="cd949-114">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="cd949-115">Il pulsante **Indice** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="cd949-115">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="cd949-116">Non è possibile selezionare **entrambi i pulsanti apice e** **pedice** .</span><span class="sxs-lookup"><span data-stu-id="cd949-116">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cd949-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd949-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd949-118">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="cd949-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="cd949-119">**interfaccia utente \_ FONTVERTICALPOSITION**</span><span class="sxs-lookup"><span data-stu-id="cd949-119">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="cd949-120">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="cd949-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 