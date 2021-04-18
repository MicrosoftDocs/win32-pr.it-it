---
description: Microsoft ha implementato una matrice di estensioni per il formato di file di configurazione automatica dello strumento di navigazione per aggiungere il supporto IPv6 nelle funzioni helper di WinINet e WinHTTP WPAD.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317017"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione

Microsoft ha implementato una matrice di estensioni per il formato di file di configurazione automatica dello strumento di navigazione per aggiungere il supporto IPv6 nelle funzioni helper di WinINet e WinHTTP WPAD.

L'esplosione di Internet nel tardo 1990 ha causato una scarsità imprevista di indirizzi IPv4, con l'esaurimento del pool su base giornaliera. IPv6 fornisce una soluzione a questo problema e anche se attualmente non è ampiamente distribuito, il suo utilizzo diventerà sicuramente più diffuso in futuro. [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) è un protocollo che consente ai client Web di rilevare automaticamente la configurazione corretta del proxy per il traffico in uscita. Questa operazione è molto utile per le distribuzioni aziendali perché consente agli amministratori IT di configurare script complessi in grado di instradare il traffico per tutti i client a proxy specifici in base al server di destinazione a cui i client tentano di connettersi. WinINet e WinHTTP supportano le funzioni di supporto WPAD come definito dalla [specifica del formato di file PAC (auto-config) del proxy Navigator](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), che è diventato uno standard defacto. Sfortunatamente questa specifica è stata scritta in 1996 e non definisce il comportamento dei comportamenti della funzione quando uno script WPAD viene distribuito in una rete in grado di supportare IPv6.

Poiché IPv6 è l'onda del futuro, tutti i componenti di Windows supportano ora dual stack (IPv4 e IPv6) e solo reti IPv6. Per supportare IPv6 senza influire sulla distribuzione esistente, Microsoft ha aggiunto 6 nuove funzioni di classe helper come estensione della specifica del formato di file di Navigator proxy auto-config (PAC) ed è stata aggiunta anche una nuova funzione compatibile con IPv6 denominata **FindProxyForURLEx** che gli amministratori possono implementare nello script WPAD.

<dl> <dt>

[Definizioni API helper proxy compatibili con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[Differenze tra IPv6-Aware funzioni helper WPAD e funzioni helper WPAD legacy](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> Questa funzionalità richiede Windows Internet Explorer 7 o versione successiva.

 

 

 



