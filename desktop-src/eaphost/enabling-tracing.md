---
title: Abilitazione della traccia EAPHost
description: Può aiutare gli utenti a individuare le cause principali dei problemi che si verificano durante il processo di autenticazione EAP. Le informazioni di debug possono includere chiamate API eseguite, chiamate di funzione interne eseguite e transizioni di stato eseguite.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104047636"
---
# <a name="enabling-eaphost-tracing"></a><span data-ttu-id="0cb5c-104">Abilitazione della traccia EAPHost</span><span class="sxs-lookup"><span data-stu-id="0cb5c-104">Enabling EAPHost Tracing</span></span>

<span data-ttu-id="0cb5c-105">I log di traccia contenenti informazioni di debug possono aiutare gli utenti a individuare le cause principali dei problemi che si verificano durante il processo di autenticazione EAP.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-105">Trace logs containing debugging information can assist users in finding the root causes of issues that occur during the EAP authentication process.</span></span> <span data-ttu-id="0cb5c-106">Le informazioni di debug possono includere chiamate API eseguite, chiamate di funzione interne eseguite e transizioni di stato eseguite.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-106">The debugging information can include API calls performed, internal function calls performed, and state transitions performed.</span></span>

<span data-ttu-id="0cb5c-107">La traccia può essere abilitata sia sul lato client sia sul lato Authenticator.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-107">Tracing can be enabled on both the client side and the authenticator side.</span></span> <span data-ttu-id="0cb5c-108">La traccia può essere abilitata anche per le chiamate alle API del [servizio Routing e accesso remoto (RRAS)](/windows/desktop/RRAS/routing-start-page) .</span><span class="sxs-lookup"><span data-stu-id="0cb5c-108">Tracing can also be enabled for calls to the [Routing and Remote Access Service (RRAS)](/windows/desktop/RRAS/routing-start-page) APIs.</span></span> <span data-ttu-id="0cb5c-109">Per ulteriori informazioni, vedere [la pagina relativa alla traccia nel servizio Routing e accesso remoto](#tracing-on-the-routing-and-remote-access-service).</span><span class="sxs-lookup"><span data-stu-id="0cb5c-109">For more information, see [Tracing on the Routing and Remote Access Service](#tracing-on-the-routing-and-remote-access-service).</span></span>

> [!Note]  
> <span data-ttu-id="0cb5c-110">I log di traccia sono disponibili solo in lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-110">Trace logs are available in English only.</span></span>

 

<span data-ttu-id="0cb5c-111">Quando è abilitata la traccia EAPHost, le informazioni di registrazione vengono archiviate in un file con estensione ETL in un percorso specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-111">When EAPHost tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="0cb5c-112">Se si verificano errori durante l'autenticazione EAP, la traccia genera un file con estensione ETL che può essere inviato a Microsoft supporto tecnico Developer per l'analisi della causa radice.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-112">If errors occur during EAP authentication, tracing generates an .etl file that can be sent to Microsoft Developer Support for root cause analysis.</span></span> <span data-ttu-id="0cb5c-113">I partner che hanno accesso ai file di Microsoft Windows Build shares, symbols e TraceFormat possono convertire i file con estensione ETL in un file di testo normale usando lo strumento **tracerpt** .</span><span class="sxs-lookup"><span data-stu-id="0cb5c-113">Partners that have access to Microsoft windows build shares, symbols, and traceformat files can convert the .etl files into a plain text file using the **tracerpt** tool.</span></span>

