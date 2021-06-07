---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la proprietà \_ PKEY \_ FontProperties \_ Strikethrough dell'interfaccia utente.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b684704fdd90a8dd1b88b14db2b52540b15fccb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443792"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="6c1dc-103">Carattere \_ PKEY \_ dell'interfaccia \_ utenteProprietà barrato</span><span class="sxs-lookup"><span data-stu-id="6c1dc-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="6c1dc-104">Identifica la proprietà \_ PKEY \_ FontProperties \_ Strikethrough dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6c1dc-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="6c1dc-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c1dc-105">Remarks</span></span>

<span data-ttu-id="6c1dc-106">Ui \_ PKEY \_ FontProperties \_ Strikethrough viene usato da un'applicazione per eseguire query sullo stato del **pulsante Barrato.**</span><span class="sxs-lookup"><span data-stu-id="6c1dc-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="6c1dc-107">Il valore della proprietà deriva [**dall'enumerazione \_ FONTPROPERTIES dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) utente.</span><span class="sxs-lookup"><span data-stu-id="6c1dc-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="6c1dc-108">Il valore predefinito è `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="6c1dc-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="6c1dc-109">Lo screenshot seguente mostra il **pulsante Barrato** della barra [**multifunzione FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="6c1dc-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="6c1dc-111">La tabella seguente descrive le proprietà e il risultato dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6c1dc-111">The following table describes the properties and the UI result.</span></span>



|   <span data-ttu-id="6c1dc-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c1dc-112">Property</span></span>                       |    <span data-ttu-id="6c1dc-113">Risultato dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="6c1dc-113">UI Result</span></span>                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="6c1dc-114">**Il pulsante barrato** è disabilitato e può essere impostato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c1dc-114">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="6c1dc-115">**Il pulsante Barrato** non è selezionato.</span><span class="sxs-lookup"><span data-stu-id="6c1dc-115">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="6c1dc-116">**Il pulsante Barrato** è selezionato.</span><span class="sxs-lookup"><span data-stu-id="6c1dc-116">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="6c1dc-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c1dc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c1dc-118">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="6c1dc-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="6c1dc-119">**PROPRIETÀ FONT \_ DELL'INTERFACCIA UTENTE**</span><span class="sxs-lookup"><span data-stu-id="6c1dc-119">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="6c1dc-120">Controllo Carattere</span><span class="sxs-lookup"><span data-stu-id="6c1dc-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 