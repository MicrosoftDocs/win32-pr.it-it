---
title: Scelta di un livello di autenticazione
description: Quando si sceglie un livello di autenticazione, attenersi alle linee guida seguenti.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471150"
---
# <a name="choosing-an-authentication-level"></a><span data-ttu-id="a4124-103">Scelta di un livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="a4124-103">Choosing an Authentication Level</span></span>

<span data-ttu-id="a4124-104">Quando si sceglie un livello di autenticazione, attenersi alle linee guida seguenti.</span><span class="sxs-lookup"><span data-stu-id="a4124-104">When choosing an authentication level, use the following guideline.</span></span> <span data-ttu-id="a4124-105">Se non è rilevante se i dati inviati possono essere intercettati e modificati e i dati ricevuti possono essere intercettati o modificati, utilizzare \_ il livello di autenticazione di RPC C \_ \_ \_ None, che è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4124-105">If it does not matter whether the data being sent can be intercepted and modified, and the data received can be intercepted or modified, use RPC\_C\_AUTHN\_LEVEL\_NONE, which is the default.</span></span> <span data-ttu-id="a4124-106">Se i dati non devono essere modificati e i dati privati non vengono inviati né ricevuti, utilizzare l' \_ \_ integrità PKT del livello auth C RPC \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a4124-106">If the data should not be modified, and private data is not being sent or received, use RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY.</span></span> <span data-ttu-id="a4124-107">In tutti gli altri casi, usare \_ il \_ livello di autenticazione Pkt di RPC C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a4124-107">In all other cases, use RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

<span data-ttu-id="a4124-108">Non usare l' \_ impostazione predefinita del livello auth c RPC, la connessione del livello auth c \_ \_ \_ RPC \_ , la \_ chiamata al \_ \_ \_ \_ livello auth c RPC o il \_ \_ \_ \_ livello auth c \_ \_ PKT.</span><span class="sxs-lookup"><span data-stu-id="a4124-108">Do not use RPC\_C\_AUTHN\_LEVEL\_DEFAULT, RPC\_C\_AUTHN\_LEVEL\_CONNECT, RPC\_C\_AUTHN\_LEVEL\_CALL or RPC\_C\_AUTHN\_LEVEL\_PKT.</span></span> <span data-ttu-id="a4124-109">Un utente malintenzionato sofisticato può interrompere questi livelli di autenticazione e renderli inefficaci.</span><span class="sxs-lookup"><span data-stu-id="a4124-109">A sophisticated attacker can break these authentication levels and render them ineffective.</span></span> <span data-ttu-id="a4124-110">Ognuno di questi livelli rende leggermente più difficile per un utente malintenzionato intercettare e modificare i dati e per rappresentare, ma la sicurezza non viene realmente realizzata.</span><span class="sxs-lookup"><span data-stu-id="a4124-110">Each of these levels does make it slightly more difficult for an attacker to intercept and modify data, and to impersonate, but security is not really achieved.</span></span> <span data-ttu-id="a4124-111">Poiché il livello di sofisticazione di un utente malintenzionato è raramente noto, questi non sono scelte ottimali.</span><span class="sxs-lookup"><span data-stu-id="a4124-111">Since the sophistication level of an attacker is rarely known, these are not wise choices.</span></span>

 

 




