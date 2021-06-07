---
title: UI_PKEY_FontProperties_Bold
description: Identifica la proprietà \_ FontProperties Bold PKEY \_ \_ dell'interfaccia utente.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444382"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="b49ca-103">UI \_ PKEY \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="b49ca-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="b49ca-104">Identifica la proprietà \_ FontProperties Bold PKEY \_ \_ dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b49ca-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="b49ca-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="b49ca-105">Remarks</span></span>

<span data-ttu-id="b49ca-106">UI \_ PKEY \_ FontProperties \_ Bold viene usato da un'applicazione per eseguire query sullo stato del **pulsante** Grassetto.</span><span class="sxs-lookup"><span data-stu-id="b49ca-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="b49ca-107">Il valore della proprietà deriva dall'enumerazione [**\_ FONTPROPERTIES dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) utente.</span><span class="sxs-lookup"><span data-stu-id="b49ca-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="b49ca-108">Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="b49ca-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="b49ca-109">La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b49ca-109">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="b49ca-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b49ca-110">Property</span></span>                    |    <span data-ttu-id="b49ca-111">Risultato dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b49ca-111">UI Result</span></span>                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="b49ca-112">**Il pulsante** Grassetto è disabilitato e può essere impostato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b49ca-112">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="b49ca-113">**Il pulsante** Grassetto non è selezionato.</span><span class="sxs-lookup"><span data-stu-id="b49ca-113">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="b49ca-114">**Il pulsante** Grassetto è selezionato.</span><span class="sxs-lookup"><span data-stu-id="b49ca-114">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="b49ca-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b49ca-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b49ca-116">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="b49ca-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="b49ca-117">**PROPRIETÀ CARATTERE \_ DELL'INTERFACCIA UTENTE**</span><span class="sxs-lookup"><span data-stu-id="b49ca-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="b49ca-118">Controllo Font</span><span class="sxs-lookup"><span data-stu-id="b49ca-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 