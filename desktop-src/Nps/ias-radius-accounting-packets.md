---
title: Registrazione con server dei criteri di rete
description: Registrazione con server dei criteri di rete
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338414"
---
# <a name="logging-with-network-policy-server"></a><span data-ttu-id="4e6f3-103">Registrazione con server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="4e6f3-103">Logging With Network Policy Server</span></span>

> [!Note]  
> <span data-ttu-id="4e6f3-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="4e6f3-105">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="4e6f3-106">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="4e6f3-107">Nella tabella seguente vengono descritti solo gli aspetti più importanti dei pacchetti di accounting RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-107">The following table describes only the most important aspects of the RADIUS accounting packets.</span></span> <span data-ttu-id="4e6f3-108">Il documento sulla richiesta di contabilità RADIUS ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) fornisce informazioni dettagliate su questi pacchetti.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-108">The RADIUS Accounting Request for Comments document ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) provides detailed information on these packets.</span></span>

<span data-ttu-id="4e6f3-109">I pacchetti di accounting RADIUS possono essere divisi nelle categorie seguenti.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-109">RADIUS accounting packets can be divided into the following categories.</span></span>



| <span data-ttu-id="4e6f3-110">Pacchetto di contabilità</span><span class="sxs-lookup"><span data-stu-id="4e6f3-110">Accounting packet</span></span>  | <span data-ttu-id="4e6f3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e6f3-111">Description</span></span>                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6f3-112">Accounting-On</span><span class="sxs-lookup"><span data-stu-id="4e6f3-112">Accounting-On</span></span>      | <span data-ttu-id="4e6f3-113">Inviato dal server di accesso alla rete (NAS) per indicare che è stato riavviato.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-113">Sent by the Network Access Server (NAS) to indicate that it has restarted.</span></span><br/> <span data-ttu-id="4e6f3-114">Contiene l'identificatore NAS/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-114">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                        |
| <span data-ttu-id="4e6f3-115">Accounting-Off</span><span class="sxs-lookup"><span data-stu-id="4e6f3-115">Accounting-Off</span></span>     | <span data-ttu-id="4e6f3-116">Inviato dal NAS per indicare che è in fase di arresto.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-116">Sent by the NAS to indicate that it is being shutdown.</span></span><br/> <span data-ttu-id="4e6f3-117">Contiene l'identificatore NAS/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-117">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                                            |
| <span data-ttu-id="4e6f3-118">Accounting-Start</span><span class="sxs-lookup"><span data-stu-id="4e6f3-118">Accounting-Start</span></span>   | <span data-ttu-id="4e6f3-119">Inviato dal NAS, dopo che l'utente è stato autenticato e autorizzato, per indicare l'inizio di una sessione utente.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-119">Sent by the NAS, after the user was authenticated and authorized, to indicate the start of a user session.</span></span> <br/> <span data-ttu-id="4e6f3-120">Contiene userid, NAS-Identifier/IPAddress, oltre ad altre informazioni ricevute dal NAS.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-120">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/> |
| <span data-ttu-id="4e6f3-121">Accounting-Stop</span><span class="sxs-lookup"><span data-stu-id="4e6f3-121">Accounting-Stop</span></span>    | <span data-ttu-id="4e6f3-122">Inviato dal NAS per indicare la fine di una sessione utente.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-122">Sent by the NAS to indicate the end of a user session.</span></span><br/> <span data-ttu-id="4e6f3-123">Contiene userid, NAS-Identifier/IPAddress, oltre ad altre informazioni ricevute dal NAS.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-123">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/>                                                      |
| <span data-ttu-id="4e6f3-124">Accounting-Interim</span><span class="sxs-lookup"><span data-stu-id="4e6f3-124">Accounting-Interim</span></span> | <span data-ttu-id="4e6f3-125">Potrebbe essere inviato periodicamente dal NAS per ogni utente che ha eseguito l'accesso al server NAS.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-125">Could be sent periodically by the NAS for each user that is logged on at the NAS.</span></span> <br/> <span data-ttu-id="4e6f3-126">Questa funzionalità è in genere supportata nelle versioni più recenti del server NAS.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-126">This feature is generally supported in newer versions of NAS.</span></span><br/>                                                     |



 

<span data-ttu-id="4e6f3-127">I problemi seguenti sono importanti da considerare quando si raccolgono le informazioni di contabilità rese disponibili tramite RADIUS:</span><span class="sxs-lookup"><span data-stu-id="4e6f3-127">The following issues are important to consider when collecting accounting information made available through RADIUS:</span></span>

