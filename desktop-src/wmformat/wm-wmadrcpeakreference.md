---
title: WM/WMADRCPeakReference
description: L'attributo WM/WMADRCPeakReference contiene il livello di volume massimo del file codificato. Questo valore viene utilizzato da Windows Media Player per il controllo dinamico degli intervalli. Questo valore viene impostato dal codec ed è di sola lettura.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- Formato di Windows Media WM/WMADRCPeakReference
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397794"
---
# <a name="wmwmadrcpeakreference"></a><span data-ttu-id="ee7c7-106">WM/WMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="ee7c7-106">WM/WMADRCPeakReference</span></span>

<span data-ttu-id="ee7c7-107">L'attributo **WM/WMADRCPeakReference** contiene il livello di volume massimo del file codificato.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-107">The **WM/WMADRCPeakReference** attribute contains the maximum volume level of the file as encoded.</span></span> <span data-ttu-id="ee7c7-108">Questo valore viene utilizzato da Windows Media Player per il controllo dinamico degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-108">This value is used by Windows Media Player for dynamic range control.</span></span> <span data-ttu-id="ee7c7-109">Questo valore viene impostato dal codec ed è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-109">This value is set by the codec and is read-only.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ee7c7-110">Costante globale</span><span class="sxs-lookup"><span data-stu-id="ee7c7-110">Global Constant</span></span>

<span data-ttu-id="ee7c7-111">g \_ wszWMWMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="ee7c7-111">g\_wszWMWMADRCPeakReference</span></span>

## <a name="data-type"></a><span data-ttu-id="ee7c7-112">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ee7c7-112">Data Type</span></span>

<span data-ttu-id="ee7c7-113">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ee7c7-113">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="ee7c7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee7c7-114">Remarks</span></span>

<span data-ttu-id="ee7c7-115">Sono disponibili quattro attributi usati da Windows Media Player per il controllo dinamico degli intervalli: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-115">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="ee7c7-116">Tutti questi valori vengono impostati dal writer in base alle informazioni provenienti dal codec durante la scrittura di flussi con il codec Windows Media Audio 9 o il codec Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-116">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="ee7c7-117">I valori medi sono impostati sul livello medio del volume del flusso e i valori di picco sono impostati sul livello di volume massimo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-117">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="ee7c7-118">I valori di riferimento sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-118">The reference values are read-only.</span></span> <span data-ttu-id="ee7c7-119">I valori di destinazione vengono impostati da Windows Media Player quando viene riprodotto il file per registrare le preferenze di controllo dell'intervallo dinamico dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ee7c7-119">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee7c7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee7c7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7c7-121">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="ee7c7-121">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="ee7c7-122">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="ee7c7-122">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="ee7c7-123">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="ee7c7-123">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="ee7c7-124">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="ee7c7-124">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




