---
title: UI_PKEY_FontProperties_Italic
description: Identifica la proprietà \_ FontProperties Italic dell'interfaccia \_ utente \_ PKEY.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443812"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="3617a-103">UI \_ PKEY \_ FontProperties \_ Italic</span><span class="sxs-lookup"><span data-stu-id="3617a-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="3617a-104">Identifica la proprietà \_ FontProperties Italic dell'interfaccia \_ utente \_ PKEY.</span><span class="sxs-lookup"><span data-stu-id="3617a-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="3617a-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="3617a-105">Remarks</span></span>

<span data-ttu-id="3617a-106">Ui \_ PKEY \_ FontProperties \_ Italic viene usato da un'applicazione per eseguire query sullo stato del **pulsante Corsivo.**</span><span class="sxs-lookup"><span data-stu-id="3617a-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="3617a-107">Il valore della proprietà deriva [**dall'enumerazione \_ FONTPROPERTIES dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) utente.</span><span class="sxs-lookup"><span data-stu-id="3617a-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="3617a-108">Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="3617a-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="3617a-109">La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3617a-109">The following table describes the properties and the UI result.</span></span>



|    <span data-ttu-id="3617a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3617a-110">Property</span></span>                      |       <span data-ttu-id="3617a-111">Risultato dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="3617a-111">UI Result</span></span>                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="3617a-112">**Il pulsante** Corsivo è disabilitato e può essere impostato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3617a-112">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="3617a-113">**Il pulsante** Corsivo non è selezionato.</span><span class="sxs-lookup"><span data-stu-id="3617a-113">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="3617a-114">**Il pulsante** Corsivo è selezionato.</span><span class="sxs-lookup"><span data-stu-id="3617a-114">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="3617a-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3617a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3617a-116">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="3617a-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="3617a-117">**PROPRIETÀ FONT \_ DELL'INTERFACCIA UTENTE**</span><span class="sxs-lookup"><span data-stu-id="3617a-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="3617a-118">Controllo Carattere</span><span class="sxs-lookup"><span data-stu-id="3617a-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 