---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica la \_ \_ Proprietà DeltaSize FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046760"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="3c4db-103">Interfaccia utente \_ pkey \_ FontProperties \_ DeltaSize</span><span class="sxs-lookup"><span data-stu-id="3c4db-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="3c4db-104">Identifica la \_ \_ Proprietà DeltaSize FontProperties di pkey dell'interfaccia utente \_ .</span><span class="sxs-lookup"><span data-stu-id="3c4db-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="3c4db-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c4db-105">Remarks</span></span>

<span data-ttu-id="3c4db-106">L'interfaccia utente \_ pkey \_ FontProperties \_ DeltaSize viene utilizzata da un'applicazione nei casi in cui non è possibile che l'applicazione specifichi un valore per le **dimensioni del carattere**, ad esempio quando viene selezionata un'esecuzione di testo di dimensioni eterogenee.</span><span class="sxs-lookup"><span data-stu-id="3c4db-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="3c4db-107">Il controllo delle **dimensioni del carattere** è impostato su Blank e l'interfaccia utente \_ pkey \_ FontProperties \_ DeltaSize viene utilizzata per acquisire l'interazione dell'utente con i pulsanti di **espansione del tipo di carattere** e **compattazione dei caratteri** .</span><span class="sxs-lookup"><span data-stu-id="3c4db-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="3c4db-108">UI \_ pkey \_ FontProperties \_ DeltaSize è incluso nell' [interfaccia \_ utente \_ pkey \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)ChangedProperties.</span><span class="sxs-lookup"><span data-stu-id="3c4db-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="3c4db-109">La schermata seguente mostra i pulsanti **dimensioni** del carattere e **compattazione del carattere** della barra multifunzione [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="3c4db-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![cattura di schermata dei pulsanti dimensioni e compattazione carattere in fontcontrol.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="3c4db-111">Nella tabella seguente vengono descritti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="3c4db-111">The following table describes the property values.</span></span>



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="3c4db-112">Pulsante **aumenta carattere** selezionato.</span><span class="sxs-lookup"><span data-stu-id="3c4db-112">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="3c4db-113">Pulsante **compatta carattere** selezionato.</span><span class="sxs-lookup"><span data-stu-id="3c4db-113">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3c4db-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c4db-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c4db-115">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="3c4db-115">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="3c4db-116">**interfaccia utente \_ FONTDELTASIZE**</span><span class="sxs-lookup"><span data-stu-id="3c4db-116">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="3c4db-117">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="3c4db-117">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 