-   <span data-ttu-id="4e6f3-128">In rari casi, è possibile che i pacchetti vengano persi durante la trasmissione e che non raggiungano mai il server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-128">In rare cases, packets could be lost during transmission and may never reach the RADIUS server.</span></span>
-   <span data-ttu-id="4e6f3-129">Il server RADIUS non riceve alcuna notifica se il NAS viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-129">The RADIUS server is not notified if the NAS aborts.</span></span>
-   <span data-ttu-id="4e6f3-130">ISDN supporta più sessioni e ogni sessione genera una coppia di pacchetti Accounting-Start/Stop.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-130">ISDN supports multiple sessions and each session generates an Accounting-Start/-Stop pair of packets.</span></span> <span data-ttu-id="4e6f3-131">È presente un attributo contabilità denominato identificatore a più sessioni che identifica chiaramente tali pacchetti multisessione.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-131">There is an accounting attribute called multi-session identifier that clearly identifies such multi-session packets.</span></span> <span data-ttu-id="4e6f3-132">Verificare l'identificatore di più sessioni oltre all'identificatore di sessione per calcolare il numero di sessioni.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-132">Check for the multi-session identifier in addition to the session identifier to calculate the number of sessions.</span></span>

## <a name="requests-logged-by-nps"></a><span data-ttu-id="4e6f3-133">Richieste registrate da server dei criteri di server</span><span class="sxs-lookup"><span data-stu-id="4e6f3-133">Requests Logged by NPS</span></span>

<span data-ttu-id="4e6f3-134">Per impostazione predefinita, NPS non registra i dati.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-134">By default, NPS does not log any data.</span></span> <span data-ttu-id="4e6f3-135">Il server dei criteri di accesso può essere configurato tramite l'interfaccia utente NPS (NPS. msc) per registrare le richieste seguenti.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-135">NPS can be configured, using the NPS user interface (nps.msc), to log the following requests.</span></span>



| <span data-ttu-id="4e6f3-136">Pacchetto registrato</span><span class="sxs-lookup"><span data-stu-id="4e6f3-136">Logged packet</span></span>          | <span data-ttu-id="4e6f3-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e6f3-137">Description</span></span>                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6f3-138">Richiesta accounting</span><span class="sxs-lookup"><span data-stu-id="4e6f3-138">Accounting Request</span></span>     | <span data-ttu-id="4e6f3-139">Tutti i pacchetti di contabilità descritti nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-139">Any of the accounting packets described in the previous table.</span></span><br/>                                                                    |
| <span data-ttu-id="4e6f3-140">Richiesta di autenticazione</span><span class="sxs-lookup"><span data-stu-id="4e6f3-140">Authentication Request</span></span> | <span data-ttu-id="4e6f3-141">Inviato dal NAS per conto dell'utente che si connette.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-141">Sent by the NAS on behalf of the connecting user.</span></span><br/> <span data-ttu-id="4e6f3-142">Le voci di log contengono solo attributi in ingresso.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-142">The log entries contain only incoming attributes.</span></span><br/>                    |
| <span data-ttu-id="4e6f3-143">Accettazione autenticazione</span><span class="sxs-lookup"><span data-stu-id="4e6f3-143">Authentication Accept</span></span>  | <span data-ttu-id="4e6f3-144">Inviato da NPS per indicare che la connessione utente deve essere accettata.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-144">Sent by NPS to indicate that the user connection should be accepted.</span></span><br/> <span data-ttu-id="4e6f3-145">Le voci di log contengono solo attributi in uscita.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-145">The log entries contain only outgoing attributes.</span></span><br/> |
| <span data-ttu-id="4e6f3-146">Rifiuto autenticazione</span><span class="sxs-lookup"><span data-stu-id="4e6f3-146">Authentication Reject</span></span>  | <span data-ttu-id="4e6f3-147">Inviato da NPS per indicare che la connessione utente deve essere rifiutata.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-147">Sent by NPS to indicate that the user connection should be rejected.</span></span><br/> <span data-ttu-id="4e6f3-148">Le voci di log contengono solo attributi in uscita.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-148">The log entries contain only outgoing attributes.</span></span><br/> |



 

<span data-ttu-id="4e6f3-149">I dati registrati da NPS possono accedere a un file di testo nel server NPS o a un database SQL centrale.</span><span class="sxs-lookup"><span data-stu-id="4e6f3-149">Data logged by NPS can go to a text file on the NPS server or to a central SQL database.</span></span> <span data-ttu-id="4e6f3-150">Per ulteriori informazioni sulla registrazione di NPS SQL, vedere [programmabilità SQL](sql-programmability.md).</span><span class="sxs-lookup"><span data-stu-id="4e6f3-150">For more information on NPS SQL logging, see [SQL Programmability](sql-programmability.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e6f3-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e6f3-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e6f3-152">Servizio di autenticazione Internet e server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="4e6f3-152">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="4e6f3-153">Autenticazione, autorizzazione e accounting RADIUS</span><span class="sxs-lookup"><span data-stu-id="4e6f3-153">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="4e6f3-154">Utilizzo di un server di stato</span><span class="sxs-lookup"><span data-stu-id="4e6f3-154">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

