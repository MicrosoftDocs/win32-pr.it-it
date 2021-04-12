---
description: Informazioni sull'architettura di ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Informazioni sull'architettura di ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233703"
---
# <a name="about-the-acm-architecture"></a>Informazioni sull'architettura di ACM

Il modulo di configurazione automatica (ACM) è il nuovo componente di configurazione wireless per Windows Vista. Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) usano invece il servizio Wireless Zero Configuration (WZC).

L'ACM analizza periodicamente le reti e usa un processo iterativo per selezionare e connettersi alla rete preferita nell'intervallo, se tale rete ha un'interfaccia abilitata per la connessione automatica. L'ACM Salva e recupera anche i profili di rete, che contengono le impostazioni di ACM, media Specific Module (MSM), Security e Independent Hardware Vendor (IHV). Questi profili di rete sono per la configurazione automatica.

La configurazione automatica supporta le impostazioni globali e per interfaccia e i profili di rete. Le impostazioni globali e i profili di rete vengono configurati se il computer è stato aggiunto a un dominio con un oggetto Criteri di gruppo a livello di dominio o unità organizzativa (OU) nella gerarchia di Active Directory (AD). Le impostazioni e i profili di criteri di gruppo sono di sola lettura, applicati a ogni interfaccia 802,11 nel sistema e hanno sempre la precedenza sulle impostazioni per interfaccia e per utente e i profili di rete. I profili criteri di gruppo sono posizionati nella parte superiore dell'elenco Profilo di rete preferito in ogni interfaccia di rete 802,11.

L'architettura di ACM è estendibile. IHV può implementare funzionalità wireless proprietarie senza modificare il Framework 802,11 nativo fornito. Le funzioni e le strutture di controllo IHV esposte abilitano questa estensibilità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Wi-Fi nativo](about-native-wifi.md)
</dt> </dl>

 

 



