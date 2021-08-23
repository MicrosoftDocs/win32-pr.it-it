---
description: Il tunneling automatico con indirizzi compatibili con IPv4 e 6to4 funziona entrambi tramite una route per un prefisso che è on-link \# all'interfaccia 2. I 32 bit che segue il prefisso vengono estratti e usati come indirizzo di destinazione IPv4 per il pacchetto incapsulato.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Tunneling automatico IPv6 e 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4170d937e331d38337c21b777ae232a39fcb304f8550a1d1ed994ef55101bb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758491"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a>Tunneling automatico IPv6 e 6to4

Il tunneling automatico con indirizzi compatibili con IPv4 e 6to4 funziona entrambi tramite una route per un prefisso che è on-link \# all'interfaccia 2. I 32 bit che segue il prefisso vengono estratti e usati come indirizzo di destinazione IPv4 per il pacchetto incapsulato.

Il tunneling automatico usa il prefisso ::/96, che è abilitato per impostazione predefinita. Può essere disabilitato rimuovendo la route per ::/96.

6to4 usa il prefisso 2002::/16, che non è abilitato per impostazione predefinita.

 

 



