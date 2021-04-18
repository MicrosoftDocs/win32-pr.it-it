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
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a><span data-ttu-id="7e934-103">Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione</span><span class="sxs-lookup"><span data-stu-id="7e934-103">IPv6 Extensions to Navigator Auto-Config File Format</span></span>

<span data-ttu-id="7e934-104">Microsoft ha implementato una matrice di estensioni per il formato di file di configurazione automatica dello strumento di navigazione per aggiungere il supporto IPv6 nelle funzioni helper di WinINet e WinHTTP WPAD.</span><span class="sxs-lookup"><span data-stu-id="7e934-104">Microsoft has implemented an array of extensions to the Navigator Auto-Config File Format in order to add IPv6 support in the WinINet and WinHTTP WPAD helper functions.</span></span>

<span data-ttu-id="7e934-105">L'esplosione di Internet nel tardo 1990 ha causato una scarsità imprevista di indirizzi IPv4, con l'esaurimento del pool su base giornaliera.</span><span class="sxs-lookup"><span data-stu-id="7e934-105">The explosion of the Internet in the late 1990’s has caused an unexpected scarcity of IPv4 addresses, with the pool depleting on a daily basis.</span></span> <span data-ttu-id="7e934-106">IPv6 fornisce una soluzione a questo problema e anche se attualmente non è ampiamente distribuito, il suo utilizzo diventerà sicuramente più diffuso in futuro.</span><span class="sxs-lookup"><span data-stu-id="7e934-106">IPv6 provides a solution to this problem and although it is currently not widely deployed, its use will definitely become more prevalent in the future.</span></span> <span data-ttu-id="7e934-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) è un protocollo che consente ai client Web di rilevare automaticamente la configurazione corretta del proxy per il traffico in uscita.</span><span class="sxs-lookup"><span data-stu-id="7e934-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) is a protocol that allows web clients to automatically detect what the correct proxy configuration should be for their outgoing traffic.</span></span> <span data-ttu-id="7e934-108">Questa operazione è molto utile per le distribuzioni aziendali perché consente agli amministratori IT di configurare script complessi in grado di instradare il traffico per tutti i client a proxy specifici in base al server di destinazione a cui i client tentano di connettersi.</span><span class="sxs-lookup"><span data-stu-id="7e934-108">This is very useful for corporate deployments because it allows IT administrators to setup complex scripts that can route traffic for all clients to specific proxies based on the target server the clients are attempting to connect to.</span></span> <span data-ttu-id="7e934-109">WinINet e WinHTTP supportano le funzioni di supporto WPAD come definito dalla [specifica del formato di file PAC (auto-config) del proxy Navigator](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), che è diventato uno standard defacto.</span><span class="sxs-lookup"><span data-stu-id="7e934-109">WinINet and WinHTTP support WPAD helper functions as defined by the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), which has become a defacto standard.</span></span> <span data-ttu-id="7e934-110">Sfortunatamente questa specifica è stata scritta in 1996 e non definisce il comportamento dei comportamenti della funzione quando uno script WPAD viene distribuito in una rete in grado di supportare IPv6.</span><span class="sxs-lookup"><span data-stu-id="7e934-110">Unfortunately this specification was written in 1996 and does not define what the function behaviors should be when a WPAD script is deployed in an IPv6 capable network.</span></span>

<span data-ttu-id="7e934-111">Poiché IPv6 è l'onda del futuro, tutti i componenti di Windows supportano ora dual stack (IPv4 e IPv6) e solo reti IPv6.</span><span class="sxs-lookup"><span data-stu-id="7e934-111">Since IPv6 is the wave of the future, all Windows components now support dual stack (IPv4 and IPv6) and IPv6 only networks.</span></span> <span data-ttu-id="7e934-112">Per supportare IPv6 senza influire sulla distribuzione esistente, Microsoft ha aggiunto 6 nuove funzioni di classe helper come estensione della specifica del formato di file di Navigator proxy auto-config (PAC) ed è stata aggiunta anche una nuova funzione compatibile con IPv6 denominata **FindProxyForURLEx** che gli amministratori possono implementare nello script WPAD.</span><span class="sxs-lookup"><span data-stu-id="7e934-112">In order to support IPv6 without affecting existing deployment, Microsoft added 6 new helper class functions as an extension to the Navigator Proxy Auto-Config (PAC) File Format specification and also added a new IPv6 capable function called **FindProxyForURLEx** that administrators can implement in the WPAD script.</span></span>

<dl> <dt>

[<span data-ttu-id="7e934-113">Definizioni API helper proxy compatibili con IPv6</span><span class="sxs-lookup"><span data-stu-id="7e934-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[<span data-ttu-id="7e934-114">Differenze tra IPv6-Aware funzioni helper WPAD e funzioni helper WPAD legacy</span><span class="sxs-lookup"><span data-stu-id="7e934-114">Differences Between IPv6-Aware WPAD Helper Functions and Legacy WPAD Helper Functions</span></span>](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
<span data-ttu-id="7e934-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7e934-115"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="7e934-116">Questa funzionalità richiede Windows Internet Explorer 7 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="7e934-116">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



