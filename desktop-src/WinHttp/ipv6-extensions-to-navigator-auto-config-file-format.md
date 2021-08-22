---
description: Microsoft ha implementato una matrice di estensioni per navigator Auto-Config File Format per aggiungere il supporto IPv6 nelle funzioni helper WinINet e WinHTTP WPAD.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6db6d687cfde0c3289026e8fa36c77c3ff5372727d1604652160b0683169b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644011"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione

Microsoft ha implementato una matrice di estensioni per navigator Auto-Config File Format per aggiungere il supporto IPv6 nelle funzioni helper WinINet e WinHTTP WPAD.

L'esplosione di Internet alla fine degli anni '90 ha causato una scarsità imprevista di indirizzi IPv4, con il pool in esaurimento su base giornaliera. IPv6 offre una soluzione a questo problema e anche se attualmente non è ampiamente distribuito, il suo uso diventerà sicuramente più prevalente in futuro. [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) è un protocollo che consente ai client Web di rilevare automaticamente la configurazione del proxy corretta per il traffico in uscita. Ciò è molto utile per le distribuzioni aziendali perché consente agli amministratori IT di configurare script complessi in grado di indirizzare il traffico per tutti i client a proxy specifici in base al server di destinazione a cui i client tentano di connettersi. WinINet e WinHTTP supportano le funzioni helper WPAD come definito dalla specifica del formato di [file PAC (Navigator Proxy Auto-Config),](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html)che è diventata uno standard defacto. Sfortunatamente questa specifica è stata scritta nel 1996 e non definisce i comportamenti della funzione quando uno script WPAD viene distribuito in una rete con supporto IPv6.

Poiché IPv6 è l'ondata del futuro, tutti i componenti Windows supportano ora le reti dual stack (IPv4 e IPv6) e solo IPv6. Per supportare IPv6 senza influire sulla distribuzione esistente, Microsoft ha aggiunto 6 nuove funzioni di classe helper come estensione alla specifica del formato di file PAC (Navigator Proxy Auto-Config) e ha aggiunto anche una nuova funzione con supporto IPv6 denominata **FindProxyForURLEx** che gli amministratori possono implementare nello script WPAD.

<dl> <dt>

[Definizioni dell'API helper proxy con supporto IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[Differenze tra IPv6-Aware funzioni helper WPAD e funzioni helper WPAD legacy](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> Questa funzionalità richiede Windows Internet Explorer 7 o versione successiva.

 

 

 



