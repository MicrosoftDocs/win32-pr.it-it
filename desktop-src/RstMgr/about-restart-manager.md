---
title: Informazioni su Gestione riavvio
description: Il motivo principale per cui l'installazione e gli aggiornamenti del software richiede un riavvio del sistema è che alcuni dei file da aggiornare sono attualmente utilizzati da un'applicazione o da un servizio in esecuzione.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Riavviare Gestione riavvio gestione, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1cfd300d554e311ab43cc0a9413514b6b60081
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729575"
---
# <a name="about-restart-manager"></a><span data-ttu-id="4b597-104">Informazioni su Gestione riavvio</span><span class="sxs-lookup"><span data-stu-id="4b597-104">About Restart Manager</span></span>

<span data-ttu-id="4b597-105">Il motivo principale per cui l'installazione e gli aggiornamenti del software richiede un riavvio del sistema è che alcuni dei file da aggiornare sono attualmente utilizzati da un'applicazione o da un servizio in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4b597-105">The primary reason software installation and updates require a system restart is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="4b597-106">Gestione riavvio consente l'arresto e il riavvio di tutti i servizi e delle applicazioni critiche.</span><span class="sxs-lookup"><span data-stu-id="4b597-106">Restart Manager enables all but the critical applications and services to be shut down and restarted .</span></span> <span data-ttu-id="4b597-107">Ciò consente di liberare i file in uso e di completare le operazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="4b597-107">This frees the files that are in use and allows installation operations to complete.</span></span> <span data-ttu-id="4b597-108">Consente inoltre di eliminare o ridurre il numero di riavvii del sistema necessari per completare un'installazione o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4b597-108">It can also eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span>

<span data-ttu-id="4b597-109">Gestione riavvio interrompe le applicazioni nell'ordine seguente e, dopo l'aggiornamento delle applicazioni, riavvia le applicazioni che sono state registrate per il riavvio in ordine inverso.</span><span class="sxs-lookup"><span data-stu-id="4b597-109">The Restart Manager stops applications in the following order, and after the applications have been updated, restarts applications that have been registered for restart in the reverse order.</span></span>

1.  <span data-ttu-id="4b597-110">Applicazioni GUI</span><span class="sxs-lookup"><span data-stu-id="4b597-110">GUI applications</span></span>
2.  <span data-ttu-id="4b597-111">Applicazioni console</span><span class="sxs-lookup"><span data-stu-id="4b597-111">Console applications</span></span>
3.  <span data-ttu-id="4b597-112">Servizi Windows</span><span class="sxs-lookup"><span data-stu-id="4b597-112">Windows services</span></span>
4.  <span data-ttu-id="4b597-113">Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="4b597-113">Windows explorer</span></span>

<span data-ttu-id="4b597-114">Gestione riavvio arresta l'applicazione o i servizi solo se il chiamante dispone delle autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="4b597-114">Restart Manager shuts down application or services only if the caller has permission to do so.</span></span> <span data-ttu-id="4b597-115">Si noti che l'arresto tra le sessioni non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4b597-115">Note that shutdown across sessions is not supported.</span></span>

<span data-ttu-id="4b597-116">Le applicazioni che usano la versione di [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4,0 per l'installazione e la manutenzione utilizzano automaticamente Gestione riavvio per ridurre i riavvii del sistema.</span><span class="sxs-lookup"><span data-stu-id="4b597-116">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="4b597-117">I programmi di installazione personalizzati possono anche essere progettati per chiamare l'API di gestione riavvio per arrestare e riavviare le applicazioni e i servizi.</span><span class="sxs-lookup"><span data-stu-id="4b597-117">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="4b597-118">Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare l'API di gestione riavvio per pianificare i riavvii in modo da ridurre al minimo l'alterazione del flusso di lavoro dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4b597-118">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

<span data-ttu-id="4b597-119">Per informazioni sull'uso dell'API Gestione riavvio durante l'installazione e gli aggiornamenti, vedere [uso di gestione riavvio](using-restart-manager.md).</span><span class="sxs-lookup"><span data-stu-id="4b597-119">For information about using the Restart Manager API during installation and updates, see [Using Restart Manager](using-restart-manager.md).</span></span>

<span data-ttu-id="4b597-120">I servizi di sistema critici non possono essere arrestati e riavviati da Gestione riavvio senza riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="4b597-120">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="4b597-121">Per ulteriori informazioni sull'identificazione dei servizi di sistema critici, vedere [Critical System Services](critical-system-services.md).</span><span class="sxs-lookup"><span data-stu-id="4b597-121">For more information about identifying critical system services, see [Critical System Services](critical-system-services.md).</span></span>

<span data-ttu-id="4b597-122">Le applicazioni e i servizi devono essere preparati per essere arrestati da Gestione riavvio e salvare i dati utente e le informazioni sullo stato necessarie per un riavvio pulito.</span><span class="sxs-lookup"><span data-stu-id="4b597-122">Your applications and services should be prepared to be shut down by the Restart Manager and save user data and state information that are needed for a clean restart.</span></span> <span data-ttu-id="4b597-123">Per ulteriori informazioni su come preparare le applicazioni e i servizi in modo che funzionino con Gestione riavvio, vedere [linee guida per le applicazioni e i servizi](guidelines-for-applications-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="4b597-123">For more information about how to prepare your applications and services to work with the Restart Manager, see [Guidelines for Applications and Services](guidelines-for-applications-and-services.md).</span></span>

<span data-ttu-id="4b597-124">Per informazioni di riferimento sulle enumerazioni, le strutture e le funzioni dell'API di gestione riavvio, vedere la sezione [riferimento a gestione riavvio](restart-manager-reference.md)</span><span class="sxs-lookup"><span data-stu-id="4b597-124">For reference information about the enumerations, structures, and functions of the Restart Manager API, see the [Restart Manager Reference](restart-manager-reference.md) section</span></span>

 

 