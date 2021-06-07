---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica la proprietà \_ \_ DeltaSize FontProperties PKEY \_ dell'interfaccia utente.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444392"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="aec40-103">UI \_ PKEY \_ FontProperties \_ DeltaSize</span><span class="sxs-lookup"><span data-stu-id="aec40-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="aec40-104">Identifica la proprietà \_ \_ DeltaSize FontProperties PKEY \_ dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="aec40-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="aec40-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="aec40-105">Remarks</span></span>

<span data-ttu-id="aec40-106">Ui PKEY FontProperties DeltaSize viene usato da un'applicazione nei casi in cui non è possibile per l'applicazione specificare un valore per Dimensioni carattere, ad esempio quando viene selezionata un'esecuzione di testo di \_ \_ dimensioni \_ eterogenee. </span><span class="sxs-lookup"><span data-stu-id="aec40-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="aec40-107">Il **controllo Dimensioni carattere è** impostato su vuoto e l'interfaccia utente \_ PKEY FontProperties DeltaSize viene usata per acquisire l'interazione dell'utente con i pulsanti Aumenta e Riduci \_ \_ carattere.  </span><span class="sxs-lookup"><span data-stu-id="aec40-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="aec40-108">UI \_ PKEY \_ FontProperties \_ DeltaSize è incluso in [UI \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span><span class="sxs-lookup"><span data-stu-id="aec40-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="aec40-109">Lo screenshot seguente mostra i pulsanti **Aumenta carattere e** Riduci carattere del controllo FontControl della barra [**multifunzione.**](windowsribbon-element-fontcontrol.md) </span><span class="sxs-lookup"><span data-stu-id="aec40-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot dei pulsanti per l'estensione e la riduzione del tipo di carattere in fontcontrol.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="aec40-111">Nella tabella seguente vengono descritti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="aec40-111">The following table describes the property values.</span></span>



|     <span data-ttu-id="aec40-112">Valore</span><span class="sxs-lookup"><span data-stu-id="aec40-112">Value</span></span>                 |  <span data-ttu-id="aec40-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aec40-113">Description</span></span>                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="aec40-114">**Pulsante Aumenta dimensioni** carattere selezionato.</span><span class="sxs-lookup"><span data-stu-id="aec40-114">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="aec40-115">**È stato fatto clic sul** pulsante Riduci carattere.</span><span class="sxs-lookup"><span data-stu-id="aec40-115">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="aec40-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aec40-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec40-117">Proprietà del controllo Font</span><span class="sxs-lookup"><span data-stu-id="aec40-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="aec40-118">**\_FONTDELTASIZE DELL'INTERFACCIA UTENTE**</span><span class="sxs-lookup"><span data-stu-id="aec40-118">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="aec40-119">Controllo Font</span><span class="sxs-lookup"><span data-stu-id="aec40-119">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 