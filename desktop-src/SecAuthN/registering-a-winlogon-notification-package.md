---
description: Le informazioni sui pacchetti di notifica di Winlogon sono memorizzate nel registro di sistema. Le voci del registro di sistema specificano il nome del pacchetto di notifica, il nome della DLL che implementa il pacchetto e i nomi delle funzioni che gestiscono gli eventi Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrazione di un pacchetto di notifica Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227374"
---
# <a name="registering-a-winlogon-notification-package"></a><span data-ttu-id="2effa-104">Registrazione di un pacchetto di notifica Winlogon</span><span class="sxs-lookup"><span data-stu-id="2effa-104">Registering a Winlogon Notification Package</span></span>

<span data-ttu-id="2effa-105">Le informazioni sui pacchetti di notifica di [*Winlogon*](../secgloss/w-gly.md) sono memorizzate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2effa-105">Information about [*Winlogon*](../secgloss/w-gly.md) notification packages is stored in the registry.</span></span> <span data-ttu-id="2effa-106">Le voci del registro di sistema specificano il nome del pacchetto di notifica, il nome della DLL che implementa il pacchetto e i nomi delle funzioni che gestiscono gli eventi Winlogon.</span><span class="sxs-lookup"><span data-stu-id="2effa-106">Registry entries specify the name of the notification package, the name of the DLL that implements the package, and the names of the functions that handle Winlogon events.</span></span>

<span data-ttu-id="2effa-107">Quando si avvia Winlogon, viene verificato il registro di sistema e vengono caricati tutti i pacchetti di notifica registrati.</span><span class="sxs-lookup"><span data-stu-id="2effa-107">When Winlogon starts, it checks the registry and loads any registered notification packages.</span></span> <span data-ttu-id="2effa-108">Quando si verifica un evento, Winlogon chiama la funzione del gestore eventi designata per ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2effa-108">When an event occurs, Winlogon calls the designated event handler function for each package.</span></span> <span data-ttu-id="2effa-109">È possibile registrare più pacchetti di notifiche degli eventi in un sistema.</span><span class="sxs-lookup"><span data-stu-id="2effa-109">Multiple event notification packages may be registered on a system.</span></span>

<span data-ttu-id="2effa-110">Per registrare il pacchetto di notifica, creare una chiave del registro di sistema denominata **Notify** come sottochiave della chiave del registro di sistema seguente e aggiungere i valori descritti in dettaglio nelle [voci del registro](registry-entries.md)di sistema.</span><span class="sxs-lookup"><span data-stu-id="2effa-110">To register your notification package, create a registry key named **Notify** as a subkey of the following registry key and add the values detailed in [Registry Entries](registry-entries.md).</span></span>

<span data-ttu-id="2effa-111">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**</span><span class="sxs-lookup"><span data-stu-id="2effa-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Winlogon**</span></span>

 

 
