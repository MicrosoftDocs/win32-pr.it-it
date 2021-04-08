---
title: Gestione riavvio
description: Scrivere programmi di installazione personalizzati per eliminare i riavvii del sistema necessari per completare l'aggiornamento di un file in uso. Arrestare e riavviare tutti i servizi di sistema, ma non critici, dai programmi.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Gestione riavvio riavvio gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047081"
---
# <a name="restart-manager"></a><span data-ttu-id="189a4-105">Gestione riavvio</span><span class="sxs-lookup"><span data-stu-id="189a4-105">Restart Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="189a4-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="189a4-106">Purpose</span></span>

<span data-ttu-id="189a4-107">L'API di gestione riavvio può eliminare o ridurre il numero di riavvii del sistema necessari per completare un'installazione o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="189a4-107">The Restart Manager API can eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span> <span data-ttu-id="189a4-108">Il motivo principale per cui gli aggiornamenti software richiedono un riavvio del sistema durante un'installazione o un aggiornamento è che alcuni dei file che vengono aggiornati vengono attualmente utilizzati da un'applicazione o da un servizio in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="189a4-108">The primary reason software updates require a system restart during an installation or update is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="189a4-109">Gestione riavvio consente di arrestare e riavviare tutti i [servizi di sistema](critical-system-services.md) , tranne quelli critici.</span><span class="sxs-lookup"><span data-stu-id="189a4-109">The Restart Manager enables all but the [critical system services](critical-system-services.md) to be shut down and restarted.</span></span> <span data-ttu-id="189a4-110">Consente di liberare i file in uso e di completare le operazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="189a4-110">This frees files that are in use and allows installation operations to complete.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="189a4-111">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="189a4-111">Where applicable</span></span>

<span data-ttu-id="189a4-112">La DLL di gestione riavvio Esporta un'interfaccia C pubblica che può essere caricata da programmi di installazione standard o personalizzati.</span><span class="sxs-lookup"><span data-stu-id="189a4-112">The Restart Manager DLL exports a public C interface that can be loaded by standard or custom installers.</span></span> <span data-ttu-id="189a4-113">Il programma di installazione può usare Gestione riavvio per registrare i file che devono essere sostituiti durante l'installazione di un'applicazione o di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="189a4-113">The installer can use the Restart Manager to register files that should be replaced during the installation of an application or update.</span></span> <span data-ttu-id="189a4-114">Quindi, durante un aggiornamento o un'installazione successiva, il programma di installazione può usare Gestione riavvio per determinare quali file non possono essere aggiornati perché sono attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="189a4-114">Then during a subsequent update or installation, the installer can use the Restart Manager to determine which files cannot be updated because they are currently in use.</span></span> <span data-ttu-id="189a4-115">Gestione riavvio può arrestare e riavviare i servizi o le applicazioni non critiche che attualmente utilizzano tali file.</span><span class="sxs-lookup"><span data-stu-id="189a4-115">Restart Manager can shut down and restart the non-critical services or applications that are currently using those files.</span></span> <span data-ttu-id="189a4-116">I programmi di installazione possono indirizzare Gestione riavvio per arrestare e riavviare le applicazioni o i servizi in base al file in uso, l'ID processo (PID) o il nome breve di un servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="189a4-116">Installers can direct the Restart Manager to shut down and restart applications or services based on the file in use, the process ID (PID), or the short-name of a Windows service.</span></span>

<span data-ttu-id="189a4-117">Gestione riavvio è progettato per lo sviluppo di applicazioni di tipo desktop.</span><span class="sxs-lookup"><span data-stu-id="189a4-117">Restart Manager is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="189a4-118">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="189a4-118">Developer audience</span></span>

<span data-ttu-id="189a4-119">Questa documentazione è destinata agli sviluppatori di applicazioni di installazione che desiderano sfruttare le funzionalità del programma di installazione di Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="189a4-119">This documentation is intended for developers of installation applications who want to take advantage of the installer capabilities in Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="189a4-120">Le applicazioni che usano la versione di [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4,0 per l'installazione e la manutenzione utilizzano automaticamente Gestione riavvio per ridurre i riavvii del sistema.</span><span class="sxs-lookup"><span data-stu-id="189a4-120">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="189a4-121">I programmi di installazione personalizzati possono anche essere progettati per chiamare l'API di gestione riavvio per arrestare e riavviare le applicazioni e i servizi.</span><span class="sxs-lookup"><span data-stu-id="189a4-121">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="189a4-122">Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare l'API di gestione riavvio per pianificare i riavvii in modo da ridurre al minimo l'alterazione del flusso di lavoro dell'utente.</span><span class="sxs-lookup"><span data-stu-id="189a4-122">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="189a4-123">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="189a4-123">Run-time requirements</span></span>

<span data-ttu-id="189a4-124">L'API Gestione riavvio è disponibile a partire da Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="189a4-124">The Restart Manager API is available beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="189a4-125">Gestione riavvio è costituito da una singola DLL che le applicazioni possono caricare per accedere all'API di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="189a4-125">Restart Manager consists of a single DLL that applications can load to access the Restart Manager API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="189a4-126">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="189a4-126">In this section</span></span>



| <span data-ttu-id="189a4-127">Argomento</span><span class="sxs-lookup"><span data-stu-id="189a4-127">Topic</span></span>                                                                 | <span data-ttu-id="189a4-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="189a4-128">Description</span></span>                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="189a4-129">Informazioni su Gestione riavvio</span><span class="sxs-lookup"><span data-stu-id="189a4-129">About Restart Manager</span></span>](about-restart-manager.md)<br/>         | <span data-ttu-id="189a4-130">Argomenti introduttivi che descrivono Gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="189a4-130">Overview topics that describe the Restart Manager.</span></span><br/>   |
| [<span data-ttu-id="189a4-131">Utilizzo di gestione riavvio</span><span class="sxs-lookup"><span data-stu-id="189a4-131">Using Restart Manager</span></span>](using-restart-manager.md)<br/>         | <span data-ttu-id="189a4-132">Argomenti introduttivi sull'uso dell'API Gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="189a4-132">Overview topics about using the Restart Manager API.</span></span><br/> |
| [<span data-ttu-id="189a4-133">Riferimento a gestione riavvio</span><span class="sxs-lookup"><span data-stu-id="189a4-133">Restart Manager Reference</span></span>](restart-manager-reference.md)<br/> | <span data-ttu-id="189a4-134">Argomenti di riferimento per l'API di gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="189a4-134">Reference topics for the Restart Manager API.</span></span><br/>        |



 

 

