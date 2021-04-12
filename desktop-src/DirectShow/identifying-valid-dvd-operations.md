---
description: Identificazione di operazioni DVD valide
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificazione di operazioni DVD valide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401283"
---
# <a name="identifying-valid-dvd-operations"></a><span data-ttu-id="eb531-103">Identificazione di operazioni DVD valide</span><span class="sxs-lookup"><span data-stu-id="eb531-103">Identifying Valid DVD Operations</span></span>

<span data-ttu-id="eb531-104">Diversi fattori determinano se è possibile eseguire un'operazione DVD specifica:</span><span class="sxs-lookup"><span data-stu-id="eb531-104">Several factors determine whether you can perform a given DVD operation:</span></span>

-   <span data-ttu-id="eb531-105">Dominio corrente.</span><span class="sxs-lookup"><span data-stu-id="eb531-105">The current domain.</span></span> <span data-ttu-id="eb531-106">Alcuni comandi sono validi solo in alcuni domini.</span><span class="sxs-lookup"><span data-stu-id="eb531-106">Some commands are only valid in certain domains.</span></span> <span data-ttu-id="eb531-107">Quando il dominio viene modificato, lo strumento di spostamento Invia un \_ evento di modifica del dominio DVD EC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="eb531-107">When the domain changes, the navigator sends an EC\_DVD\_DOMAIN\_CHANGE event.</span></span> <span data-ttu-id="eb531-108">È anche possibile chiamare [**IDvdInfo2:: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) per ottenere il dominio corrente.</span><span class="sxs-lookup"><span data-stu-id="eb531-108">You can also call [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) to get the current domain.</span></span>
-   <span data-ttu-id="eb531-109">Flag UOPS.</span><span class="sxs-lookup"><span data-stu-id="eb531-109">UOPS flags.</span></span> <span data-ttu-id="eb531-110">Si tratta di flag scritti sul disco che indicano quali operazioni sono consentite.</span><span class="sxs-lookup"><span data-stu-id="eb531-110">These are flags written onto the disc that indicate which operations are permitted.</span></span> <span data-ttu-id="eb531-111">Ogni volta che i flag cambiano, lo strumento di spostamento Invia un \_ \_ \_ evento di modifica UOPs valido del DVD EC \_ con i nuovi flag.</span><span class="sxs-lookup"><span data-stu-id="eb531-111">Whenever the flags change, the navigator sends a EC\_DVD\_VALID\_UOPS\_CHANGE event with the new flags.</span></span> <span data-ttu-id="eb531-112">È anche possibile chiamare [**IDvdInfo2:: GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) per ottenere i flag UOPs correnti.</span><span class="sxs-lookup"><span data-stu-id="eb531-112">You can also call [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) to get the current UOPS flags.</span></span>
-   <span data-ttu-id="eb531-113">Contenuto DVD.</span><span class="sxs-lookup"><span data-stu-id="eb531-113">DVD content.</span></span> <span data-ttu-id="eb531-114">Alcuni comandi potrebbero non essere rilevanti in base al contenuto del DVD.</span><span class="sxs-lookup"><span data-stu-id="eb531-114">Some commands may not be relevant based on the content of the DVD.</span></span> <span data-ttu-id="eb531-115">Ad esempio, il metodo [**IDVDControl2:: SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) può essere consentito in base ai flag Domain e UOPs correnti, ma il video potrebbe avere solo un angolo.</span><span class="sxs-lookup"><span data-stu-id="eb531-115">For example, the [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) method might be permitted according to the current domain and UOPS flags, yet the video might have only one angle.</span></span> <span data-ttu-id="eb531-116">In tal caso, la chiamata **SelectAngle** è consentita ma non è un'opzione significativa.</span><span class="sxs-lookup"><span data-stu-id="eb531-116">In that case, the **SelectAngle** call is permitted but is not a meaningful option.</span></span>

<span data-ttu-id="eb531-117">In caso di dubbio, consentire un'azione.</span><span class="sxs-lookup"><span data-stu-id="eb531-117">When in doubt, permit an action.</span></span> <span data-ttu-id="eb531-118">Nel peggiore dei casi, il metodo [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) avrà esito negativo ed è possibile inviare commenti e suggerimenti all'utente.</span><span class="sxs-lookup"><span data-stu-id="eb531-118">At worst, the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method will fail and you can give feedback to the user.</span></span> <span data-ttu-id="eb531-119">Il feedback dovrebbe essere relativamente discreto.</span><span class="sxs-lookup"><span data-stu-id="eb531-119">The feedback should be relatively unobtrusive.</span></span> <span data-ttu-id="eb531-120">Ad esempio, è possibile che si lampeggi una piccola X rossa per avvisare l'utente.</span><span class="sxs-lookup"><span data-stu-id="eb531-120">For example, you might flash a small red X to alert the user.</span></span> <span data-ttu-id="eb531-121">Il navigatore DVD restituisce VFW \_ e \_ DVD \_ INVALIDDOMAIN quando il dominio vieta un'operazione e l' \_ operazione VFW e DVD viene \_ \_ \_ inibita quando i flag UOPs proibiscono un'operazione.</span><span class="sxs-lookup"><span data-stu-id="eb531-121">The DVD Navigator returns VFW\_E\_DVD\_INVALIDDOMAIN when the domain prohibits an operation, and VFW\_E\_DVD\_OPERATION\_INHIBITED when the UOPS flags prohibit an operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb531-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb531-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb531-123">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="eb531-123">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