<span data-ttu-id="0cb5c-114">Gli errori del server dei criteri di rete non vengono acquisiti nei log EAPHost.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-114">Network policy server (NPS) failures are not captured in the EAPHost logs.</span></span> <span data-ttu-id="0cb5c-115">Se si sta tentando di risolvere un errore di NPS, visualizzare il IASSAM. LOG e [IASNAP. ](https://go.microsoft.com/fwlink/p/?linkid=84108) File di log.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-115">If you are trying to troubleshoot a NPS failure, view the IASSAM.LOG and [IASNAP.LOG](https://go.microsoft.com/fwlink/p/?linkid=84108) files.</span></span>

## <a name="tracing-on-the-client"></a><span data-ttu-id="0cb5c-116">Traccia nel client</span><span class="sxs-lookup"><span data-stu-id="0cb5c-116">Tracing on the Client</span></span>

<span data-ttu-id="0cb5c-117">Per abilitare la traccia sul lato client:</span><span class="sxs-lookup"><span data-stu-id="0cb5c-117">To enable tracing on the client side:</span></span>

1.  <span data-ttu-id="0cb5c-118">Aprire una finestra del prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="0cb5c-119">Eseguire il comando seguente: **logman** **Start Trace** **EapHostPeer** **-o** **. \\ EapHostPeer. etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="0cb5c-119">Run the following command: **logman** **start trace** **EapHostPeer** **-o** **.\\EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="0cb5c-120">Riprodurre lo scenario che si desidera tracciare.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-120">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="0cb5c-121">Eseguire il comando seguente: **logman** **Stop** **EapHostPeer** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="0cb5c-121">Run the following command: **logman** **stop** **EapHostPeer** **-ets**</span></span>
5.  <span data-ttu-id="0cb5c-122">Convertire il file ETL in testo usando il comando seguente: **tracerpt EapHostPeer. etl** **– PDB** **&lt; PDBPATH &gt;** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**</span><span class="sxs-lookup"><span data-stu-id="0cb5c-122">Convert the etl file into text using the following command: **tracerpt EapHostPeer.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostPeer.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="0cb5c-123">Se non si dispone dell'accesso allo strumento tracerpt, evitare l'ultimo passaggio e inviare il file con estensione ETL a Microsoft supporto tecnico Developer.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-123">If you do not have access to the tracerpt tool, avoid the last step and send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="tracing-on-the-authenticator"></a><span data-ttu-id="0cb5c-124">Traccia nell'autenticatore</span><span class="sxs-lookup"><span data-stu-id="0cb5c-124">Tracing on the Authenticator</span></span>

<span data-ttu-id="0cb5c-125">Per abilitare la traccia sul lato Authenticator:</span><span class="sxs-lookup"><span data-stu-id="0cb5c-125">To enable tracing on the authenticator side:</span></span>

1.  <span data-ttu-id="0cb5c-126">Aprire una finestra del prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-126">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="0cb5c-127">Eseguire il comando seguente: **logman** **Start Trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr. etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="0cb5c-127">Run the following command: **logman** **start trace** **EapHostAuthr** **-o** **.\\EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**</span></span>
3.  <span data-ttu-id="0cb5c-128">Riprodurre lo scenario che si desidera tracciare.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-128">Reproduce the scenario that you want to trace.</span></span>
4.  <span data-ttu-id="0cb5c-129">Eseguire il comando seguente: **logman** **Stop** **EapHostAuthr** **-ETS**</span><span class="sxs-lookup"><span data-stu-id="0cb5c-129">Run the following command: **logman** **stop** **EapHostAuthr** **-ets**</span></span>
5.  <span data-ttu-id="0cb5c-130">Convertire il file ETL in testo usando il comando seguente: **tracerpt EapHostAuthr. etl** **– PDB** **&lt; PDBPATH &gt;** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**</span><span class="sxs-lookup"><span data-stu-id="0cb5c-130">Convert the etl file into text using the following command: **tracerpt EapHostAuthr.etl** **–pdb** **&lt;pdbpath&gt;** **-tp** **&lt;tracemessagefilesdirectorypath&gt;** **-o** **EapHostAuthr.txt**</span></span>
    > [!Note]  
    > <span data-ttu-id="0cb5c-131">Se non si dispone dell'accesso allo strumento tracerpt, evitare l'ultimo passaggio e inviare invece il file con estensione ETL a Microsoft supporto tecnico Developer.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-131">If you do not have access to the tracerpt tool, avoid the last step and instead send the .etl file to Microsoft Developer Support.</span></span>

     

## <a name="event-tracing"></a><span data-ttu-id="0cb5c-132">Traccia eventi</span><span class="sxs-lookup"><span data-stu-id="0cb5c-132">Event tracing</span></span>

<span data-ttu-id="0cb5c-133">In Windows 7 e nelle versioni successive di Windows, EapHost fornisce la traccia basata su eventi per l'autenticatore e il peer.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-133">In Windows 7 and later versions of Windows, EapHost provides event based tracing on the authenticator and the peer.</span></span> <span data-ttu-id="0cb5c-134">Il vantaggio della traccia basata su eventi è che non sono necessari file di simboli per visualizzare i messaggi di traccia.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-134">The advantage of event based tracing is that no symbol files are needed to view the trace messages.</span></span> <span data-ttu-id="0cb5c-135">Per abilitare la traccia eventi:</span><span class="sxs-lookup"><span data-stu-id="0cb5c-135">To enable event tracing:</span></span>

1.  <span data-ttu-id="0cb5c-136">Aprire **eventviewer**.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-136">Open **EventViewer**.</span></span>
2.  <span data-ttu-id="0cb5c-137">Messaggi EapHost critici registrati in: "visualizzazioni personalizzate \\ eventi amministrativi"</span><span class="sxs-lookup"><span data-stu-id="0cb5c-137">Critical EapHost messages are logged under: “Custom Views\\Administrative Events”</span></span>
3.  <span data-ttu-id="0cb5c-138">Messaggi non critici registrati in: "applicazioni e servizi \\ Microsoft \\ Windows \\ EAPHost</span><span class="sxs-lookup"><span data-stu-id="0cb5c-138">Non-critical messages are logged under: “Applications and Services\\Microsoft\\Windows\\EapHost</span></span>
4.  <span data-ttu-id="0cb5c-139">I messaggi di evento di tipo "analitico" e "debug" possono essere visualizzati nello stesso percorso selezionando **Mostra log analitici e di debug** dal menu **Visualizza** della barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-139">"Analytic" and "Debug" type event messages can be seen under the same path by selecting **Show Analytic and Debug Logs** from the **view** menu in the title bar.</span></span>

## <a name="tracing-on-the-routing-and-remote-access-service"></a><span data-ttu-id="0cb5c-140">Traccia nel servizio Routing e accesso remoto</span><span class="sxs-lookup"><span data-stu-id="0cb5c-140">Tracing on the Routing and Remote Access Service</span></span>

<span data-ttu-id="0cb5c-141">Per abilitare la traccia RRAS:</span><span class="sxs-lookup"><span data-stu-id="0cb5c-141">To enable RRAS tracing:</span></span>

1.  <span data-ttu-id="0cb5c-142">Aprire una finestra del prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-142">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="0cb5c-143">Eseguire il comando seguente: **netsh** **RAS** **set** **TR** **\* *_ _* en**</span><span class="sxs-lookup"><span data-stu-id="0cb5c-143">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* en*\*</span></span>
3.  <span data-ttu-id="0cb5c-144">Aprire **% systemroot% \\ Tracing** per visualizzare le tracce RAS</span><span class="sxs-lookup"><span data-stu-id="0cb5c-144">Open **%systemroot%\\tracing** to view RAS traces</span></span>

<span data-ttu-id="0cb5c-145">Per disabilitare la traccia RRAS:</span><span class="sxs-lookup"><span data-stu-id="0cb5c-145">To disable RRAS tracing:</span></span>

1.  <span data-ttu-id="0cb5c-146">Aprire una finestra del prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="0cb5c-146">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="0cb5c-147">Eseguire il comando seguente: **netsh** **RAS** **set** **TR** **\* *_ _* dis**</span><span class="sxs-lookup"><span data-stu-id="0cb5c-147">Run the following command: **netsh** **ras** **set** **tr** **\**_ _\* dis*\*</span></span>

<span data-ttu-id="0cb5c-148">Per ulteriori informazioni, vedere [comandi netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="0cb5c-148">For more information, see [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cb5c-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cb5c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cb5c-150">Uso di EAPHost</span><span class="sxs-lookup"><span data-stu-id="0cb5c-150">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="0cb5c-151">Servizio Routing e Accesso remoto (RRAS)</span><span class="sxs-lookup"><span data-stu-id="0cb5c-151">Routing and Remote Access Service (RRAS)</span></span>](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 