---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473059"
---
# <a name="iagentexshowdefaultcharacterproperties"></a><span data-ttu-id="dbb2b-103">IAgentEx::ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="dbb2b-103">IAgentEx::ShowDefaultCharacterProperties</span></span>

<span data-ttu-id="dbb2b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dbb2b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

<span data-ttu-id="dbb2b-105">Visualizza la finestra Proprietà carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="dbb2b-105">Displays default character properties window.</span></span>

-   <span data-ttu-id="dbb2b-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="dbb2b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dbb2b-107"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="dbb2b-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="dbb2b-108">Coordinata x della finestra, in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="dbb2b-108">The x-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="dbb2b-109"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="dbb2b-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="dbb2b-110">Coordinata y della finestra, in pixel, rispetto all'origine della schermata (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="dbb2b-110">The y-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="dbb2b-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span><span class="sxs-lookup"><span data-stu-id="dbb2b-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span></span>
</dt> <dd>

<span data-ttu-id="dbb2b-112">Flag di posizione predefinito.</span><span class="sxs-lookup"><span data-stu-id="dbb2b-112">Default position flag.</span></span> <span data-ttu-id="dbb2b-113">Se questo parametro è **true**, Microsoft Agent Visualizza la finestra delle proprietà per il carattere predefinito nell'ultima posizione in cui è comparso.</span><span class="sxs-lookup"><span data-stu-id="dbb2b-113">If this parameter is **True**, Microsoft Agent displays the property sheet window for the default character at the last location it appeared.</span></span>

> [!Note]  
> <span data-ttu-id="dbb2b-114">Per Windows 2000, potrebbe essere necessario chiamare la nuova API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) per assicurarsi che questa finestra diventi la finestra in primo piano.</span><span class="sxs-lookup"><span data-stu-id="dbb2b-114">For Windows 2000, it may be necessary to call the new [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API to ensure that this window becomes the foreground window.</span></span> <span data-ttu-id="dbb2b-115">Per ulteriori informazioni sull'impostazione della finestra in primo piano in Windows 2000, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="dbb2b-115">For more information about setting the foreground window under Windows 2000, see the Platform SDK documentation.</span></span>

 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="dbb2b-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dbb2b-116">See Also</span></span>

[<span data-ttu-id="dbb2b-117">**IAgentNotifySinkEx::D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="dbb2b-117">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 