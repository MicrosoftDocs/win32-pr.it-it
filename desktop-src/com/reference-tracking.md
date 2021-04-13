---
title: Rilevamento riferimenti
description: Rilevamento riferimenti
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474310"
---
# <a name="reference-tracking"></a><span data-ttu-id="7d930-103">Rilevamento riferimenti</span><span class="sxs-lookup"><span data-stu-id="7d930-103">Reference Tracking</span></span>

<span data-ttu-id="7d930-104">Il rilevamento dei riferimenti può impedire la versione iniziale non intenzionale o dannosa di oggetti.</span><span class="sxs-lookup"><span data-stu-id="7d930-104">Reference tracking can prevent the unintentional or malicious early release of objects.</span></span>

<span data-ttu-id="7d930-105">Quando si Abilita il rilevamento dei riferimenti, si richiede che le chiamate [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribuite vengano autenticate da com.</span><span class="sxs-lookup"><span data-stu-id="7d930-105">When you enable reference tracking, you are requesting that distributed [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls be authenticated by COM.</span></span> <span data-ttu-id="7d930-106">Quando è abilitata la verifica dei riferimenti, COM tiene traccia dei conteggi dei riferimenti per ogni utente, in modo che un utente possa chiamare la **versione** solo sugli oggetti che l'utente ha precedentemente chiamato **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="7d930-106">When reference tracking is enabled, COM keeps track of per-user reference counts so that a user can call **Release** only on objects that the user previously called **AddRef** on.</span></span> <span data-ttu-id="7d930-107">Sebbene il rilevamento dei riferimenti possa ridurre le prestazioni, garantisce che, indipendentemente dal numero di volte in cui un determinato utente chiama il **rilascio**, gli oggetti e gli stub continueranno a esistere se qualcun altro ha un riferimento.</span><span class="sxs-lookup"><span data-stu-id="7d930-107">Although reference tracking can decrease performance, it ensures that no matter how many times a given user calls **Release**, the objects and stubs will still exist if someone else has a reference to them.</span></span>

<span data-ttu-id="7d930-108">Il client può impostare il rilevamento dei riferimenti per un processo passando il \_ flag EOAC Secure \_ refs Capability in una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="7d930-108">The client can set reference tracking for a process by passing the EOAC\_SECURE\_REFS capability flag in a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="7d930-109">È inoltre possibile abilitare o disabilitare il rilevamento dei riferimenti per tutte le applicazioni in un computer utilizzando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="7d930-109">You can also enable or disable reference tracking for all applications on a computer by using Dcomcnfg.exe.</span></span>

<span data-ttu-id="7d930-110">Se la verifica dei riferimenti è abilitata, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) utilizza sempre le impostazioni di sicurezza predefinite.</span><span class="sxs-lookup"><span data-stu-id="7d930-110">If reference tracking is enabled, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) always uses default security settings.</span></span> <span data-ttu-id="7d930-111">In questo caso, le chiamate a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) su **IUnknown** avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7d930-111">In this case, calls to [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) on **IUnknown** will fail.</span></span>

 

 