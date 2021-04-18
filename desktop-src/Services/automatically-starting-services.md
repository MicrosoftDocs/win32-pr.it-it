---
description: Durante l'avvio del sistema, SCM avvia tutti i servizi di avvio automatico e i servizi da cui dipendono. Se, ad esempio, un servizio di avvio automatico dipende da un servizio di avvio a richiesta, viene avviato automaticamente anche il servizio di avvio a richiesta.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Avvio automatico dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306340"
---
# <a name="automatically-starting-services"></a><span data-ttu-id="a2a58-104">Avvio automatico dei servizi</span><span class="sxs-lookup"><span data-stu-id="a2a58-104">Automatically Starting Services</span></span>

<span data-ttu-id="a2a58-105">Durante l'avvio del sistema, SCM avvia tutti i servizi di avvio automatico e i servizi da cui dipendono.</span><span class="sxs-lookup"><span data-stu-id="a2a58-105">During system boot, the SCM starts all auto-start services and the services on which they depend.</span></span> <span data-ttu-id="a2a58-106">Se, ad esempio, un servizio di avvio automatico dipende da un servizio di avvio a richiesta, viene avviato automaticamente anche il servizio di avvio a richiesta.</span><span class="sxs-lookup"><span data-stu-id="a2a58-106">For example, if an auto-start service depends on a demand-start service, the demand-start service is also started automatically.</span></span>

<span data-ttu-id="a2a58-107">L'ordine di caricamento è determinato dai seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="a2a58-107">The load order is determined by the following:</span></span>

1.  <span data-ttu-id="a2a58-108">Ordine dei gruppi nell'elenco del gruppo di ordini di caricamento.</span><span class="sxs-lookup"><span data-stu-id="a2a58-108">The order of groups in the load ordering group list.</span></span> <span data-ttu-id="a2a58-109">Queste informazioni vengono archiviate nel valore **ServiceGroupOrder** nella seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="a2a58-109">This information is stored in the **ServiceGroupOrder** value in the following registry key:</span></span>

    <span data-ttu-id="a2a58-110">**\_ \_ \\ Controllo CurrentControlSet del sistema del computer \\ locale \\ HKEY**</span><span class="sxs-lookup"><span data-stu-id="a2a58-110">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

    <span data-ttu-id="a2a58-111">Per specificare il gruppo di ordini di caricamento per un servizio, usare il parametro *lpLoadOrderGroup* della funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="a2a58-111">To specify the load ordering group for a service, use the *lpLoadOrderGroup* parameter of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) or [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function.</span></span>

2.  <span data-ttu-id="a2a58-112">Ordine dei servizi all'interno di un gruppo specificato nel vettore di ordine dei tag.</span><span class="sxs-lookup"><span data-stu-id="a2a58-112">The order of services within a group specified in the tags order vector.</span></span> <span data-ttu-id="a2a58-113">Queste informazioni vengono archiviate nel valore **GroupOrderList** nella seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="a2a58-113">This information is stored in the **GroupOrderList** value in the following registry key:</span></span>

    <span data-ttu-id="a2a58-114">**\_ \_ \\ Controllo CurrentControlSet del sistema del computer \\ locale \\ HKEY**</span><span class="sxs-lookup"><span data-stu-id="a2a58-114">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

3.  <span data-ttu-id="a2a58-115">Le dipendenze elencate per ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="a2a58-115">The dependencies listed for each service.</span></span>

<span data-ttu-id="a2a58-116">Al termine dell'avvio, il sistema esegue il programma di verifica dell'avvio specificato dal valore **BootVerificationProgram** della chiave del registro di sistema seguente: **HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control**.</span><span class="sxs-lookup"><span data-stu-id="a2a58-116">When the boot is complete, the system executes the boot verification program specified by the **BootVerificationProgram** value of the following registry key: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control**.</span></span>

<span data-ttu-id="a2a58-117">Per impostazione predefinita, questo valore non è impostato.</span><span class="sxs-lookup"><span data-stu-id="a2a58-117">By default, this value is not set.</span></span> <span data-ttu-id="a2a58-118">Il sistema segnala semplicemente che l'avvio ha avuto esito positivo dopo che il primo utente ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="a2a58-118">The system simply reports that the boot was successful after the first user has logged on.</span></span> <span data-ttu-id="a2a58-119">È possibile fornire un programma di verifica di avvio che controlla la presenza di problemi nel sistema e segnala lo stato di avvio a SCM tramite la funzione [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="a2a58-119">You can supply a boot verification program that checks the system for problems and reports the boot status to the SCM using the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>

<span data-ttu-id="a2a58-120">Al termine dell'avvio, il sistema salva un clone del database nell'ultima configurazione (ultima) corretta.</span><span class="sxs-lookup"><span data-stu-id="a2a58-120">After a successful boot, the system saves a clone of the database in the last-known-good (LKG) configuration.</span></span> <span data-ttu-id="a2a58-121">Il sistema può ripristinare questa copia del database se le modifiche apportate al database attivo provocano un errore del riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="a2a58-121">The system can restore this copy of the database if changes made to the active database cause the system reboot to fail.</span></span> <span data-ttu-id="a2a58-122">Di seguito è riportata la chiave del registro di sistema per il database:</span><span class="sxs-lookup"><span data-stu-id="a2a58-122">The following is the registry key for this database:</span></span>

<span data-ttu-id="a2a58-123">**HKEY \_ \_ servizi di controllo di sistema del computer locale \\ \\ *xxx* \\**</span><span class="sxs-lookup"><span data-stu-id="a2a58-123">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\ControlSet *XXX*\\Services**</span></span>

<span data-ttu-id="a2a58-124">dove *xxx* è il valore salvato nel seguente valore del registro di **sistema: HKEY \_ Local \_ computer \\ System \\ Select \\ LastKnownGood**.</span><span class="sxs-lookup"><span data-stu-id="a2a58-124">where *XXX* is the value saved in the following registry value: **HKEY\_LOCAL\_MACHINE\\System\\Select\\LastKnownGood**.</span></span>

<span data-ttu-id="a2a58-125">Se un servizio di avvio automatico con \_ errore critico del servizio \_ non viene avviato, il controllo SCM riavvia il computer utilizzando la configurazione ultima.</span><span class="sxs-lookup"><span data-stu-id="a2a58-125">If an auto-start service with a SERVICE\_ERROR\_CRITICAL error control level fails to start, the SCM reboots the computer using the LKG configuration.</span></span> <span data-ttu-id="a2a58-126">Se la configurazione ultima è già in uso, l'avvio ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a2a58-126">If the LKG configuration is already being used, the boot fails.</span></span>

<span data-ttu-id="a2a58-127">Un servizio di avvio automatico può essere configurato come servizio di avvio automatico ritardato chiamando la funzione [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) con le \_ informazioni di \_ avvio automatico ritardato della configurazione del servizio \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a2a58-127">An auto-start service can be configured as a delayed auto-start service by calling the [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function with SERVICE\_CONFIG\_DELAYED\_AUTO\_START\_INFO.</span></span> <span data-ttu-id="a2a58-128">Questa modifica viene applicata dopo l'avvio del sistema successivo.</span><span class="sxs-lookup"><span data-stu-id="a2a58-128">This change takes effect after the next system boot.</span></span> <span data-ttu-id="a2a58-129">Per altre informazioni, vedere [**\_ informazioni sull' \_ \_ avvio automatico \_ ritardato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span><span class="sxs-lookup"><span data-stu-id="a2a58-129">For more information, see [**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span></span>

 

 



