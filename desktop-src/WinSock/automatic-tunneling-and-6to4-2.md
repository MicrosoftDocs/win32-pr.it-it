---
description: Il tunneling automatico con indirizzi compatibili con IPv4 e 6to4 entrambi funzionano tramite una route per un prefisso collegato all'interfaccia \# 2. I 32 bit che seguono il prefisso vengono estratti e utilizzati come indirizzo di destinazione IPv4 per il pacchetto incapsulato.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Tunneling automatico IPv6 e 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307048"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a><span data-ttu-id="2b686-104">Tunneling automatico IPv6 e 6to4</span><span class="sxs-lookup"><span data-stu-id="2b686-104">IPv6 Automatic Tunneling and 6to4</span></span>

<span data-ttu-id="2b686-105">Il tunneling automatico con indirizzi compatibili con IPv4 e 6to4 entrambi funzionano tramite una route per un prefisso collegato all'interfaccia \# 2.</span><span class="sxs-lookup"><span data-stu-id="2b686-105">Automatic tunneling with IPv4-compatible addresses and 6to4 both work through a route for a prefix that is on-link to interface \#2.</span></span> <span data-ttu-id="2b686-106">I 32 bit che seguono il prefisso vengono estratti e utilizzati come indirizzo di destinazione IPv4 per il pacchetto incapsulato.</span><span class="sxs-lookup"><span data-stu-id="2b686-106">The 32 bits following the prefix are extracted and used as an IPv4 destination address for the encapsulated packet.</span></span>

<span data-ttu-id="2b686-107">Il tunneling automatico usa il prefisso::/96, che è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2b686-107">Automatic tunneling uses the ::/96 prefix, which is enabled by default.</span></span> <span data-ttu-id="2b686-108">Può essere disabilitato rimuovendo la route per::/96.</span><span class="sxs-lookup"><span data-stu-id="2b686-108">It can be disabled by removing the route for ::/96.</span></span>

<span data-ttu-id="2b686-109">6to4 utilizza il prefisso 2002::/16, che non è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2b686-109">6to4 uses the 2002::/16 prefix, which is not enabled by default.</span></span>

 

 



