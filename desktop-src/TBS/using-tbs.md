---
title: Uso di TBS
description: Ogni comando inviato a TBS è associato a un'entità specifica. Questa operazione viene eseguita creando uno o più contesti per un'entità, che vengono quindi associati a ogni comando successivo Inviato da tale entità.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- Servizi di base TPM TBS, esempi
- Servizi di base TPM TBS, uso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955519"
---
# <a name="using-tbs"></a><span data-ttu-id="625c4-106">Uso di TBS</span><span class="sxs-lookup"><span data-stu-id="625c4-106">Using TBS</span></span>

<span data-ttu-id="625c4-107">La funzionalità Servizi di base TPM è divisa in quattro aree funzionali:</span><span class="sxs-lookup"><span data-stu-id="625c4-107">The TPM Base Services feature is divided into four functional areas:</span></span>

-   [<span data-ttu-id="625c4-108">Virtualizzazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="625c4-108">Resource Virtualization</span></span>](resource-virtualization.md)
-   [<span data-ttu-id="625c4-109">Pianificazione comandi</span><span class="sxs-lookup"><span data-stu-id="625c4-109">Command Scheduling</span></span>](command-scheduling.md)
-   [<span data-ttu-id="625c4-110">Risparmio energia</span><span class="sxs-lookup"><span data-stu-id="625c4-110">Power Management</span></span>](power-management.md)
-   [<span data-ttu-id="625c4-111">Blocco comandi</span><span class="sxs-lookup"><span data-stu-id="625c4-111">Command Blocking</span></span>](command-blocking.md)

<span data-ttu-id="625c4-112">Per assicurarsi che entità diverse non possano accedere alle risorse reciproche, ogni comando inviato a TBS è associato a un'entità specifica.</span><span class="sxs-lookup"><span data-stu-id="625c4-112">To ensure that different entities cannot access each other's resources, each command submitted to the TBS is associated with a specific entity.</span></span> <span data-ttu-id="625c4-113">Questa operazione viene eseguita creando uno o più contesti per un'entità, che vengono quindi associati a ogni comando successivo Inviato da tale entità.</span><span class="sxs-lookup"><span data-stu-id="625c4-113">This is accomplished by creating one or more contexts for an entity, which are then associated with each subsequent command submitted by that entity.</span></span> <span data-ttu-id="625c4-114">Ogni comando include un oggetto context, che consente a TBS di eseguire i comandi TPM nel contesto appropriato.</span><span class="sxs-lookup"><span data-stu-id="625c4-114">Each command includes a context object, which allows the TBS to execute TPM commands under the appropriate context.</span></span> <span data-ttu-id="625c4-115">Tutti gli oggetti creati dai comandi vengono scaricati dal TPM quando il contesto viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="625c4-115">All objects created by commands are flushed from the TPM when the context is closed.</span></span>

<span data-ttu-id="625c4-116">Un'entità crea il contesto prima di accedere prima a TBS e mantiene il contesto fino a quando non termina l'esecuzione degli accessi TBS.</span><span class="sxs-lookup"><span data-stu-id="625c4-116">An entity creates the context before it first accesses the TBS and maintains the context until it is finished performing TBS accesses.</span></span> <span data-ttu-id="625c4-117">Ad esempio, nel caso di TSS, la funzionalità del servizio TCG Core Services (TCS) di TSS creerebbe un contesto di TBS all'avvio e manterrà il contesto attivo fino a quando non si arresta.</span><span class="sxs-lookup"><span data-stu-id="625c4-117">For example, in the case of a TSS, the TCG core services (TCS) feature of the TSS would create a TBS context when it starts up, and it would keep that context active until it shuts down.</span></span>

<span data-ttu-id="625c4-118">Per Windows Server 2008 e Windows Vista, TBS limita l'accesso all'API TBS agli account Administrators, NT AUTHORITY \\ LocalService e NT Authority \\ NetworkService.</span><span class="sxs-lookup"><span data-stu-id="625c4-118">For Windows Server 2008 and Windows Vista, the TBS restricts access to the TBS API to the Administrators, NT AUTHORITY\\LocalService, and NT AUTHORITY\\NetworkService accounts.</span></span> <span data-ttu-id="625c4-119">Per impostazione predefinita, questi account sono gli unici che possono connettersi a TBS e creare contesti.</span><span class="sxs-lookup"><span data-stu-id="625c4-119">By default, these accounts are the only ones that can connect to TBS and create contexts.</span></span> <span data-ttu-id="625c4-120">Le restrizioni di accesso possono essere modificate creando un **accesso** alla chiave del registro di sistema con un nome di valore del registro di sistema di stringa (**reg \_ SZ**) **securityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="625c4-120">Access restrictions can be modified by creating a registry key **Access** with a string (**REG\_SZ**) registry value name **SecurityDescriptor**</span></span> <dl> <dt>

