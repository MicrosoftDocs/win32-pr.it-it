---
title: Limite di tempo del server con IDirectorySearch
description: Per evitare di usare tutto il tempo della CPU e impedire l'esecuzione di altre operazioni, specificare il limite di tempo di ricerca per un valore ridotto, quindi eseguire di nuovo l'applicazione in un secondo momento se non riesce a generare il report.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Limite di tempo del server con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, limite di tempo del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955082"
---
# <a name="server-time-limit-with-idirectorysearch"></a><span data-ttu-id="03e26-105">Limite di tempo del server con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="03e26-105">Server Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="03e26-106">Quando si richiede una ricerca in un server occupato, potrebbe essere necessario richiedere che il server limiti la ricerca a un limite di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="03e26-106">When you request a search on a busy server, you may want to request that the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="03e26-107">Si consiglia, ad esempio, di eseguire un'applicazione per generare un report settimanale in un server in cui è in esecuzione quasi la sua capacità.</span><span class="sxs-lookup"><span data-stu-id="03e26-107">For example, you want to run an application to generate a weekly report on a server that is running near its capacity.</span></span> <span data-ttu-id="03e26-108">Per evitare di usare tutto il tempo della CPU e impedire l'esecuzione di altre operazioni, specificare il limite di tempo di ricerca per un valore ridotto, quindi eseguire di nuovo l'applicazione in un secondo momento se non riesce a generare il report.</span><span class="sxs-lookup"><span data-stu-id="03e26-108">To avoid using all the CPU time and preventing other operations from running, specify the search time limit to a small value and then rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="03e26-109">Alcuni server potrebbero imporre un limite di tempo amministrativo.</span><span class="sxs-lookup"><span data-stu-id="03e26-109">Some servers might impose their own administrative time limit.</span></span> <span data-ttu-id="03e26-110">In questi casi, se si specifica un valore per il limite di tempo di ricerca superiore al limite di tempo amministrativo, il server ignorerà la specifica e utilizzerà il relativo valore limite di tempo interno.</span><span class="sxs-lookup"><span data-stu-id="03e26-110">In these cases, if you specify a search time limit value greater than the administrative time limit, the server will ignore your specification and use its internal time limit value instead.</span></span>

<span data-ttu-id="03e26-111">Il valore predefinito per il limite di tempo del server non è limite.</span><span class="sxs-lookup"><span data-stu-id="03e26-111">The default for the server time limit is no limit.</span></span> <span data-ttu-id="03e26-112">Per impostare un limite di tempo per il server, impostare un'opzione di ricerca **Ads \_ SEARCHPREF \_ tempo \_ limite** con un valore **\_ Integer ADSTYPE** che contenga il limite di tempo del server, in secondi, nella matrice di [**\_ \_ informazioni SEARCHPREF degli annunci**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="03e26-112">To set a server time limit, set an **ADS\_SEARCHPREF\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the server time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="03e26-113">Questa operazione è illustrata nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="03e26-113">This operation is shown in the following code example.</span></span> <span data-ttu-id="03e26-114">Un limite di tempo del server pari a zero indica nessun limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="03e26-114">A server time limit of zero indicates no time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




