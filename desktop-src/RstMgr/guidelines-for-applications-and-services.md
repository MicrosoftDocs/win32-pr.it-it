---
title: Linee guida per le applicazioni e i servizi
description: Per ridurre il numero di riavvii del sistema durante l'installazione e la manutenzione di applicazioni in Windows Vista o Windows Server 2008, è necessario osservare le linee guida seguenti per consentire l'arresto corretto e riavviato dell'applicazione o del servizio.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297945"
---
# <a name="guidelines-for-applications-and-services"></a><span data-ttu-id="4db40-103">Linee guida per le applicazioni e i servizi</span><span class="sxs-lookup"><span data-stu-id="4db40-103">Guidelines for Applications and Services</span></span>

<span data-ttu-id="4db40-104">Per ridurre il numero di riavvii del sistema durante l'installazione e la manutenzione di applicazioni in Windows Vista o Windows Server 2008, è necessario osservare le linee guida seguenti per consentire l'arresto corretto e riavviato dell'applicazione o del servizio.</span><span class="sxs-lookup"><span data-stu-id="4db40-104">To reduce the number of system restarts when installing and servicing applications on Windows Vista or Windows Server 2008, you should observe the following guidelines to enable your application or service to be shut down cleanly and restarted.</span></span>

-   <span data-ttu-id="4db40-105">Le applicazioni e i servizi devono essere preparati per essere arrestati e riavviati dal sistema quando è necessario installare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4db40-105">Your applications and services should be prepared to be shut down and restarted by the system when this is necessary to install an update.</span></span> <span data-ttu-id="4db40-106">In genere, quando viene installato un aggiornamento, è necessario arrestare un'applicazione o un servizio perché attualmente è in uso un file interessato.</span><span class="sxs-lookup"><span data-stu-id="4db40-106">Typically, when an update is installed, an application or service needs to be shut down because it currently holds an affected file in use.</span></span> <span data-ttu-id="4db40-107">Tutte le applicazioni o i servizi che possono contenere un file in uso durante un aggiornamento devono essere preparati per l'arresto corretto.</span><span class="sxs-lookup"><span data-stu-id="4db40-107">All applications or services that can hold a file in use during an update should be prepared to shut down cleanly.</span></span>
-   <span data-ttu-id="4db40-108">Le applicazioni devono salvare i dati utente e le informazioni sullo stato necessarie dopo un riavvio e rispettare le linee guida descritte nella sezione [linee guida per le applicazioni](guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="4db40-108">Your applications should save user data and state information that are needed after a restart and should adhere to the guidelines that are described in the section [Guidelines for Applications](guidelines-for-applications.md).</span></span>
-   <span data-ttu-id="4db40-109">I servizi devono rispettare le linee guida descritte nella sezione [linee guida per i servizi di](guidelines-for-services.md).</span><span class="sxs-lookup"><span data-stu-id="4db40-109">Your services should adhere to the guidelines that are described in the section [Guidelines for Services](guidelines-for-services.md).</span></span>
-   <span data-ttu-id="4db40-110">Gestione riavvio non arresta i [servizi di sistema critici](critical-system-services.md). Pertanto, questi servizi devono limitare il numero di dll da cui dipendono.</span><span class="sxs-lookup"><span data-stu-id="4db40-110">Restart Manager does not shut down [critical system services](critical-system-services.md); therefore, these services should limit the number of DLLs they depend on.</span></span>

 

 