<span data-ttu-id="625c4-121">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="625c4-121">Data type</span></span>
</dt> <dd><span data-ttu-id="625c4-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="625c4-122">REG_SZ</span></span></dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

<span data-ttu-id="625c4-123">Esempio:</span><span class="sxs-lookup"><span data-stu-id="625c4-123">Example:</span></span>

<span data-ttu-id="625c4-124">**O:BAG: BAD: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; LS**</span><span class="sxs-lookup"><span data-stu-id="625c4-124">**O:BAG:BAD:(A;;0x00000001;;;BA)(A;;0x00000001;;;NS)(A;;0x00000001;;;LS)**</span></span>

<span data-ttu-id="625c4-125">Per impostazione predefinita, il numero massimo di contesti supportato da TBS è 25.</span><span class="sxs-lookup"><span data-stu-id="625c4-125">By default, the maximum number of contexts supported by the TBS is 25.</span></span> <span data-ttu-id="625c4-126">Questo numero può essere modificato creando o modificando un valore **DWORD** del registro di sistema denominato **MaxContexts** in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**.</span><span class="sxs-lookup"><span data-stu-id="625c4-126">This number can be altered by creating or modifying a **DWORD** registry value named **MaxContexts** under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Tpm**.</span></span> <span data-ttu-id="625c4-127">È possibile osservare l'utilizzo del contesto di TBS in tempo reale usando lo strumento Performance Monitor per tenere traccia del numero di contesti TBS.</span><span class="sxs-lookup"><span data-stu-id="625c4-127">Real-time TBS context usage can be observed by using the performance monitor tool to track the number of TBS contexts.</span></span>

<span data-ttu-id="625c4-128">Per Windows 8, Windows Server 2012 e versioni successive, TBS consente l'accesso agli utenti e agli amministratori standard.</span><span class="sxs-lookup"><span data-stu-id="625c4-128">For Windows 8, Windows Server 2012 and later, the TBS allows access to standard users and administrators.</span></span> <span data-ttu-id="625c4-129">Le chiavi del registro di sistema **securityDescriptor** e **MaxContexts** sono diventate obsolete.</span><span class="sxs-lookup"><span data-stu-id="625c4-129">The **SecurityDescriptor** and **MaxContexts** registry keys became obsolete.</span></span> <span data-ttu-id="625c4-130">Per Windows 8, Windows Server 2012 e versioni successive, TBS limita l'accesso a determinati comandi usando il blocco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="625c4-130">For Windows 8, Windows Server 2012 and later, the TBS restricts access to certain commands using Command Blocking.</span></span>

<span data-ttu-id="625c4-131">Per Windows 10, versione 1607, TBS consente l'accesso dalle applicazioni AppContainer.</span><span class="sxs-lookup"><span data-stu-id="625c4-131">For Windows 10, version 1607, the TBS allows access from AppContainer applications.</span></span> <span data-ttu-id="625c4-132">Per ogni versione del TPM, le chiavi **BlockedAppContainerCommands** e **AllowedW8AppContainerCommands** sono state aggiunte con gli elenchi corrispondenti rispettivamente dei comandi TPM bloccati e consentiti.</span><span class="sxs-lookup"><span data-stu-id="625c4-132">For each TPM version, the keys **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands** have been added with the matching lists of blocked and allowed TPM commands, respectively.</span></span>

<span data-ttu-id="625c4-133">Per Windows 10, versione 1803, le chiavi del registro di sistema in **AllowedW8AppContainerCommands** non sono più supportate.</span><span class="sxs-lookup"><span data-stu-id="625c4-133">For Windows 10, version 1803, the registry keys under **AllowedW8AppContainerCommands** are no longer supported.</span></span>

 

 




