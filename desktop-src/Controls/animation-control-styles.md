---
title: Stili del controllo Animation (CommCtrl. h)
description: Questa sezione elenca gli stili della finestra usati con i controlli di animazione.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327604"
---
# <a name="animation-control-styles"></a><span data-ttu-id="85c5c-103">Stili del controllo di animazione</span><span class="sxs-lookup"><span data-stu-id="85c5c-103">Animation Control Styles</span></span>

<span data-ttu-id="85c5c-104">Questa sezione elenca gli stili della finestra usati con i controlli di animazione.</span><span class="sxs-lookup"><span data-stu-id="85c5c-104">This section lists the window styles used with animation controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="85c5c-105">Costante</span><span class="sxs-lookup"><span data-stu-id="85c5c-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="85c5c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85c5c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <span data-ttu-id="85c5c-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85c5c-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="85c5c-108">Avvia la riproduzione dell'animazione non appena viene aperto il clip AVI.</span><span class="sxs-lookup"><span data-stu-id="85c5c-108">Starts playing the animation as soon as the AVI clip is opened.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <span data-ttu-id="85c5c-109"><dt><strong>ACS_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85c5c-109"><dt><strong>ACS_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="85c5c-110">Centra l'animazione nella finestra del controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="85c5c-110">Centers the animation in the animation control's window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <span data-ttu-id="85c5c-111"><dt><strong>ACS_TIMER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85c5c-111"><dt><strong>ACS_TIMER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="85c5c-112">Per impostazione predefinita, il controllo Crea un thread per riprodurre il clip AVI.</span><span class="sxs-lookup"><span data-stu-id="85c5c-112">By default, the control creates a thread to play the AVI clip.</span></span> <span data-ttu-id="85c5c-113">Se si imposta questo flag, il controllo riproduce il clip senza creare un thread. internamente il controllo Usa un timer Win32 per sincronizzare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="85c5c-113">If you set this flag, the control plays the clip without creating a thread; internally the control uses a Win32 timer to synchronize playback.</span></span> <br/> <span data-ttu-id="85c5c-114"><strong>Comctl32.dll versione 6 e successive:</strong> Questo stile non è supportato.</span><span class="sxs-lookup"><span data-stu-id="85c5c-114"><strong>Comctl32.dll version 6 and later:</strong> This style is not supported.</span></span> <span data-ttu-id="85c5c-115">Per impostazione predefinita, il controllo riproduce il clip AVI senza creare un thread.</span><span class="sxs-lookup"><span data-stu-id="85c5c-115">By default, the control plays the AVI clip without creating a thread.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="85c5c-116">Comctl32.dll versione 6 non è ridistribuibile.</span><span class="sxs-lookup"><span data-stu-id="85c5c-116">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="85c5c-117">Per usare Comctl32.dll versione 6, specificarla in un manifesto.</span><span class="sxs-lookup"><span data-stu-id="85c5c-117">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="85c5c-118">Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="85c5c-118">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <span data-ttu-id="85c5c-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85c5c-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="85c5c-120">Consente di associare il colore di sfondo di un'animazione a quello della finestra sottostante, creando uno &quot; &quot; sfondo trasparente.</span><span class="sxs-lookup"><span data-stu-id="85c5c-120">Allows you to match an animation's background color to that of the underlying window, creating a &quot;transparent&quot; background.</span></span> <span data-ttu-id="85c5c-121">L'elemento padre del controllo animazione non deve avere lo stile WS_CLIPCHILDREN (vedere <a href="/windows/desktop/winmsg/window-styles">stili della finestra</a>).</span><span class="sxs-lookup"><span data-stu-id="85c5c-121">The parent of the animation control must not have the WS_CLIPCHILDREN style (see <a href="/windows/desktop/winmsg/window-styles">Window Styles</a>).</span></span> <span data-ttu-id="85c5c-122">Il controllo Invia un messaggio di <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> al relativo elemento padre.</span><span class="sxs-lookup"><span data-stu-id="85c5c-122">The control sends a <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> message to its parent.</span></span> <span data-ttu-id="85c5c-123">Usare <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> per impostare il colore di sfondo per il contesto di dispositivo su un valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="85c5c-123">Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> to set the background color for the device context to an appropriate value.</span></span> <span data-ttu-id="85c5c-124">Il controllo interpreta il pixel superiore sinistro del primo fotogramma come colore di sfondo predefinito dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="85c5c-124">The control interprets the upper-left pixel of the first frame as the animation's default background color.</span></span> <span data-ttu-id="85c5c-125">Verrà rimappato tutti i pixel con tale colore al valore fornito in risposta a WM_CTLCOLORSTATIC.</span><span class="sxs-lookup"><span data-stu-id="85c5c-125">It will remap all pixels with that color to the value you supplied in response to WM_CTLCOLORSTATIC.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="85c5c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85c5c-126">Requirements</span></span>



| <span data-ttu-id="85c5c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c5c-127">Requirement</span></span> | <span data-ttu-id="85c5c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="85c5c-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85c5c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85c5c-129">Header</span></span><br/> | <dl> <span data-ttu-id="85c5c-130"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85c5c-130"><dt>CommCtrl.h</dt></span></span> </dl> |



