---
title: UI_PKEY_FontProperties_Underline
description: Identifica la proprietà \_ FontProperties Underline dell'interfaccia \_ utente \_ PKEY.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443782"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="52497-103">UI \_ PKEY \_ FontProperties \_ Underline</span><span class="sxs-lookup"><span data-stu-id="52497-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="52497-104">Identifica la proprietà \_ FontProperties Underline dell'interfaccia \_ utente \_ PKEY.</span><span class="sxs-lookup"><span data-stu-id="52497-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="52497-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="52497-105">Remarks</span></span>

<span data-ttu-id="52497-106">Ui \_ PKEY \_ FontProperties \_ Underline viene usato da un'applicazione per eseguire query sullo stato del **pulsante Sottolineatura.**</span><span class="sxs-lookup"><span data-stu-id="52497-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="52497-107">Il valore della proprietà deriva [**dall'enumerazione \_ FONTUNDERLINE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) utente.</span><span class="sxs-lookup"><span data-stu-id="52497-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="52497-108">Il valore predefinito è `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="52497-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="52497-109">Lo screenshot seguente mostra il **pulsante Sottolinea** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="52497-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="52497-111">La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="52497-111">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="52497-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52497-112">Property</span></span>                   |       <span data-ttu-id="52497-113">Risultato dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="52497-113">UI Result</span></span>                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="52497-114">**Il pulsante** Sottolineatura è disabilitato e può essere impostato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52497-114">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="52497-115">**Il pulsante** Sottolineatura non è selezionato.</span><span class="sxs-lookup"><span data-stu-id="52497-115">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="52497-116">**Il pulsante** Sottolineatura è selezionato.</span><span class="sxs-lookup"><span data-stu-id="52497-116">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="52497-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52497-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52497-118">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="52497-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="52497-119">**\_FONTUNDERLINE dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="52497-119">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="52497-120">Controllo Carattere</span><span class="sxs-lookup"><span data-stu-id="52497-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 