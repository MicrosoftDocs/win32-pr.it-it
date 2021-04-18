---
title: Modifiche al supporto hardware legacy di DX9
description: Modifiche al supporto hardware legacy di DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300574"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a><span data-ttu-id="010da-103">Modifiche al supporto hardware legacy di DX9</span><span class="sxs-lookup"><span data-stu-id="010da-103">Changes in DX9 legacy hardware support</span></span>

## <a name="platform"></a><span data-ttu-id="010da-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="010da-104">Platform</span></span>

<span data-ttu-id="010da-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="010da-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="010da-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="010da-106">Description</span></span>

<span data-ttu-id="010da-107">Intel e AMD/ATI non supportano più le parti grafiche DX9 e non aggiorneranno i driver per questi dispositivi per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="010da-107">Intel and AMD/ATI no longer support their DX9 graphics parts and will not be updating drivers for these devices for Windows 8.</span></span> <span data-ttu-id="010da-108">Inoltre, questi dispositivi non sono inclusi in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="010da-108">Furthermore, these devices are not covered in-box for Windows 8.</span></span> <span data-ttu-id="010da-109">Gli ultimi driver per questi dispositivi sono quelli disponibili in WU e nei siti Web OEM/IHV. molti dati di vista e molti di questi driver di versione finale presentano problemi in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="010da-109">The last drivers for these devices are those available on WU and on the OEM/IHV’s websites; many date from Vista, and many of these final version drivers exhibit problems on Windows 8.</span></span> <span data-ttu-id="010da-110">Inoltre, nVidia ha recentemente dichiarato di non supportare le parti di DX9 (vista e precedente) per dispositivi mobili (notebook) per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="010da-110">In addition, nVidia has recently stated that they will not support their DX9 (Vista and older) mobile (notebook) parts for Windows 8.</span></span> <span data-ttu-id="010da-111">Continuano a supportare le parti DX9 del desktop.</span><span class="sxs-lookup"><span data-stu-id="010da-111">They continue to support their desktop DX9 parts.</span></span>

<span data-ttu-id="010da-112">Tutte queste combinazioni di driver/parti si trovano nell'elenco di fallback software di Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="010da-112">All of these driver/part combinations are on the Internet Explorer 9 software fallback list.</span></span> <span data-ttu-id="010da-113">Ciò significa che, per motivi di prestazioni o di stabilità, Internet Explorer 9 utilizza il rendering del software su questi dispositivi.</span><span class="sxs-lookup"><span data-stu-id="010da-113">This means that for either performance or stability reasons, Internet Explorer 9 uses software rendering on these devices.</span></span> <span data-ttu-id="010da-114">Questo è un buon indizio che l'esperienza con le app di Windows Store non sarà soddisfacente su questi driver e parti.</span><span class="sxs-lookup"><span data-stu-id="010da-114">This is a good indication that the experience with Windows Store apps will not be satisfactory on these drivers and parts.</span></span>

## <a name="manifestation"></a><span data-ttu-id="010da-115">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="010da-115">Manifestation</span></span>

<span data-ttu-id="010da-116">Poiché non è disponibile alcun supporto per questi dispositivi, molti utenti con queste parti si troveranno in esecuzione sul driver di visualizzazione di base di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="010da-116">As there is no in-box support for these devices, many users with these parts will wind up running on the Microsoft Basic Display Driver.</span></span> <span data-ttu-id="010da-117">Si tratta di una GPU software WDDM 1,2 basata su DISTORSIONe ed è effettivamente più veloce di alcune delle parti di questa classe, ad esempio la serie Intel GMA500.</span><span class="sxs-lookup"><span data-stu-id="010da-117">This is a WARP-based WDDM 1.2 software GPU, and is actually faster than some of the parts in this class, for example, the Intel GMA500 series).</span></span> <span data-ttu-id="010da-118">Supporta Aero-Glass e DWM ed è in grado di eseguire app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="010da-118">It supports aero-glass and DWM, and can run Windows Store apps.</span></span>

<span data-ttu-id="010da-119">Tuttavia, presenta alcune limitazioni importanti:</span><span class="sxs-lookup"><span data-stu-id="010da-119">However, it has some important limitations:</span></span>

-   <span data-ttu-id="010da-120">Non supporta più monitor o proiezione</span><span class="sxs-lookup"><span data-stu-id="010da-120">It doesn’t support multiple monitors or projection</span></span>
-   <span data-ttu-id="010da-121">Non supporta la sospensione, sebbene supporti la sospensione</span><span class="sxs-lookup"><span data-stu-id="010da-121">It doesn’t support sleep, though it does support hibernation</span></span>
-   <span data-ttu-id="010da-122">Spesso non è possibile modificare la risoluzione dello schermo</span><span class="sxs-lookup"><span data-stu-id="010da-122">It often will not allow changing screen resolution</span></span>

## <a name="mitigation"></a><span data-ttu-id="010da-123">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="010da-123">Mitigation</span></span>

<span data-ttu-id="010da-124">Se dopo il test si scopre che l'esperienza utente non è accettabile, è possibile scegliere di impostare i requisiti hardware per i propri prodotti che escludono le parti Intel e AMD DX9 precedenti.</span><span class="sxs-lookup"><span data-stu-id="010da-124">If after testing, you find that the user experience is not acceptable, you may choose to set hardware requirements for their products that exclude these older DX9 Intel and AMD parts.</span></span> <span data-ttu-id="010da-125">Si può anche scegliere di avvisare i clienti che potrebbero avere un'esperienza inaccettabile su queste parti.</span><span class="sxs-lookup"><span data-stu-id="010da-125">You may also choose to alert your customers that they may have an unacceptable experience on these parts.</span></span>

## <a name="tests"></a><span data-ttu-id="010da-126">Test</span><span class="sxs-lookup"><span data-stu-id="010da-126">Tests</span></span>

<span data-ttu-id="010da-127">Valutare le prestazioni e l'esperienza su questi dispositivi:</span><span class="sxs-lookup"><span data-stu-id="010da-127">Evaluate the performance and experience on these devices:</span></span>

-   <span data-ttu-id="010da-128">Qual è l'esperienza della versione del driver finale disponibile?</span><span class="sxs-lookup"><span data-stu-id="010da-128">What is the experience like on the final driver version available?</span></span>
-   <span data-ttu-id="010da-129">Qual è l'esperienza di MSBDD?</span><span class="sxs-lookup"><span data-stu-id="010da-129">What is the experience like on the MSBDD?</span></span>

 

 




