---
description: Una rete viene visualizzata come meccanismo di trasporto che trasmette i dati da un punto a un altro.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485316"
---
# <a name="network"></a><span data-ttu-id="0e0ef-103">Rete</span><span class="sxs-lookup"><span data-stu-id="0e0ef-103">Network</span></span>

<span data-ttu-id="0e0ef-104">Una rete viene visualizzata come meccanismo di trasporto che trasmette i dati da un punto a un altro.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-104">A network is viewed as the transport mechanism that conveys data from one point to another.</span></span> <span data-ttu-id="0e0ef-105">I provider di servizi TAPI gestiscono i protocolli specifici necessari per eseguire operazioni quali la creazione di una sessione di comunicazione in una determinata rete.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-105">TAPI service providers handle the specific protocols required to perform operations such as establishing a communications session on a given network.</span></span> <span data-ttu-id="0e0ef-106">Un'applicazione server o un utente finale richiede in genere solo informazioni di rete molto generali, ad esempio il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-106">An end-user or server application normally requires only very general network information, such as address type.</span></span>

<span data-ttu-id="0e0ef-107">Alcuni tipi comuni di reti:</span><span class="sxs-lookup"><span data-stu-id="0e0ef-107">Some common types of networks:</span></span>

-   <span data-ttu-id="0e0ef-108">**Pot (servizio telefonico Plain Old):** La voce e i dati vengono trasmessi in formato analogico durante il *ciclo locale* e vengono trasmessi digitalmente altrove.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-108">**POTS (Plain Old Telephone Service):** Voice and data are transmitted in analog format while in the *local loop* and are digitally transmitted elsewhere.</span></span> <span data-ttu-id="0e0ef-109">In genere, un tipo di supporto per chiamata, un canale per riga.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-109">Typically, one media type per call, one channel per line.</span></span>
-   <span data-ttu-id="0e0ef-110">**ISDN (Integrated Services Digital Network):** Trasmesse digitalmente.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-110">**ISDN (Integrated Services Digital Network):** Transmitted digitally.</span></span> <span data-ttu-id="0e0ef-111">Velocità fino a 128 kbps nelle righe Basic Rate Interface (BRI-ISDN) e molto più elevate sulle linee PRI-ISDN (Primary Rate Interface).</span><span class="sxs-lookup"><span data-stu-id="0e0ef-111">Speeds of up to 128 Kbps on Basic Rate Interface (BRI-ISDN) lines and much higher on Primary Rate Interface (PRI-ISDN) lines.</span></span> <span data-ttu-id="0e0ef-112">Almeno tre canali e un massimo di 32 canali, per la trasmissione simultanea e gestita in modo indipendente di voce e dati.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-112">At least three channels and as many as 32 channels, for simultaneous, independently operated transmission of voice and data.</span></span> <span data-ttu-id="0e0ef-113">Standard internazionale.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-113">International standard.</span></span>
-   <span data-ttu-id="0e0ef-114">**T1/E1:** Trasmesse digitalmente.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-114">**T1/E1:** Transmitted digitally.</span></span> <span data-ttu-id="0e0ef-115">T1 è un collegamento di trasmissione con una capacità di 1,544 Mbps, in genere usato per connettere le reti tra le distanze remote.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-115">T1 is a transmission link with a capacity of 1.544 Mbps, typically used for connecting networks across remote distances.</span></span> <span data-ttu-id="0e0ef-116">Nell'Unione europea T1 viene chiamato E1.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-116">In the European Union T1 is called E1.</span></span>
-   <span data-ttu-id="0e0ef-117">**Switched 56:** Segnalazione a 56 Kbps tramite linee telefoniche remote, ma richiede apparecchiature speciali.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-117">**Switched 56:** Signaling at 56 Kbps over dial-up telephone lines, but requires special equipment.</span></span> <span data-ttu-id="0e0ef-118">Limitato alle chiamate ad altre strutture appositamente fornite.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-118">Limited to calls to other specially equipped facilities.</span></span>
-   <span data-ttu-id="0e0ef-119">**Centrex:** Servizi di rete centralizzati tramite linee telefoniche normali e l'uso di apparecchiature aziendali telefoniche.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-119">**CENTREX:** Centralized network services through regular telephone lines and using telephone company equipment.</span></span> <span data-ttu-id="0e0ef-120">Non è necessaria alcuna attrezzatura speciale.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-120">No special equipment required.</span></span>
-   <span data-ttu-id="0e0ef-121">**PBX digitali (scambi di rami privati) e sistemi principali:** Voce e dati trasmessi su sistemi telefonici privati mediante interfacce proprietarie.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-121">**Digital PBXs (private branch exchanges) and key systems:** Voice and data transmitted on private telephone systems using proprietary interfaces.</span></span>
-   <span data-ttu-id="0e0ef-122">**Reti IP:** Voce e dati trasmessi nelle reti tramite il protocollo IP (Internet Protocol), ad esempio Internet stesso o una rete Intranet aziendale.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-122">**IP Networks:** Voice and data transmitted on networks using the Internet Protocol (IP), such as the Internet itself or a corporate intranet.</span></span>

<span data-ttu-id="0e0ef-123">Tenere presente che non si tratta di un elenco completo.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-123">Please note that this list is not exhaustive.</span></span> <span data-ttu-id="0e0ef-124">È possibile supportare qualsiasi meccanismo di trasporto di rete, dato che i provider di servizi appropriati.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-124">Any network transport mechanism can be supported, given appropriate service providers.</span></span>

 

 



