---
title: Strutture API Servizi Desktop remoto
description: Elenca le strutture usate con l'API Servizi Desktop remoto.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117799"
---
# <a name="remote-desktop-services-api-structures"></a><span data-ttu-id="a98ec-103">Strutture API Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="a98ec-103">Remote Desktop Services API Structures</span></span>

<span data-ttu-id="a98ec-104">Con l'API Servizi Desktop remoto vengono utilizzate le strutture seguenti.</span><span class="sxs-lookup"><span data-stu-id="a98ec-104">The following structures are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a98ec-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a98ec-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a98ec-106">**\_def canale**</span><span class="sxs-lookup"><span data-stu-id="a98ec-106">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

<span data-ttu-id="a98ec-107">Contiene il nome e le opzioni di un canale virtuale Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-107">Contains the name and options of a Remote Desktop Services virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-108">**\_punti di ingresso del canale \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-108">**CHANNEL\_ENTRY\_POINTS**</span></span>](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

<span data-ttu-id="a98ec-109">Contiene i puntatori alle funzioni chiamate da una DLL sul lato client per accedere ai canali virtuali.</span><span class="sxs-lookup"><span data-stu-id="a98ec-109">Contains pointers to the functions called by a client-side DLL to access virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-110">**\_intestazione PDU del canale \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-110">**CHANNEL\_PDU\_HEADER**</span></span>](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

<span data-ttu-id="a98ec-111">Contiene informazioni su un blocco di dati ricevuto dall'entità finale del server di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="a98ec-111">Contains information about a data block being received by the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-112">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="a98ec-112">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dd>

<span data-ttu-id="a98ec-113">Contiene informazioni su un Key Pack di gestione licenze Servizi Desktop remoto specifico.</span><span class="sxs-lookup"><span data-stu-id="a98ec-113">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-114">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="a98ec-114">**LSLicense**</span></span>](lslicense.md)
</dt> <dd>

<span data-ttu-id="a98ec-115">Contiene informazioni su una licenza di Servizi Desktop remoto specifica.</span><span class="sxs-lookup"><span data-stu-id="a98ec-115">Contains information about a specific Remote Desktop Services license.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-116">**WTSCLIENT**</span><span class="sxs-lookup"><span data-stu-id="a98ec-116">**WTSCLIENT**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

<span data-ttu-id="a98ec-117">Contiene informazioni su un client Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="a98ec-117">Contains information about a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-118">**WTSCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="a98ec-118">**WTSCONFIGINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

<span data-ttu-id="a98ec-119">Contiene informazioni su una sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-119">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-120">**WTSINFO**</span><span class="sxs-lookup"><span data-stu-id="a98ec-120">**WTSINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

<span data-ttu-id="a98ec-121">Contiene informazioni su una sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-121">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-122">**WTSINFOEX**</span><span class="sxs-lookup"><span data-stu-id="a98ec-122">**WTSINFOEX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

<span data-ttu-id="a98ec-123">Contiene un'Unione a [**\_ livello di WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) che contiene informazioni estese su una sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-123">Contains a [**WTSINFOEX\_LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) union that contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-124">**\_Level1 WTSINFOEX**</span><span class="sxs-lookup"><span data-stu-id="a98ec-124">**WTSINFOEX\_LEVEL1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

<span data-ttu-id="a98ec-125">Contiene informazioni estese su una sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-125">Contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-126">**WTSLISTENERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="a98ec-126">**WTSLISTENERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

<span data-ttu-id="a98ec-127">Contiene informazioni su un listener di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-127">Contains information about a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-128">**\_indirizzo IP \_ WTSSBX**</span><span class="sxs-lookup"><span data-stu-id="a98ec-128">**WTSSBX\_IP\_ADDRESS**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

<span data-ttu-id="a98ec-129">Contiene informazioni sull'indirizzo IP di una risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="a98ec-129">Contains information about the IP address of a network resource.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-130">**\_informazioni sulla \_ connessione del computer WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-130">**WTSSBX\_MACHINE\_CONNECT\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

<span data-ttu-id="a98ec-131">Contiene informazioni su un computer che accetta connessioni remote.</span><span class="sxs-lookup"><span data-stu-id="a98ec-131">Contains information about a computer that is accepting remote connections.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-132">**\_informazioni sul computer WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-132">**WTSSBX\_MACHINE\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

<span data-ttu-id="a98ec-133">Contiene informazioni su un computer e il relativo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="a98ec-133">Contains information about a computer and its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-134">**\_informazioni sulla sessione WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-134">**WTSSBX\_SESSION\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

<span data-ttu-id="a98ec-135">Sono incluse informazioni sulle sessioni disponibili per Connessione Desktop remoto broker (gestore connessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="a98ec-135">Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-136">**\_notifica WTSSESSION**</span><span class="sxs-lookup"><span data-stu-id="a98ec-136">**WTSSESSION\_NOTIFICATION**</span></span>](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

<span data-ttu-id="a98ec-137">Fornisce informazioni sulla notifica di modifica della sessione.</span><span class="sxs-lookup"><span data-stu-id="a98ec-137">Provides information about the session change notification.</span></span> <span data-ttu-id="a98ec-138">Un servizio riceve questa struttura nella relativa funzione [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) in risposta a un evento di modifica della sessione.</span><span class="sxs-lookup"><span data-stu-id="a98ec-138">A service receives this structure in its [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function in response to a session change event.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-139">**WTSUSERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="a98ec-139">**WTSUSERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

<span data-ttu-id="a98ec-140">Contiene le informazioni di configurazione per un utente in un controller di dominio o in un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="a98ec-140">Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-141">**\_Indirizzo client \_ WTS**</span><span class="sxs-lookup"><span data-stu-id="a98ec-141">**WTS\_CLIENT\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

<span data-ttu-id="a98ec-142">Contiene l'indirizzo di rete del client di una sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-142">Contains the client network address of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-143">**\_visualizzazione client \_ WTS**</span><span class="sxs-lookup"><span data-stu-id="a98ec-143">**WTS\_CLIENT\_DISPLAY**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

<span data-ttu-id="a98ec-144">Contiene informazioni sulla visualizzazione di un client Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="a98ec-144">Contains information about the display of a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-145">**\_informazioni sul processo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-145">**WTS\_PROCESS\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

<span data-ttu-id="a98ec-146">Contiene informazioni su un processo in esecuzione in un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-146">Contains information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-147">**\_informazioni sul processo WTS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-147">**WTS\_PROCESS\_INFO\_EX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

<span data-ttu-id="a98ec-148">Contiene informazioni estese su un processo in esecuzione in un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-148">Contains extended information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="a98ec-149">[**\_informazioni sul prodotto WTS \_**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="a98ec-149">[**WTS\_PRODUCT\_INFO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span></span>
</dt> <dd>

<span data-ttu-id="a98ec-150">Dettagli della licenza del prodotto necessaria per la connessione a un server terminal.</span><span class="sxs-lookup"><span data-stu-id="a98ec-150">The details of the product license that is required to connect to a terminal server.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-151">**\_informazioni sul server WTS \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-151">**WTS\_SERVER\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

<span data-ttu-id="a98ec-152">Contiene informazioni su un server di Servizi Desktop remoto specifico.</span><span class="sxs-lookup"><span data-stu-id="a98ec-152">Contains information about a specific Remote Desktop Services server.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-153">**\_indirizzo della sessione WTS \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-153">**WTS\_SESSION\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

<span data-ttu-id="a98ec-154">Contiene l'indirizzo IP virtuale assegnato a una sessione.</span><span class="sxs-lookup"><span data-stu-id="a98ec-154">Contains the virtual IP address assigned to a session.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-155">**\_informazioni sulla sessione WTS \_**</span><span class="sxs-lookup"><span data-stu-id="a98ec-155">**WTS\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

<span data-ttu-id="a98ec-156">Contiene informazioni su una sessione client in un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="a98ec-156">Contains information about a client session on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="a98ec-157">**\_Informazioni sulla sessione WTS \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a98ec-157">**WTS\_SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

<span data-ttu-id="a98ec-158">Contiene informazioni estese su una sessione client in un server Host sessione Desktop remoto o in un server Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="a98ec-158">Contains extended information about a client session on a RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> </dl>

 

 