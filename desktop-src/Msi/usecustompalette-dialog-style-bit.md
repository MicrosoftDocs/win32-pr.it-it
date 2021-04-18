---
description: Se questo bit è impostato, le immagini nella finestra di dialogo vengono create con la tavolozza personalizzata (una per finestra di dialogo ricevuta dal primo controllo creato). Se il bit non è impostato, il rendering delle immagini viene eseguito utilizzando una tavolozza predefinita.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Bit di stile della finestra di dialogo UseCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318981"
---
# <a name="usecustompalette-dialog-style-bit"></a><span data-ttu-id="903e5-104">Bit di stile della finestra di dialogo UseCustomPalette</span><span class="sxs-lookup"><span data-stu-id="903e5-104">UseCustomPalette Dialog Style Bit</span></span>

<span data-ttu-id="903e5-105">Se questo bit è impostato, le immagini nella finestra di dialogo vengono create con la tavolozza personalizzata (una per finestra di dialogo ricevuta dal primo controllo creato).</span><span class="sxs-lookup"><span data-stu-id="903e5-105">If this bit is set, the pictures on the dialog box are created with the custom palette (one per dialog received from the first control created).</span></span> <span data-ttu-id="903e5-106">Se il bit non è impostato, il rendering delle immagini viene eseguito utilizzando una tavolozza predefinita.</span><span class="sxs-lookup"><span data-stu-id="903e5-106">If the bit is not set, the pictures are rendered using a default palette.</span></span>

<span data-ttu-id="903e5-107">In genere si imposta questo bit se la finestra di dialogo contiene un'immagine con una tavolozza speciale o diverse immagini che condividono una tavolozza personalizzata.</span><span class="sxs-lookup"><span data-stu-id="903e5-107">Typically one would set this bit if the dialog contains a picture with a special palette, or several pictures sharing a custom palette.</span></span> <span data-ttu-id="903e5-108">Non impostare il bit se la finestra di dialogo contiene diverse immagini con tavolozze diverse.</span><span class="sxs-lookup"><span data-stu-id="903e5-108">The bit should not be set if the dialog contains several pictures with different palettes.</span></span> <span data-ttu-id="903e5-109">In questo caso, è più probabile che la tavolozza predefinita fornisca un risultato soddisfacente per tutte le immagini.</span><span class="sxs-lookup"><span data-stu-id="903e5-109">In this case, the default palette is most likely to give a satisfactory result for all pictures.</span></span>

## <a name="value"></a><span data-ttu-id="903e5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="903e5-110">Value</span></span>



| <span data-ttu-id="903e5-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="903e5-111">Decimal</span></span> | <span data-ttu-id="903e5-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="903e5-112">Hexadecimal</span></span> | <span data-ttu-id="903e5-113">Costante</span><span class="sxs-lookup"><span data-stu-id="903e5-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="903e5-114">64</span><span class="sxs-lookup"><span data-stu-id="903e5-114">64</span></span>      | <span data-ttu-id="903e5-115">0x00000040</span><span class="sxs-lookup"><span data-stu-id="903e5-115">0x00000040</span></span>  | <span data-ttu-id="903e5-116">**msidbDialogAttributesUseCustomPalette**</span><span class="sxs-lookup"><span data-stu-id="903e5-116">**msidbDialogAttributesUseCustomPalette**</span></span> |



 

 

 



