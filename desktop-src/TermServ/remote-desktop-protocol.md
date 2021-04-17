---
title: Remote Desktop Protocol
description: Il protocollo Desktop remoto Microsoft (RDP) fornisce funzionalità di visualizzazione e input Remote sulle connessioni di rete per le applicazioni basate su Windows in esecuzione in un server.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Remote Desktop Protocol (RDP) Servizi Desktop remoto
- RDP (vedere Remote Desktop Protocol)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299920"
---
# <a name="remote-desktop-protocol"></a><span data-ttu-id="47f04-105">Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="47f04-105">Remote Desktop Protocol</span></span>

<span data-ttu-id="47f04-106">Il protocollo Desktop remoto Microsoft (RDP) fornisce funzionalità di visualizzazione e input Remote sulle connessioni di rete per le applicazioni basate su Windows in esecuzione in un server.</span><span class="sxs-lookup"><span data-stu-id="47f04-106">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span> <span data-ttu-id="47f04-107">RDP è progettato per supportare diversi tipi di topologie di rete e più protocolli LAN.</span><span class="sxs-lookup"><span data-stu-id="47f04-107">RDP is designed to support different types of network topologies and multiple LAN protocols.</span></span>

> [!Note]  
> <span data-ttu-id="47f04-108">Questo argomento è per gli sviluppatori di software.</span><span class="sxs-lookup"><span data-stu-id="47f04-108">This topic is for software developers.</span></span> <span data-ttu-id="47f04-109">Per informazioni sull'utente per Desktop remoto, vedere [supporto di Windows](https://windows.microsoft.com/windows/support#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="47f04-109">If you are looking for user information for Remote Desktop, see [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8).</span></span> <span data-ttu-id="47f04-110">Per informazioni sui professionisti IT per Desktop remoto, vedere [Servizi Desktop remoto su TechNet](/windows/deployment/deploy-whats-new).</span><span class="sxs-lookup"><span data-stu-id="47f04-110">If you are looking for IT professional information for Remote Desktop, see [Remote Desktop Services on TechNet](/windows/deployment/deploy-whats-new).</span></span>

 

## <a name="basic-architecture"></a><span data-ttu-id="47f04-111">Architettura di base</span><span class="sxs-lookup"><span data-stu-id="47f04-111">Basic Architecture</span></span>

<span data-ttu-id="47f04-112">RDP si basa su e su un'estensione della famiglia di protocolli ITU T. 120.</span><span class="sxs-lookup"><span data-stu-id="47f04-112">RDP is based on, and an extension of, the ITU T.120 family of protocols.</span></span> <span data-ttu-id="47f04-113">RDP è un protocollo in grado di supportare più canali che consente di usare canali virtuali distinti per il trasporto di dati di comunicazione e presentazione del dispositivo dal server, oltre ai dati crittografati del mouse e della tastiera del client.</span><span class="sxs-lookup"><span data-stu-id="47f04-113">RDP is a multiple-channel capable protocol that allows for separate virtual channels for carrying device communication and presentation data from the server, as well as encrypted client mouse and keyboard data.</span></span> <span data-ttu-id="47f04-114">RDP fornisce una base estendibile e supporta fino a 64.000 canali separati per la trasmissione dei dati e il provisioning per la trasmissione multipoint.</span><span class="sxs-lookup"><span data-stu-id="47f04-114">RDP provides an extensible base and supports up to 64,000 separate channels for data transmission and provisions for multipoint transmission.</span></span>

<span data-ttu-id="47f04-115">Sul server, RDP usa il proprio driver video per eseguire il rendering dell'output di visualizzazione costruendo le informazioni di rendering nei pacchetti di rete usando il protocollo RDP e inviando i dati attraverso la rete al client.</span><span class="sxs-lookup"><span data-stu-id="47f04-115">On the server, RDP uses its own video driver to render display output by constructing the rendering information into network packets by using RDP protocol and sending them over the network to the client.</span></span> <span data-ttu-id="47f04-116">Sul client, il protocollo RDP riceve i dati di rendering e interpreta i pacchetti nelle chiamate API GDI (Graphics Device Interface) corrispondenti di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="47f04-116">On the client, RDP receives rendering data and interprets the packets into corresponding Microsoft Windows graphics device interface (GDI) API calls.</span></span> <span data-ttu-id="47f04-117">Per il percorso di input, gli eventi del mouse e della tastiera del client vengono reindirizzati dal client al server.</span><span class="sxs-lookup"><span data-stu-id="47f04-117">For the input path, client mouse and keyboard events are redirected from the client to the server.</span></span> <span data-ttu-id="47f04-118">Sul server, il protocollo RDP utilizza il proprio driver di tastiera e mouse per ricevere gli eventi della tastiera e del mouse.</span><span class="sxs-lookup"><span data-stu-id="47f04-118">On the server, RDP uses its own keyboard and mouse driver to receive these keyboard and mouse events.</span></span>

