---
description: Vengono illustrate le considerazioni per l'implementazione delle funzioni di esportazione del filtro delle password.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Considerazioni sulla programmazione del filtro password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306435"
---
# <a name="password-filter-programming-considerations"></a><span data-ttu-id="39a7c-103">Considerazioni sulla programmazione del filtro password</span><span class="sxs-lookup"><span data-stu-id="39a7c-103">Password Filter Programming Considerations</span></span>

<span data-ttu-id="39a7c-104">Quando si implementano le funzioni di esportazione del [*filtro delle password*](/windows/desktop/SecGloss/p-gly) , tenere presenti le considerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="39a7c-104">When implementing [*password filter*](/windows/desktop/SecGloss/p-gly) export functions, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="39a7c-105">Prestare particolare attenzione quando si utilizzano password in [*testo non crittografato*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="39a7c-105">Take great care when working with [*plaintext*](/windows/desktop/SecGloss/p-gly) passwords.</span></span> <span data-ttu-id="39a7c-106">L'invio di password in testo non crittografato attraverso le reti potrebbe compromettere</span><span class="sxs-lookup"><span data-stu-id="39a7c-106">Sending plaintext passwords over networks could compromise security.</span></span> <span data-ttu-id="39a7c-107">I "sniffer" della rete possono controllare facilmente il traffico delle password in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="39a7c-107">Network "sniffers" can easily watch for plaintext password traffic.</span></span>
-   <span data-ttu-id="39a7c-108">Cancellare tutta la memoria usata per archiviare le password chiamando la funzione [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) prima di liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="39a7c-108">Erase all memory used to store passwords by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function before freeing memory.</span></span>
-   <span data-ttu-id="39a7c-109">Tutti i buffer passati nelle routine di notifica e filtro delle password devono essere considerati di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="39a7c-109">All buffers passed into password notification and filter routines should be treated as read-only.</span></span> <span data-ttu-id="39a7c-110">La scrittura di dati in questi buffer può causare un comportamento instabile.</span><span class="sxs-lookup"><span data-stu-id="39a7c-110">Writing data to these buffers may cause unstable behavior.</span></span>
-   <span data-ttu-id="39a7c-111">Tutte le routine di notifica e filtro della password devono essere thread-safe.</span><span class="sxs-lookup"><span data-stu-id="39a7c-111">All password notification and filter routines should be thread-safe.</span></span> <span data-ttu-id="39a7c-112">Usare sezioni critiche o altre tecniche di programmazione sincrona per proteggere i dati laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="39a7c-112">Use critical sections or other synchronous programming techniques to protect data where appropriate.</span></span>
-   <span data-ttu-id="39a7c-113">La notifica e il filtro delle password avvengono solo nel computer che ospita l'account.</span><span class="sxs-lookup"><span data-stu-id="39a7c-113">Password notification and filtering take place only on the computer that houses the account.</span></span>
-   <span data-ttu-id="39a7c-114">Tutti i controller di dominio sono scrivibili, quindi i pacchetti di filtro password devono essere presenti in tutti i controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="39a7c-114">All domain controllers are writeable, therefore password filter packages must be present on all domain controllers.</span></span>

    <span data-ttu-id="39a7c-115">**Domini di Windows NT 4,0:** La notifica sugli account di dominio si verifica solo sul controller di dominio primario.</span><span class="sxs-lookup"><span data-stu-id="39a7c-115">**Windows NT 4.0 domains:** Notification on domain accounts takes place only on the primary domain controller.</span></span> <span data-ttu-id="39a7c-116">Oltre al controller di dominio primario, i pacchetti di filtro password devono essere installati in tutti i controller di dominio di backup per consentire la continuazione delle notifiche in caso di modifiche al ruolo del server.</span><span class="sxs-lookup"><span data-stu-id="39a7c-116">In addition to the primary domain controller, the password filter packages should be installed on all backup domain controllers to allow notifications to continue in the event of server role changes.</span></span>

-   <span data-ttu-id="39a7c-117">Tutte le dll del filtro password vengono eseguite nel [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) dell'account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="39a7c-117">All password filter DLLs run in the [*security context*](/windows/desktop/SecGloss/s-gly) of the local system account.</span></span>



| <span data-ttu-id="39a7c-118">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="39a7c-118">For information about</span></span>                                                                                                                     | <span data-ttu-id="39a7c-119">Vedere</span><span class="sxs-lookup"><span data-stu-id="39a7c-119">See</span></span>                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a7c-120">Come installare e registrare la propria DLL di [*filtro password*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="39a7c-120">How to install and register your own [*password filter*](/windows/desktop/SecGloss/p-gly) DLL.</span></span> | [<span data-ttu-id="39a7c-121">Installazione e registrazione di una DLL di filtro password</span><span class="sxs-lookup"><span data-stu-id="39a7c-121">Installing and Registering a Password Filter DLL</span></span>](installing-and-registering-a-password-filter-dll.md) |
| <span data-ttu-id="39a7c-122">DLL di filtro password fornita da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39a7c-122">The password filter DLL provided by Microsoft.</span></span>                                                                                            | [<span data-ttu-id="39a7c-123">Imposizione avanzata delle password e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="39a7c-123">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)         |
| <span data-ttu-id="39a7c-124">Esporta le funzioni implementate da una DLL di filtro password.</span><span class="sxs-lookup"><span data-stu-id="39a7c-124">Export functions implemented by a password filter DLL.</span></span>                                                                                    | [<span data-ttu-id="39a7c-125">Funzioni di filtro password</span><span class="sxs-lookup"><span data-stu-id="39a7c-125">Password Filter Functions</span></span>](management-functions.md)                          |



 

 

 
