---
title: WM/WMADRCAverageReference
description: L'attributo WM/WMADRCAverageReference contiene il livello di volume medio del file come codificato.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Formato di Windows Media WM/WMADRCAverageReference
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299207"
---
# <a name="wmwmadrcaveragereference"></a><span data-ttu-id="0e1ef-104">WM/WMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="0e1ef-104">WM/WMADRCAverageReference</span></span>

<span data-ttu-id="0e1ef-105">L'attributo **WM/WMADRCAverageReference** contiene il livello di volume medio del file come codificato.</span><span class="sxs-lookup"><span data-stu-id="0e1ef-105">The **WM/WMADRCAverageReference** attribute contains the average volume level of the file as encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0e1ef-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="0e1ef-106">Global Constant</span></span>

<span data-ttu-id="0e1ef-107">g \_ wszWMWMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="0e1ef-107">g\_wszWMWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="0e1ef-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0e1ef-108">Data Type</span></span>

<span data-ttu-id="0e1ef-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0e1ef-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0e1ef-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e1ef-110">Remarks</span></span>

<span data-ttu-id="0e1ef-111">Sono disponibili quattro attributi usati da Windows Media Player per il controllo dinamico degli intervalli: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="0e1ef-111">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="0e1ef-112">Tutti questi valori vengono impostati dal writer in base alle informazioni provenienti dal codec durante la scrittura di flussi con il codec Windows Media Audio 9 o il codec Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="0e1ef-112">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="0e1ef-113">I valori medi sono impostati sul livello medio del volume del flusso e i valori di picco sono impostati sul livello di volume massimo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="0e1ef-113">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="0e1ef-114">I valori di riferimento sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0e1ef-114">The reference values are read-only.</span></span> <span data-ttu-id="0e1ef-115">I valori di destinazione vengono impostati da Windows Media Player quando viene riprodotto il file per registrare le preferenze di controllo dell'intervallo dinamico dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0e1ef-115">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e1ef-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e1ef-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e1ef-117">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="0e1ef-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="0e1ef-118">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="0e1ef-118">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="0e1ef-119">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="0e1ef-119">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="0e1ef-120">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="0e1ef-120">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