<span data-ttu-id="47f04-119">In una sessione di Desktop remoto tutte le variabili di ambiente, ad esempio le variabili che determinano la profondità dei colori e l'abilitazione e la disabilitazione dello sfondo, sono determinate dalle impostazioni di connessione RCP-Tcp.</span><span class="sxs-lookup"><span data-stu-id="47f04-119">In a Remote Desktop session, all environment variables—for example, variables determining color depth and wallpaper enabling and disabling—are determined by the RCP-Tcp connection settings.</span></span> <span data-ttu-id="47f04-120">Questo vale per tutte le funzioni e i metodi che impostano le variabili di ambiente nel [riferimento connessione Web Desktop remoto](remote-desktop-web-connection-reference.md) e nell' [interfaccia del provider servizi desktop remoto WMI](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="47f04-120">This applies to all functions and methods that set environment variables in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) and the [Remote Desktop Services WMI Provider interface](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="features"></a><span data-ttu-id="47f04-121">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="47f04-121">Features</span></span>

<span data-ttu-id="47f04-122">In Microsoft RDP sono incluse le funzionalità e le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="47f04-122">Microsoft RDP includes the following features and capabilities:</span></span>

<dl> <dt>

<span data-ttu-id="47f04-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Crittografia</span><span class="sxs-lookup"><span data-stu-id="47f04-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encryption</span></span>
</dt> <dd>

<span data-ttu-id="47f04-124">RDP usa la crittografia RC4 di RSA Security, una crittografia di flusso progettata per crittografare in modo efficiente piccole quantità di dati.</span><span class="sxs-lookup"><span data-stu-id="47f04-124">RDP uses RSA Security's RC4 cipher, a stream cipher designed to efficiently encrypt small amounts of data.</span></span> <span data-ttu-id="47f04-125">RC4 è progettato per garantire comunicazioni sicure su reti.</span><span class="sxs-lookup"><span data-stu-id="47f04-125">RC4 is designed for secure communications over networks.</span></span> <span data-ttu-id="47f04-126">Gli amministratori possono scegliere di crittografare i dati usando una chiave di 56 o 128 bit.</span><span class="sxs-lookup"><span data-stu-id="47f04-126">Administrators can choose to encrypt data by using a 56- or 128-bit key.</span></span>

</dd> <dt>

<span data-ttu-id="47f04-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Funzionalità di riduzione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="47f04-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Bandwidth reduction features</span></span>
</dt> <dd>

<span data-ttu-id="47f04-128">RDP supporta diversi meccanismi per ridurre la quantità di dati trasmessi tramite una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="47f04-128">RDP supports various mechanisms to reduce the amount of data transmitted over a network connection.</span></span> <span data-ttu-id="47f04-129">I meccanismi includono la compressione dei dati, la memorizzazione nella cache persistente delle bitmap e la memorizzazione nella cache di glifi e frammenti in RAM.</span><span class="sxs-lookup"><span data-stu-id="47f04-129">Mechanisms include data compression, persistent caching of bitmaps, and caching of glyphs and fragments in RAM.</span></span> <span data-ttu-id="47f04-130">La cache di bitmap persistente può offrire un miglioramento sostanziale delle prestazioni rispetto alle connessioni a larghezza di banda ridotta, soprattutto quando si eseguono applicazioni che fanno uso estensivo di bitmap di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="47f04-130">The persistent bitmap cache can provide a substantial improvement in performance over low-bandwidth connections, especially when running applications that make extensive use of large bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="47f04-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Disconnessione roaming</span><span class="sxs-lookup"><span data-stu-id="47f04-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming disconnect</span></span>
</dt> <dd>

<span data-ttu-id="47f04-132">Un utente può disconnettersi manualmente da una sessione di desktop remoto senza disconnettersi.</span><span class="sxs-lookup"><span data-stu-id="47f04-132">A user can manually disconnect from a remote desktop session without logging off.</span></span> <span data-ttu-id="47f04-133">L'utente viene automaticamente riconnesso alla sessione disconnessa quando si connette nuovamente al sistema, dallo stesso dispositivo o da un dispositivo diverso.</span><span class="sxs-lookup"><span data-stu-id="47f04-133">The user is automatically reconnected to their disconnected session when he or she logs back onto the system, either from the same device or a different device.</span></span> <span data-ttu-id="47f04-134">Quando la sessione di un utente viene interrotta in modo imprevisto da un errore di rete o del client, l'utente viene disconnesso ma non disconnesso.</span><span class="sxs-lookup"><span data-stu-id="47f04-134">When a user's session is unexpectedly terminated by a network or client failure, the user is disconnected but not logged off.</span></span>

</dd> <dt>

<span data-ttu-id="47f04-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Mapping degli Appunti</span><span class="sxs-lookup"><span data-stu-id="47f04-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Clipboard mapping</span></span>
</dt> <dd>

<span data-ttu-id="47f04-136">Gli utenti possono eliminare, copiare e incollare testo e grafica tra le applicazioni in esecuzione nel computer locale e quelle eseguite in una sessione Desktop remoto e tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="47f04-136">Users can delete, copy, and paste text and graphics between applications running on the local computer and those running in a remote desktop session, and between sessions.</span></span>

</dd> <dt>

<span data-ttu-id="47f04-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Reindirizzamento di stampa</span><span class="sxs-lookup"><span data-stu-id="47f04-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Print redirection</span></span>
</dt> <dd>

<span data-ttu-id="47f04-138">Le applicazioni in esecuzione all'interno di una sessione Desktop remoto possono stampare su una stampante collegata al dispositivo client.</span><span class="sxs-lookup"><span data-stu-id="47f04-138">Applications running within a remote desktop session can print to a printer attached to the client device.</span></span>

</dd> <dt>

<span data-ttu-id="47f04-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canali virtuali</span><span class="sxs-lookup"><span data-stu-id="47f04-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtual channels</span></span>
</dt> <dd>

<span data-ttu-id="47f04-140">Utilizzando l'architettura del canale virtuale RDP, è possibile aumentare le applicazioni esistenti e sviluppare nuove applicazioni per aggiungere funzionalità che richiedono le comunicazioni tra il dispositivo client e un'applicazione in esecuzione in una sessione di desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="47f04-140">By using RDP virtual channel architecture, existing applications can be augmented and new applications can be developed to add features that require communications between the client device and an application running in a remote desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="47f04-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Controllo remoto</span><span class="sxs-lookup"><span data-stu-id="47f04-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote control</span></span>
</dt> <dd>

<span data-ttu-id="47f04-142">Il personale di supporto del computer può visualizzare e controllare una sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="47f04-142">Computer support staff can view and control a remote desktop session.</span></span> <span data-ttu-id="47f04-143">La condivisione di input e la visualizzazione di immagini tra due sessioni di desktop remoto offre a un utente di supporto la possibilità di diagnosticare e risolvere i problemi in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="47f04-143">Sharing input and display graphics between two remote desktop sessions gives a support person the ability to diagnose and resolve problems remotely.</span></span>

</dd> <dt>

<span data-ttu-id="47f04-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Bilanciamento carico di rete</span><span class="sxs-lookup"><span data-stu-id="47f04-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network load balancing</span></span>
</dt> <dd>

<span data-ttu-id="47f04-145">RDP sfrutta i vantaggi del bilanciamento del carico di rete, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="47f04-145">RDP takes advantage of network load balancing (NLB), where available.</span></span>

</dd> </dl>

<span data-ttu-id="47f04-146">Inoltre, RDP contiene le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="47f04-146">In addition, RDP contains the following features:</span></span>

-   <span data-ttu-id="47f04-147">Supporto per il colore a 24 bit.</span><span class="sxs-lookup"><span data-stu-id="47f04-147">Support for 24-bit color.</span></span>
-   <span data-ttu-id="47f04-148">Miglioramento delle prestazioni rispetto alle connessioni remote a bassa velocità tramite una larghezza di banda ridotta.</span><span class="sxs-lookup"><span data-stu-id="47f04-148">Improved performance over low-speed dial-up connections through reduced bandwidth.</span></span>
-   <span data-ttu-id="47f04-149">Autenticazione con smart card tramite Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="47f04-149">Smart Card authentication through Remote Desktop Services.</span></span>
-   <span data-ttu-id="47f04-150">Hook da tastiera.</span><span class="sxs-lookup"><span data-stu-id="47f04-150">Keyboard hooking.</span></span> <span data-ttu-id="47f04-151">Possibilità di indirizzare le combinazioni di tasti speciali di Windows, in modalità schermo intero, al computer locale o a un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="47f04-151">The ability to direct special Windows key combinations, in full-screen mode, to the local computer or to a remote computer.</span></span>
-   <span data-ttu-id="47f04-152">Reindirizzamento stampanti audio, unità, porta e rete.</span><span class="sxs-lookup"><span data-stu-id="47f04-152">Sound, drive, port, and network printer redirection.</span></span> <span data-ttu-id="47f04-153">I suoni che si verificano nel computer remoto possono essere rilevati nel computer client in cui è in esecuzione il client RDC e le unità client locali saranno visibili alla sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="47f04-153">Sounds that occur on the remote computer can be heard on the client computer running the RDC client, and local client drives will be visible to the remote desktop session.</span></span>

 

 