---
title: Application Layer Enforcement (ALE)
description: ALE è un set di livelli in modalità kernel di Windows Filtering Platform (WFP) usati per il filtro con stato.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398977"
---
# <a name="application-layer-enforcement-ale"></a>Application Layer Enforcement (ALE)

ALE è un set di livelli in modalità kernel di Windows Filtering Platform (WFP) usati per il filtro con stato.

Il filtro con stato tiene traccia dello stato delle connessioni di rete e consente solo i pacchetti che corrispondono a uno stato di connessione noto. Ad esempio, il filtro con stato per una connessione TCP avviata da un firewall può consentire solo i pacchetti in ingresso che corrispondono ai pacchetti in uscita precedenti inviati dall'entità protetta.

I filtri nei livelli ALE autorizzano la creazione di connessioni in ingresso e in uscita, le assegnazioni delle porte, le operazioni socket come [**Listen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), la creazione di socket non elaborati e la ricezione in modalità promiscua.

Il traffico ai livelli ALE è classificato come operazione per connessione o per socket. Ai livelli non ALE i filtri possono solo classificare il traffico in base ai singoli pacchetti.

I livelli ALE sono gli unici livelli PAM in cui è possibile filtrare il traffico di rete in base all'identità dell'applicazione, usando un nome di file normalizzato, e in base all'identità dell'utente, usando un descrittore di sicurezza. (Vedere FLT \_ \_ \_ Informazioni sul nome file nella documentazione di Windows Driver Kit (WDK), per ulteriori informazioni sui nomi file normalizzati.

Inoltre, quando si usa IPsec per proteggere la connessione, è possibile eseguire il filtro ai livelli ALE anche sull'identità del computer remoto e sull'identità utente remota. Le identità del computer remoto e dell'utente vengono ottenute dalle credenziali utilizzate per la creazione di una sessione IPsec.

Per questo motivo, i criteri che impongono chi (ad esempio, "amministratore") e/o quale applicazione (ad esempio, "Internet Explorer") sono autorizzati a eseguire le operazioni di rete citate sopra vengono creati a livello di ALE.

ALE fornisce l'imposizione dei criteri, ad esempio "Consenti a Windows Messenger di accedere alla rete durante il blocco di tutte le altre applicazioni". In questo esempio, quando l'applicazione "Messenger" si connette attraverso la rete, ALE intercetta l'evento, determina che è stato avviato da Messenger ed esegue una query sul motore di filtro WFP per determinare se il socket deve essere autorizzato a continuare.

> [!Note]  
> A causa della natura dei socket dual-IP reali, le classificazioni a livello di ALE IPv4 potrebbero non verificarsi. Questo è dovuto alla progettazione, perché per tutti gli Intent e gli scopi, il socket è un socket IPv6. Per visualizzare il traffico V4 per un socket di questo tipo, creare filtri a livello V6 usando l'indirizzo mappato a IPv6.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Traffico di broadcast/multicast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[Personalizzazione del flusso di ALE](ale-flow-customization.md)
</dt> </dl>

 

 