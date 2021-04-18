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
# <a name="ipv6-automatic-tunneling-and-6to4"></a>Tunneling automatico IPv6 e 6to4

Il tunneling automatico con indirizzi compatibili con IPv4 e 6to4 entrambi funzionano tramite una route per un prefisso collegato all'interfaccia \# 2. I 32 bit che seguono il prefisso vengono estratti e utilizzati come indirizzo di destinazione IPv4 per il pacchetto incapsulato.

Il tunneling automatico usa il prefisso::/96, che è abilitato per impostazione predefinita. Può essere disabilitato rimuovendo la route per::/96.

6to4 utilizza il prefisso 2002::/16, che non è abilitato per impostazione predefinita.

 

 



