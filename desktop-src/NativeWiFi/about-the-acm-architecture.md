---
description: Informazioni sull'architettura di ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Informazioni sull'architettura di ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d75b6b365970c34174facd035ddf38c625e3e4fac72f011e612998c46e9bee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065177"
---
# <a name="about-the-acm-architecture"></a>Informazioni sull'architettura di ACM

Il modulo di configurazione automatica (ACM) è il nuovo componente di configurazione wireless per Windows Vista. Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) usano invece il servizio Wireless Zero Configuration (WZC).

ACM analizza periodicamente le reti e usa un processo iterativo per selezionare e connettersi alla rete preferita nell'intervallo, se tale rete ha un'interfaccia abilitata per la connessione automatica. ACM salva e recupera anche i profili di rete che contengono le impostazioni ACM, MSM (Media Specific Module), sicurezza e fornitore di hardware indipendente (IHV). Questi profili di rete sono per la configurazione automatica.

La configurazione automatica supporta le impostazioni globali e per interfaccia e i profili di rete. Le impostazioni globali e i profili di rete vengono configurati se il computer è stato aggiunto a un dominio con un oggetto Criteri di gruppo a livello di dominio o di unità organizzativa (OU) nella gerarchia di Active Directory (AD). Queste impostazioni e profili di Criteri di gruppo sono di sola lettura, applicati a ogni interfaccia 802.11 nel sistema e hanno sempre la precedenza sulle impostazioni per interfaccia e per utente e sui profili di rete. I profili di Criteri di gruppo vengono inseriti all'inizio dell'elenco dei profili di rete preferiti in ogni interfaccia di rete 802.11.

L'architettura ACM è estendibile. IHV possono implementare funzionalità wireless proprietarie senza modificare il framework nativo 802.11 fornito. Le funzioni e le strutture di controllo IHV esposte abilitano questa estendibilità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Wi-Fi nativo](about-native-wifi.md)
</dt> </dl>

 

 



