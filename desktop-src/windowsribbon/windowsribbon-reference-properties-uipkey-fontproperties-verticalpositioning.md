---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica la proprietà \_ Ui PKEY \_ FontProperties \_ VerticalPositioning.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444302"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="b5205-103">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="b5205-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="b5205-104">Identifica la proprietà \_ Ui PKEY \_ FontProperties \_ VerticalPositioning.</span><span class="sxs-lookup"><span data-stu-id="b5205-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="b5205-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5205-105">Remarks</span></span>

<span data-ttu-id="b5205-106">Ui PKEY FontProperties VerticalPositioning viene usato da un'applicazione per eseguire query sul valore dei \_ \_ controlli \_ **Apice** **e Pedice.**</span><span class="sxs-lookup"><span data-stu-id="b5205-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="b5205-107">Il valore della proprietà deriva [**dall'enumerazione \_ FONTVERTICALPOSITION dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) utente.</span><span class="sxs-lookup"><span data-stu-id="b5205-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="b5205-108">Il valore predefinito è `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="b5205-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="b5205-109">Lo screenshot seguente mostra i **pulsanti Apice** e **Pedice** della barra [**multifunzione FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="b5205-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="b5205-111">La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b5205-111">The following table describes the properties and the UI result.</span></span>



|     <span data-ttu-id="b5205-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5205-112">Property</span></span>                           |          <span data-ttu-id="b5205-113">Risultato dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b5205-113">UI Result</span></span>                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="b5205-114">**I pulsanti Apice** **e Pedice** sono disabilitati e possono essere impostati solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b5205-114">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="b5205-115">**I pulsanti Apice** **e Pedice** non sono selezionati.</span><span class="sxs-lookup"><span data-stu-id="b5205-115">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="b5205-116">**Il pulsante Apice** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="b5205-116">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="b5205-117">**Il pulsante Pedice** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="b5205-117">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="b5205-118">Non **è possibile selezionare** entrambi **i** pulsanti Apice e Pedice.</span><span class="sxs-lookup"><span data-stu-id="b5205-118">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b5205-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5205-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5205-120">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="b5205-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="b5205-121">**\_FONTVERTICALPOSITION DELL'INTERFACCIA UTENTE**</span><span class="sxs-lookup"><span data-stu-id="b5205-121">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="b5205-122">Controllo Carattere</span><span class="sxs-lookup"><span data-stu-id="b5205-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 