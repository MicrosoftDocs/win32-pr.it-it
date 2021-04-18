---
description: Un pacchetto di notifica Winlogon è una DLL che esporta funzioni che gestiscono gli eventi Winlogon. Ad esempio, quando un utente accede al sistema, Winlogon chiama ogni funzione del gestore eventi di accesso del pacchetto di notifica per fornire informazioni sull'evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Creazione di un pacchetto di notifica Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311941"
---
# <a name="creating-a-winlogon-notification-package"></a><span data-ttu-id="ed2a5-104">Creazione di un pacchetto di notifica Winlogon</span><span class="sxs-lookup"><span data-stu-id="ed2a5-104">Creating a Winlogon Notification Package</span></span>

<span data-ttu-id="ed2a5-105">Un pacchetto di notifica [*Winlogon*](/windows/desktop/SecGloss/w-gly) è una dll che esporta funzioni che gestiscono gli eventi Winlogon.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-105">A [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="ed2a5-106">Ad esempio, quando un utente accede al sistema, Winlogon chiama ogni funzione del gestore eventi di accesso del pacchetto di notifica per fornire informazioni sull'evento.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-106">For example, when a user logs onto the system, Winlogon calls each notification package's logon event handler function to provide information about the event.</span></span>

<span data-ttu-id="ed2a5-107">I nomi delle funzioni del gestore eventi implementati in un pacchetto di notifica vengono lasciati allo sviluppatore; Winlogon controlla il registro di sistema per ottenere i nomi delle funzioni del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-107">The names of the event handler functions implemented in a notification package are left up to the developer; Winlogon checks the registry to obtain the names of the event handler functions.</span></span> <span data-ttu-id="ed2a5-108">Ad esempio, un pacchetto di notifica può implementare la funzione del gestore eventi di accesso come se `WLEventLogon` fosse un altro a usare `HandleLogonEvent` .</span><span class="sxs-lookup"><span data-stu-id="ed2a5-108">For example, one notification package might implement the logon event handler function as `WLEventLogon` whereas another might use `HandleLogonEvent`.</span></span>

<span data-ttu-id="ed2a5-109">Non è necessario implementare e registrare i gestori eventi per ogni evento Winlogon, solo per gli eventi che risultano utili per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-109">You do not have to implement and register event handlers for every Winlogon event, only for events that are useful to your application.</span></span> <span data-ttu-id="ed2a5-110">Ogni funzione del gestore eventi deve usare il prototipo di funzione descritto nel [prototipo di funzione del gestore eventi](event-handler-function-prototype.md).</span><span class="sxs-lookup"><span data-stu-id="ed2a5-110">Each event handler function must use the function prototype described in [Event Handler Function Prototype](event-handler-function-prototype.md).</span></span> <span data-ttu-id="ed2a5-111">Questo prototipo ha un solo parametro: una struttura di [**\_ \_ informazioni di notifica di WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) che contiene i dettagli sull'evento.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-111">This prototype has a single parameter: a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains details about the event.</span></span>

<span data-ttu-id="ed2a5-112">Winlogon ignora l'output delle funzioni del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-112">Winlogon ignores the output of event handler functions.</span></span> <span data-ttu-id="ed2a5-113">Se la gestione di un evento richiede l'interazione con Winlogon, usare le [funzioni di supporto di Winlogon](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ed2a5-113">If handling an event requires interacting with Winlogon, use the [Winlogon Support Functions](authentication-functions.md).</span></span>

<span data-ttu-id="ed2a5-114">Per usare il pacchetto di notifiche Winlogon, la DLL deve essere copiata nella cartella% SystemRoot% \\ system32 ed è necessario eseguire un aggiornamento del registro di sistema per il pacchetto di notifica.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-114">To use your Winlogon notification package, the DLL must be copied to the %SystemRoot%\\system32 folder, and a registry update must be made for the notification package.</span></span> <span data-ttu-id="ed2a5-115">Per informazioni sull'aggiornamento del registro di sistema, vedere la pagina relativa alla [registrazione di un pacchetto di notifica Winlogon](registering-a-winlogon-notification-package.md).</span><span class="sxs-lookup"><span data-stu-id="ed2a5-115">For information about the registry update, see [Registering a Winlogon Notification Package](registering-a-winlogon-notification-package.md).</span></span>

 

 
