---
title: Applicazione a livello di applicazione (ALE)
description: ALE è un set di Windows in modalità kernel che vengono usati per il filtro con stato.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d74db5fdc231569f65c3b25cb630b306111aa5d6a7e3eb7faad743a5f74db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069471"
---
# <a name="application-layer-enforcement-ale"></a>Applicazione a livello di applicazione (ALE)

ALE è un set di Windows in modalità kernel che vengono usati per il filtro con stato.

Il filtro con stato tiene traccia dello stato delle connessioni di rete e consente solo pacchetti che corrispondono a uno stato di connessione noto. Ad esempio, il filtro con stato per una connessione TCP avviata da dietro un firewall può consentire solo pacchetti in ingresso che corrispondono ai pacchetti in uscita precedenti inviati dall'entità protetta.

I filtri nei livelli ALE autorizzano la creazione di connessioni in ingresso e in uscita, le assegnazioni di porte, le operazioni socket come [**listen(),**](/windows/desktop/api/winsock2/nf-winsock2-listen)la creazione di socket non elaborati e la ricezione in modalità promiscua.

Il traffico ai livelli ALE viene classificato per ogni connessione o operazione per socket. Nei livelli non ALE, i filtri possono classificare il traffico solo per pacchetto.

I livelli ALE sono gli unici livelli WFP in cui il traffico di rete può essere filtrato in base all'identità dell'applicazione, usando un nome di file normalizzato e in base all'identità utente, usando un descrittore di sicurezza. (Vedere FLT) \_ FILE \_ NAME INFORMATION nella documentazione di Windows Driver Kit \_ (WDK) per altre informazioni sui nomi di file normalizzati.

Inoltre, quando si usa IPsec per proteggere la connessione, è possibile applicare filtri ai livelli ALE anche sull'identità del computer remoto e sull'identità utente remota. Le identità utente e del computer remoto vengono ottenute dalle credenziali usate nella creazione di una sessione IPsec.

Per questo motivo, i criteri che imponino chi (ad esempio, "amministratore") e/o quale applicazione (ad esempio, "Internet Explorer") è autorizzata a eseguire le operazioni di rete indicate in precedenza vengono creati ai livelli ALE.

ALE fornisce l'imposizione di criteri come "consentire Windows Messenger a tutti gli accessi alla rete bloccando tutte le altre applicazioni". In questo esempio, quando l'applicazione "Messenger" si connette attraverso la rete, ALE intercetta l'evento, determina che è stato avviato da Messenger ed esegue una query sul motore di filtro WFP per determinare se il socket deve essere autorizzato a procedere.

> [!Note]  
> A causa della natura dei veri socket dual-IP, le classificazioni al livello ALE IPv4 potrebbero non verificarsi. Questo è per impostazione predefinita, perché per tutte le finalità e per tutti gli scopi, il socket è un socket IPv6. Per visualizzare il traffico V4 per un socket di questo tipo, creare filtri a livello V6 usando l'indirizzo mappato IPv6.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Traffico multicast/broadcast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[Personalizzazione Flow ale](ale-flow-customization.md)
</dt> </dl>

 

 