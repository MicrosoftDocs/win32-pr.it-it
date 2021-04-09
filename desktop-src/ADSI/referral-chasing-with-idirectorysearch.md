---
title: Inseguimento dei riferimenti con IDirectorySearch
description: Un riferimento è il meccanismo utilizzato da un server di directory per indirizzare un client a un altro server quando non contiene dati sufficienti sull'oggetto richiesto da una query.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Inseguimento dei riferimenti con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, inseguimento del riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963455"
---
# <a name="referral-chasing-with-idirectorysearch"></a><span data-ttu-id="faca4-105">Inseguimento dei riferimenti con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="faca4-105">Referral Chasing with IDirectorySearch</span></span>

<span data-ttu-id="faca4-106">Un riferimento è il meccanismo utilizzato da un server di directory per indirizzare un client a un altro server quando non contiene dati sufficienti sull'oggetto richiesto da una query.</span><span class="sxs-lookup"><span data-stu-id="faca4-106">A referral is the mechanism that a directory server uses to direct a client to another server when it does not contain sufficient data about the object requested by a query.</span></span>

<span data-ttu-id="faca4-107">In una ricerca a un livello o un sottoalbero, i riferimenti vengono restituiti solo per i contenitori noti, immediatamente subordinati di dominio, schema o configurazione. ovvero domini figlio che sono discendenti diretti.</span><span class="sxs-lookup"><span data-stu-id="faca4-107">In a one-level or subtree search, referrals are returned for known, immediately subordinate domain, schema, or configuration containers only; that is, child domains that are direct descendants.</span></span> <span data-ttu-id="faca4-108">Per altre informazioni, vedere [ambito di ricerca](/windows/desktop/AD/search-scope).</span><span class="sxs-lookup"><span data-stu-id="faca4-108">For more information, see [Search Scope](/windows/desktop/AD/search-scope).</span></span>

<span data-ttu-id="faca4-109">In una directory, non tutti i dati sono disponibili in un singolo server, bensì distribuiti in più server diversi in rete.</span><span class="sxs-lookup"><span data-stu-id="faca4-109">In a directory, not all data is available on a single server, rather, it is distributed over several different servers across the network.</span></span> <span data-ttu-id="faca4-110">Se i server condividono i dati che altri server possono fornire, possono fornire riferimenti a un client quando una query richiesta non può essere risolta nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="faca4-110">If the servers share the data that other servers can provide, they can provide referrals to a client when a requested query cannot be resolved on the originating server.</span></span> <span data-ttu-id="faca4-111">Ad esempio, quando un client chiede al server a di eseguire una query su un oggetto utente (U), un può suggerire che il client continua la ricerca sul server B se U non si trova su un oggetto, ma viene identificato come B. Il client ha la possibilità di proseguire o meno il riferimento.</span><span class="sxs-lookup"><span data-stu-id="faca4-111">For example, when a client asks Server A to query a user object (U), then A can suggest that the client continue the search on Server B if U does not reside on A, but is identified to be on B. The client has the choice to pursue the referral or not.</span></span> <span data-ttu-id="faca4-112">I riferimenti consentono al client di avere una conoscenza precedente della capacità di ogni server, ma il client deve specificare il tipo di riferimenti che un server deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="faca4-112">Referrals free the client from having to possess previous knowledge of the capability of each server, but the client must specify the type of referrals a server should perform.</span></span>

<span data-ttu-id="faca4-113">Per abilitare o disabilitare l'indisponibilità di riferimento, impostare un'opzione di ricerca dei **riferimenti di ADS \_ SEARCHPREF \_ Chase \_** con un valore **\_ Integer ADSTYPE** che contenga uno dei valori di enumerazione per gli [**annunci \_ Chase per \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) i riferimenti di enumerazione nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="faca4-113">To enable or disable referral chasing, set an **ADS\_SEARCHPREF\_CHASE\_REFERRALS** search option with an **ADSTYPE\_INTEGER** value that contains one of the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) enumeration values in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="faca4-114">Nell'esempio di codice seguente viene illustrato come abilitare i riferimenti per Chase.</span><span class="sxs-lookup"><span data-stu-id="faca4-114">The following code example shows how to enable chase referrals.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



<span data-ttu-id="faca4-115">Per ulteriori informazioni sui riferimenti in Active Directory, vedere [riferimenti](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="faca4-115">For more information about referrals in Active Directory, see [Referrals](/windows/desktop/AD/referrals).</span></span>

 

 