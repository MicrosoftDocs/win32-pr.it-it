---
title: WM/WMADRCAverageTarget
description: L'attributo WM/WMADRCAverageTarget contiene il livello di volume medio richiesto dall'utente. Questo valore viene utilizzato da Windows Media Player per il controllo dinamico degli intervalli.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Formato di Windows Media WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299205"
---
# <a name="wmwmadrcaveragetarget"></a><span data-ttu-id="081a9-105">WM/WMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="081a9-105">WM/WMADRCAverageTarget</span></span>

<span data-ttu-id="081a9-106">L'attributo **WM/WMADRCAverageTarget** contiene il livello di volume medio richiesto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="081a9-106">The **WM/WMADRCAverageTarget** attribute contains the average volume level requested by the user.</span></span> <span data-ttu-id="081a9-107">Questo valore viene utilizzato da Windows Media Player per il controllo dinamico degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="081a9-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="081a9-108">Costante globale</span><span class="sxs-lookup"><span data-stu-id="081a9-108">Global Constant</span></span>

<span data-ttu-id="081a9-109">g \_ wszWMWMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="081a9-109">g\_wszWMWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="081a9-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="081a9-110">Data Type</span></span>

<span data-ttu-id="081a9-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="081a9-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="081a9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="081a9-112">Remarks</span></span>

<span data-ttu-id="081a9-113">Sono disponibili quattro attributi usati da Windows Media Player per il controllo dinamico degli intervalli: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="081a9-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="081a9-114">Tutti questi valori vengono impostati dal writer in base alle informazioni provenienti dal codec durante la scrittura di flussi con il codec Windows Media Audio 9 o il codec Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="081a9-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="081a9-115">I valori medi sono impostati sul livello medio del volume del flusso e i valori di picco sono impostati sul livello di volume massimo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="081a9-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="081a9-116">I valori di riferimento sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="081a9-116">The reference values are read-only.</span></span> <span data-ttu-id="081a9-117">I valori di destinazione vengono impostati da Windows Media Player quando viene riprodotto il file per registrare le preferenze di controllo dell'intervallo dinamico dell'utente.</span><span class="sxs-lookup"><span data-stu-id="081a9-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="081a9-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="081a9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="081a9-119">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="081a9-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="081a9-120">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="081a9-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="081a9-121">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="081a9-121">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="081a9-122">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="081a9-122">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




