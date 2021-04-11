---
description: Tabelle Frequency
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tabelle Frequency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123561"
---
# <a name="frequency-tables"></a><span data-ttu-id="239cc-103">Tabelle Frequency</span><span class="sxs-lookup"><span data-stu-id="239cc-103">Frequency Tables</span></span>

<span data-ttu-id="239cc-104">Il filtro del sintonizzatore TV (kstvtune.ax) include un elenco interno di tabelle di frequenza.</span><span class="sxs-lookup"><span data-stu-id="239cc-104">The TV Tuner filter (kstvtune.ax) has an internal list of frequency tables.</span></span> <span data-ttu-id="239cc-105">Ogni tabella Frequency contiene un elenco di frequenze e corrisponde alle frequenze broadcast o Cable per un determinato paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="239cc-105">Each frequency table contains a list of frequencies, and corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="239cc-106">Un'applicazione viene ottimizzata per una determinata frequenza chiamando il metodo [**IAMTuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) con l'indice della frequenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="239cc-106">An application tunes to a particular frequency by calling the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method with the index of the desired frequency.</span></span>

<span data-ttu-id="239cc-107">Per alcuni paesi o aree geografiche, i numeri di indice delle tabelle di frequenza vengono mappati direttamente ai numeri di canale.</span><span class="sxs-lookup"><span data-stu-id="239cc-107">For some countries/regions, the index numbers of the frequency tables map directly to channel numbers.</span></span> <span data-ttu-id="239cc-108">Tuttavia, i numeri di canale fissi non sono appropriati per tutti i mercati.</span><span class="sxs-lookup"><span data-stu-id="239cc-108">Fixed channel numbers are not appropriate for all markets, however.</span></span> <span data-ttu-id="239cc-109">Ad esempio, i numeri di canale europei non vengono effettivamente utilizzati dai consumer.</span><span class="sxs-lookup"><span data-stu-id="239cc-109">For instance, the European channel numbers are not actually used by consumers.</span></span> <span data-ttu-id="239cc-110">Al contrario, gli utenti si aspettano di scegliere e assegnare i propri numeri di canale per le frequenze usate dagli operatori broadcast o Cable nell'area.</span><span class="sxs-lookup"><span data-stu-id="239cc-110">Instead, consumers expect to choose and assign their own channel numbers for the frequencies that are used by the broadcast or cable operators in their area.</span></span> <span data-ttu-id="239cc-111">Per questi paesi/aree geografiche, le applicazioni non devono esporre i numeri di indice direttamente all'utente.</span><span class="sxs-lookup"><span data-stu-id="239cc-111">For these countries/regions, applications should not expose the index numbers directly to the user.</span></span> <span data-ttu-id="239cc-112">Instread, l'applicazione deve tenere un mapping interno tra i numeri di canale (presentati all'utente) e gli indici di frequenza (per l'ottimizzazione).</span><span class="sxs-lookup"><span data-stu-id="239cc-112">Instread, the application should keep an internal mapping between channel numbers (presented to the user) and frequency indexes (for tuning).</span></span>

<span data-ttu-id="239cc-113">La maggior parte degli operatori di cavi non statunitensi è gratuita per la trasmissione in base alle frequenze scelte, spesso combinando frequenze da standard diversi nella stessa linea di canali.</span><span class="sxs-lookup"><span data-stu-id="239cc-113">Most non-US cable operators are free to broadcast on frequencies of their choosing, often mixing frequencies from different standards into the same channel lineup.</span></span> <span data-ttu-id="239cc-114">Viene quindi usata una tabella con frequenza "Unicable" per qualsiasi paese/area geografica priva di standard Cable Channel standard Authority.</span><span class="sxs-lookup"><span data-stu-id="239cc-114">Therefore, a "Unicable" frequency table is used for any country/region that lacks a standard cable channel standards authority.</span></span> <span data-ttu-id="239cc-115">Viene inoltre fornito un meccanismo per eseguire l'override delle singole frequenze nelle tabelle di frequenza.</span><span class="sxs-lookup"><span data-stu-id="239cc-115">Also, a mechanism is provided to override individual frequencies in the frequency tables.</span></span> <span data-ttu-id="239cc-116">Questo meccanismo è descritto nella sezione seguente, [sostituzioni di frequenza](frequency-overrides.md).</span><span class="sxs-lookup"><span data-stu-id="239cc-116">This mechanism is described in the following section, [Frequency Overrides](frequency-overrides.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="239cc-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="239cc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="239cc-118">Ottimizzazione della TV analoga internazionale</span><span class="sxs-lookup"><span data-stu-id="239cc-118">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



