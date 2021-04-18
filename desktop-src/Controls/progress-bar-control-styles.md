---
title: Stili del controllo indicatore di stato (CommCtrl. h)
description: Gli stili di controllo seguenti sono supportati dai controlli indicatore di stato
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327859"
---
# <a name="progress-bar-control-styles"></a><span data-ttu-id="3474c-103">Stili del controllo indicatore di stato</span><span class="sxs-lookup"><span data-stu-id="3474c-103">Progress Bar Control Styles</span></span>

<span data-ttu-id="3474c-104">Gli stili di controllo seguenti sono supportati dai controlli [indicatore di stato](progress-bar-control.md) :</span><span class="sxs-lookup"><span data-stu-id="3474c-104">The following control styles are supported by [Progress Bar](progress-bar-control.md) controls:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3474c-105">Costante</span><span class="sxs-lookup"><span data-stu-id="3474c-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3474c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3474c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <span data-ttu-id="3474c-107"><dt><strong>PBS_MARQUEE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3474c-107"><dt><strong>PBS_MARQUEE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3474c-108"><a href="common-control-versions.md">Versione 6,0</a> o successiva.</span><span class="sxs-lookup"><span data-stu-id="3474c-108"><a href="common-control-versions.md">Version 6.0</a> or later.</span></span> <span data-ttu-id="3474c-109">L'indicatore di stato non aumenta di dimensione ma si sposta ripetutamente lungo la lunghezza della barra, indicando l'attività senza specificare quale percentuale dello stato di avanzamento è completa.</span><span class="sxs-lookup"><span data-stu-id="3474c-109">The progress indicator does not grow in size but instead moves repeatedly along the length of the bar, indicating activity without specifying what proportion of the progress is complete.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3474c-110">Comctl32.dll versione 6 non è ridistribuibile ma è incluso in Windows o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3474c-110">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="3474c-111">Per usare Comctl32.dll versione 6, specificarla in un manifesto.</span><span class="sxs-lookup"><span data-stu-id="3474c-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="3474c-112">Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="3474c-112">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <span data-ttu-id="3474c-113"><dt><strong>PBS_SMOOTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3474c-113"><dt><strong>PBS_SMOOTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3474c-114"><a href="common-control-versions.md">Versione 4,70</a> o successiva.</span><span class="sxs-lookup"><span data-stu-id="3474c-114"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="3474c-115">L'indicatore di stato Visualizza lo stato di avanzamento in una barra di scorrimento uniforme anziché nella barra segmentata predefinita.</span><span class="sxs-lookup"><span data-stu-id="3474c-115">The progress bar displays progress status in a smooth scrolling bar instead of the default segmented bar.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3474c-116">Questo stile è supportato solo nel tema classico di Windows.</span><span class="sxs-lookup"><span data-stu-id="3474c-116">This style is supported only in the Windows Classic theme.</span></span> <span data-ttu-id="3474c-117">Tutti gli altri temi eseguono l'override di questo stile.</span><span class="sxs-lookup"><span data-stu-id="3474c-117">All other themes override this style.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <span data-ttu-id="3474c-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3474c-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3474c-119"><a href="common-control-versions.md">Versione 6,0</a> o successiva e <strong>Windows Vista.</strong></span><span class="sxs-lookup"><span data-stu-id="3474c-119"><a href="common-control-versions.md">Version 6.0</a> or later and <strong>Windows Vista.</strong></span></span> <span data-ttu-id="3474c-120">Determina il comportamento dell'animazione che l'indicatore di stato deve usare quando si esegue lo scorrimento indietro (da un valore più elevato a un valore più basso).</span><span class="sxs-lookup"><span data-stu-id="3474c-120">Determines the animation behavior that the progress bar should use when moving backward (from a higher value to a lower value).</span></span> <span data-ttu-id="3474c-121">Se è impostato, si verificherà &quot; una &quot; transizione uniforme, in caso contrario il controllo passerà &quot; &quot; al valore più basso.</span><span class="sxs-lookup"><span data-stu-id="3474c-121">If this is set, then a &quot;smooth&quot; transition will occur, otherwise the control will &quot;jump&quot; to the lower value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <span data-ttu-id="3474c-122"><dt><strong>PBS_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3474c-122"><dt><strong>PBS_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3474c-123"><a href="common-control-versions.md">Versione 4,70</a> o successiva.</span><span class="sxs-lookup"><span data-stu-id="3474c-123"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="3474c-124">L'indicatore di stato Visualizza lo stato di avanzamento verticalmente, dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="3474c-124">The progress bar displays progress status vertically, from bottom to top.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="3474c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3474c-125">Remarks</span></span>

<span data-ttu-id="3474c-126">È possibile impostare gli stili dell'indicatore di stato, nello stesso modo degli altri controlli comuni, con [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="3474c-126">You can set progress bar styles, in the same way as other common controls, with [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga), or [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="3474c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3474c-127">Requirements</span></span>



| <span data-ttu-id="3474c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3474c-128">Requirement</span></span> | <span data-ttu-id="3474c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3474c-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3474c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3474c-130">Header</span></span><br/> | <dl> <span data-ttu-id="3474c-131"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3474c-131"><dt>CommCtrl.h</dt></span></span> </dl> |



 

