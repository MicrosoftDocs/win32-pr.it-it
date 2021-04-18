---
title: Messaggi DWM
description: In questa sezione vengono fornite informazioni sui messaggi di Gestione finestre desktop (DWM).
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Gestione finestre desktop (DWM), riferimento
- DWM (Gestione finestre desktop), riferimento
- Gestione finestre desktop (DWM), messaggi
- DWM (Gestione finestre desktop), messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "106299359"
---
# <a name="dwm-messages"></a><span data-ttu-id="b0e12-107">Messaggi DWM</span><span class="sxs-lookup"><span data-stu-id="b0e12-107">DWM Messages</span></span>

<span data-ttu-id="b0e12-108">In questa sezione vengono fornite informazioni sui messaggi di Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="b0e12-108">This section contains information about the Desktop Window Manager (DWM) messages.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0e12-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b0e12-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0e12-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="b0e12-110">Topic</span></span></th>
<th><span data-ttu-id="b0e12-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0e12-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b0e12-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b0e12-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="b0e12-113">Informa tutte le finestre di primo livello che il colore di colorazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="b0e12-113">Informs all top-level windows that the colorization color has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0e12-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b0e12-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="b0e12-115">Informa tutte le finestre di primo livello che la composizione di DWM è stata abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b0e12-115">Informs all top-level windows that DWM composition has been enabled or disabled.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b0e12-116">A partire da Windows 8, la composizione di DWM è sempre abilitata, quindi questo messaggio non viene inviato indipendentemente dalle modifiche della modalità video.</span><span class="sxs-lookup"><span data-stu-id="b0e12-116">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0e12-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="b0e12-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="b0e12-118">Inviato quando i criteri di rendering dell'area non client vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="b0e12-118">Sent when the non-client area rendering policy has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0e12-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span><span class="sxs-lookup"><span data-stu-id="b0e12-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span></span><br/></td>
<td><span data-ttu-id="b0e12-120">Indica a una finestra di fornire una bitmap statica da utilizzare come <em>anteprima in tempo reale</em> (nota anche come <em>Anteprima di visualizzazione</em>) di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="b0e12-120">Instructs a window to provide a static bitmap to use as a <em>live preview</em> (also known as a <em>Peek preview</em>) of that window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0e12-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="b0e12-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span></span><br/></td>
<td><span data-ttu-id="b0e12-122">Indica a una finestra di fornire una bitmap statica da utilizzare come rappresentazione di anteprima di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="b0e12-122">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0e12-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b0e12-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="b0e12-124">Inviato quando una finestra di DWM composta viene ingrandita.</span><span class="sxs-lookup"><span data-stu-id="b0e12-124">Sent when a DWM composed window is maximized.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





