---
title: UI_PKEY_FontProperties_Size
description: Identifica la proprietà della dimensione FontProperties dell'interfaccia utente \_ pkey \_ \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297767"
---
# <a name="ui_pkey_fontproperties_size"></a><span data-ttu-id="06987-103">\_ \_ Dimensioni FontProperties dell'interfaccia utente pkey \_</span><span class="sxs-lookup"><span data-stu-id="06987-103">UI\_PKEY\_FontProperties\_Size</span></span>

<span data-ttu-id="06987-104">Identifica la proprietà della dimensione FontProperties dell'interfaccia utente \_ pkey \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="06987-104">Identifies the UI\_PKEY\_FontProperties\_Size property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a><span data-ttu-id="06987-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="06987-105">Remarks</span></span>

<span data-ttu-id="06987-106">L'interfaccia utente \_ pkey \_ FontProperties \_ dimensioni viene utilizzata da un'applicazione per eseguire una query sul valore del controllo **dimensioni carattere** .</span><span class="sxs-lookup"><span data-stu-id="06987-106">UI\_PKEY\_FontProperties\_Size is used by an application to query the value of the **Font size** control.</span></span>

<span data-ttu-id="06987-107">I valori validi per questa proprietà sono compresi tra 1 e 9999 inclusi.</span><span class="sxs-lookup"><span data-stu-id="06987-107">Valid values for this property range from 1 to 9999, inclusive.</span></span> <span data-ttu-id="06987-108">Se un utente tenta di immettere un valore non valido, la voce viene rifiutata e il controllo della **dimensione del carattere** viene ripristinato all'ultimo valore valido.</span><span class="sxs-lookup"><span data-stu-id="06987-108">If a user tries to enter an invalid value, the entry is rejected and the **Font size** control reverts to the last valid value.</span></span>

<span data-ttu-id="06987-109">Se un'applicazione tenta di impostare le dimensioni del carattere a livello di codice su un valore non compreso nell'intervallo valido, il Framework della barra multifunzione invalida tutte le proprietà del tipo di carattere e imposta i controlli del tipo di carattere (**dimensione** del carattere e **tipo di carattere**) su blank o sullo stato predefinito, laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="06987-109">If an application attempts to set font size programmatically to a value outside the valid range, the Ribbon framework invalidates all font properties and sets the font controls (**Font size** and **Font face**) to blank or to their default state, where appropriate.</span></span>

<span data-ttu-id="06987-110">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="06987-110">The default value is 0.</span></span>

<span data-ttu-id="06987-111">Il valore 0 indica che non è selezionata alcuna dimensione a punto singolo (nessun testo o un'esecuzione di testo di dimensioni eterogenee).</span><span class="sxs-lookup"><span data-stu-id="06987-111">A value of 0 specifies that no single point size is selected (either no text, or a run of heterogeneously sized text, is selected).</span></span>

<span data-ttu-id="06987-112">Un utente non può impostare il controllo della **dimensione del carattere** su 0.</span><span class="sxs-lookup"><span data-stu-id="06987-112">A user cannot set the **Font size** control to 0.</span></span>

<span data-ttu-id="06987-113">Diverso da 0, i valori validi per \_ l'interfaccia utente pkey \_ FontProperties \_ dimensioni variano tra *MinimumFontSize* e *MaximumFontSize* come dichiarato nel markup del controllo del [tipo di carattere](windowsribbon-controls-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="06987-113">Other than 0, valid values for UI\_PKEY\_FontProperties\_Size range between *MinimumFontSize* and *MaximumFontSize* as declared in the [Font Control](windowsribbon-controls-fontcontrol.md) markup.</span></span>

> [!Note]  
> <span data-ttu-id="06987-114">Il controllo **dimensioni carattere** è impostato su blank quando la dimensione del carattere è impostata a livello di codice su 0, ad esempio quando viene evidenziata un'esecuzione di testo di dimensioni eterogenee.</span><span class="sxs-lookup"><span data-stu-id="06987-114">The **Font size** control is set to blank when the font size is programmatically set to 0, such as when a run of heterogeneously sized text is highlighted.</span></span>

 

<span data-ttu-id="06987-115">Quando viene selezionata un'esecuzione di testo di dimensioni eterogenee, l'applicazione deve eseguire una query sull' [interfaccia utente \_ pkey \_ FontProperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) per acquisire i comandi di **aumento** dei tipi di carattere e **compatta** .</span><span class="sxs-lookup"><span data-stu-id="06987-115">Where a run of heterogeneously sized text is selected, the application should query [UI\_PKEY\_FontProperties\_DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) to capture **Grow font** and **Shrink font** commands.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06987-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06987-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06987-117">Proprietà del controllo del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="06987-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="06987-118">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="06987-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




