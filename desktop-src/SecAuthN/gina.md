---
description: Lo scopo di una DLL GINA è fornire procedure di identificazione e autenticazione utente personalizzabili. Per impostazione predefinita, GINA esegue questa operazione delegando il monitoraggio degli eventi SAS a Winlogon, che riceve ed elabora le sequenze di attenzione (SASs, Secure Attention Sequence) CTL + ALT + CANC.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758267"
---
# <a name="gina"></a><span data-ttu-id="b8ce9-104">GINA</span><span class="sxs-lookup"><span data-stu-id="b8ce9-104">GINA</span></span>

<span data-ttu-id="b8ce9-105">[*Gina*](/windows/desktop/SecGloss/g-gly) opera nel [*contesto*](/windows/desktop/SecGloss/c-gly) del processo [*Winlogon*](/windows/desktop/SecGloss/w-gly) e, di conseguenza, la DLL GINA viene caricata molto presto nel processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-105">The [*GINA*](/windows/desktop/SecGloss/g-gly) operates in the [*context*](/windows/desktop/SecGloss/c-gly) of the [*Winlogon*](/windows/desktop/SecGloss/w-gly) process and, as such, the GINA DLL is loaded very early in the boot process.</span></span> <span data-ttu-id="b8ce9-106">La DLL GINA deve seguire le regole in modo che l'integrità del sistema venga mantenuta, in particolare in relazione all'interazione con l'utente.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-106">The GINA DLL must follow rules so that the integrity of the system is maintained, particularly with respect to interaction with the user.</span></span>

> [!Note]  
> <span data-ttu-id="b8ce9-107">Le DLL GINA vengono ignorate in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-107">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="b8ce9-108">L'uso più comune di GINA consiste nel comunicare con un dispositivo esterno, ad esempio un [*lettore*](/windows/desktop/SecGloss/r-gly)di smart card.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-108">The most common use of the GINA is to communicate with an external device such as a smart-card [*reader*](/windows/desktop/SecGloss/r-gly).</span></span> <span data-ttu-id="b8ce9-109">È essenziale impostare il parametro Start per il driver di dispositivo su System (Winnt. h: SERVICE \_ System \_ Start) per assicurarsi che il driver venga caricato nel momento in cui Gina viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-109">It is essential to set the start parameter for the device driver to system (Winnt.h: SERVICE\_SYSTEM\_START) to ensure that the driver is loaded by the time the GINA is invoked.</span></span>

<span data-ttu-id="b8ce9-110">Lo scopo di una DLL GINA è fornire procedure di identificazione e autenticazione utente personalizzabili.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-110">The purpose of a GINA DLL is to provide customizable user identification and authentication procedures.</span></span> <span data-ttu-id="b8ce9-111">Per impostazione predefinita, GINA esegue questa operazione delegando il monitoraggio degli eventi SAS a Winlogon, che riceve ed elabora le sequenze di attenzione (SASs, [*Secure Attention Sequence*](/windows/desktop/SecGloss/s-gly) ) CTL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-111">The default GINA does this by delegating SAS event monitoring to Winlogon, which receives and processes CTL+ALT+DEL [*secure attention sequences*](/windows/desktop/SecGloss/s-gly) (SASs).</span></span> <span data-ttu-id="b8ce9-112">Un oggetto GINA personalizzato è responsabile dell'impostazione per la ricezione di eventi di firma di accesso condiviso (ad eccezione dell'evento di firma di accesso condiviso con CTRL + ALT + CANC) e la notifica di Winlogon quando si verificano eventi SAS.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-112">A custom GINA is responsible for setting itself up to receive SAS events (other than the default CTRL+ALT+DEL SAS event) and notifying Winlogon when SAS events occur.</span></span> <span data-ttu-id="b8ce9-113">Winlogon valuterà il proprio stato per determinare gli elementi necessari per elaborare la firma di accesso condiviso di GINA personalizzata.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-113">Winlogon will evaluate its state to determine what is required to process the custom GINA's SAS.</span></span> <span data-ttu-id="b8ce9-114">Questa elaborazione include in genere le chiamate alle funzioni di elaborazione SAS di GINA.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-114">This processing usually includes calls to the GINA's SAS processing functions.</span></span>

<span data-ttu-id="b8ce9-115">Per informazioni sulle funzioni di esportazione GINA specifiche, vedere [funzioni di esportazione Gina](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="b8ce9-115">For information about specific GINA export functions, see [GINA Export Functions](authentication-functions.md).</span></span> <span data-ttu-id="b8ce9-116">Per informazioni sull'utilizzo delle strutture GINA per il passaggio di informazioni, vedere la pagina relativa alle [strutture Gina](authentication-structures.md).</span><span class="sxs-lookup"><span data-stu-id="b8ce9-116">For information about using GINA structures to pass information, see [GINA Structures](authentication-structures.md).</span></span>



| <span data-ttu-id="b8ce9-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="b8ce9-117">Topic</span></span>                                                                             | <span data-ttu-id="b8ce9-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8ce9-118">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="b8ce9-119">Caricamento ed esecuzione di una DLL GINA</span><span class="sxs-lookup"><span data-stu-id="b8ce9-119">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)<br/>   | <span data-ttu-id="b8ce9-120">Il valore della chiave del registro di sistema da modificare per caricare ed eseguire una DLL GINA personalizzata.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-120">Which registry key value to alter to load and run a custom GINA DLL.</span></span><br/> |
| [<span data-ttu-id="b8ce9-121">Compilazione e test di una DLL GINA</span><span class="sxs-lookup"><span data-stu-id="b8ce9-121">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)<br/> | <span data-ttu-id="b8ce9-122">Come testare una DLL GINA.</span><span class="sxs-lookup"><span data-stu-id="b8ce9-122">How to test a GINA DLL.</span></span><br/>                                              |



 

 

