---
title: Disponibilità dei driver grafici applicabili in Windows Update
description: La disponibilità di questi driver in Windows Update (WU) determinerà se a un utente viene automaticamente offerto un aggiornamento da Windows 7, Windows 8 o Windows 8.1 a Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298105"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a><span data-ttu-id="84719-103">Disponibilità dei driver grafici applicabili in Windows Update</span><span class="sxs-lookup"><span data-stu-id="84719-103">Availability of applicable graphics drivers on Windows Update</span></span>

<span data-ttu-id="84719-104">La disponibilità di questi driver in Windows Update (WU) determinerà se a un utente viene automaticamente offerto un aggiornamento da Windows 7, Windows 8 o Windows 8.1 a Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84719-104">The availability of these drivers on Windows Update (WU) will determine whether a user is automatically offered an upgrade from Windows 7, Windows 8 or Windows 8.1 to Windows 10.</span></span> <span data-ttu-id="84719-105">Se le analisi hardware hanno mostrato che non è disponibile alcun driver grafico in Windows Update per la scheda grafica del PC, agli utenti non è stato offerto il sistema operativo Windows 10 aggiornato.</span><span class="sxs-lookup"><span data-stu-id="84719-105">If hardware scans showed that there was no graphics driver available on Windows Update for the graphics adapter in the PC, users were not offered the updated Windows 10 OS.</span></span> <span data-ttu-id="84719-106">Tuttavia, gli utenti possono comunque ottenere Windows 10 attraverso altre origini ed eseguire manualmente l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="84719-106">However, users can still obtain Windows 10 through other sources and manually perform the upgrade.</span></span>

<span data-ttu-id="84719-107">Alcuni utenti non erano certi del motivo per cui l'aggiornamento non veniva offerto quando altre persone erano, anche se in preparazione aggiornamento è stato spiegato che non era disponibile alcun driver grafico per l'hardware.</span><span class="sxs-lookup"><span data-stu-id="84719-107">Some users were unsure of why they were not offered the upgrade when other people were, even though the Upgrade Advisor explained that there was no graphics driver available for their hardware.</span></span>

<span data-ttu-id="84719-108">Inoltre, alcuni utenti hanno forzato un aggiornamento e hanno quindi scoperto che la loro funzionalità grafica e le prestazioni sono state rilevate a causa della mancanza di un driver hardware.</span><span class="sxs-lookup"><span data-stu-id="84719-108">Additionally, some users forced an upgrade and then found that their graphics functionality and performance suffered due to the lack of a hardware driver.</span></span>

## <a name="mitigations"></a><span data-ttu-id="84719-109">Soluzioni di prevenzione</span><span class="sxs-lookup"><span data-stu-id="84719-109">Mitigations</span></span>

<span data-ttu-id="84719-110">Per attenuare questo problema, gli utenti possono installare manualmente un driver precedente, ad esempio Windows 7, Windows 8 o Windows 8.1, accedendo al sito Web IHV o OEM e scaricando un driver in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="84719-110">To mitigate this, users can manually install an older driver, i.e. from Windows 7, Windows 8 or Windows 8.1, by going to the IHV or OEM web site and downloading a driver explicitly.</span></span> <span data-ttu-id="84719-111">Questa operazione deve essere eseguita dopo l'aggiornamento e non è garantita.</span><span class="sxs-lookup"><span data-stu-id="84719-111">This must be done after the upgrade and is not guaranteed to work.</span></span> <span data-ttu-id="84719-112">Non esiste alcuna soluzione supportata se un driver di grafica appropriato non è disponibile in WU.</span><span class="sxs-lookup"><span data-stu-id="84719-112">There is no supported solution if a suitable graphics driver is not available on WU.</span></span> <span data-ttu-id="84719-113">L'utente deve decidere se:</span><span class="sxs-lookup"><span data-stu-id="84719-113">The user must decide whether to:</span></span>

-   <span data-ttu-id="84719-114">Rimanere nel sistema operativo precedente;</span><span class="sxs-lookup"><span data-stu-id="84719-114">Remain on the previous OS;</span></span>
-   <span data-ttu-id="84719-115">Accettare le limitazioni del driver software, Microsoft Basic Display Adapter (MSBDA); o</span><span class="sxs-lookup"><span data-stu-id="84719-115">Accept the limitations of the software driver, Microsoft Basic Display Adapter (MSBDA); or</span></span>
-   <span data-ttu-id="84719-116">Acquistare una nuova scheda grafica con un driver Windows 10 supportato.</span><span class="sxs-lookup"><span data-stu-id="84719-116">Buy a new graphics card that has a supported Windows 10 driver.</span></span>

## <a name="solutions"></a><span data-ttu-id="84719-117">Soluzioni</span><span class="sxs-lookup"><span data-stu-id="84719-117">Solutions</span></span>

<span data-ttu-id="84719-118">È fondamentale che IHV e gli OEM carichino i driver grafici Windows 10 in WU per qualsiasi hardware che intende supportare.</span><span class="sxs-lookup"><span data-stu-id="84719-118">It’s critical that IHVs and OEMs upload their Windows 10 graphics drivers to WU for any hardware that they intend to support.</span></span>

<span data-ttu-id="84719-119">Si noti che l'hardware che ha raggiunto la fine del Live (EOL) potrebbe non avere driver in WU.</span><span class="sxs-lookup"><span data-stu-id="84719-119">Note that hardware that has reached End-Of-Live (EOL) might not have drivers on WU.</span></span> <span data-ttu-id="84719-120">In questo caso non esiste alcuna soluzione: l'utente deve scegliere una delle opzioni in mitigazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="84719-120">There is no solution in this case – the user must choose one of the options under Mitigations above.</span></span>

 

 




