---
title: Informazioni su TBS
description: Servizio di sistema che consente la condivisione trasparente delle risorse del Trusted Platform Module (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- Servizi di base TPM TBS, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104223400"
---
# <a name="about-tbs"></a><span data-ttu-id="25cd5-104">Informazioni su TBS</span><span class="sxs-lookup"><span data-stu-id="25cd5-104">About TBS</span></span>

<span data-ttu-id="25cd5-105">La funzionalità Servizi di base TPM (TBS) è un servizio di sistema che consente la condivisione trasparente delle risorse del Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="25cd5-105">The TPM Base Services (TBS) feature is a system service that allows transparent sharing of the Trusted Platform Module (TPM) resources.</span></span> <span data-ttu-id="25cd5-106">Condivide contemporaneamente le risorse TPM tra più applicazioni nello stesso computer fisico, anche se tali applicazioni vengono eseguite in macchine virtuali diverse.</span><span class="sxs-lookup"><span data-stu-id="25cd5-106">It simultaneously shares the TPM resources among multiple applications on the same physical machine, even if those applications run on different virtual machines.</span></span> <span data-ttu-id="25cd5-107">A partire da Windows 8 e Windows Server 2012, TBS è preinstallato in tutti i sistemi con un TPM.</span><span class="sxs-lookup"><span data-stu-id="25cd5-107">Starting with Windows 8 and Windows Server 2012, TBS comes pre-installed on all systems with a TPM.</span></span>

<span data-ttu-id="25cd5-108">Il Trusted Computing Group (TCG) definisce una Trusted Platform Module che fornisce funzioni di crittografia progettate per fornire attendibilità alla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="25cd5-108">The Trusted Computing Group (TCG) defines a Trusted Platform Module that provides cryptographic functions designed to provide trust in the platform.</span></span> <span data-ttu-id="25cd5-109">Poiché il TPM è implementato nell'hardware, dispone di risorse finite.</span><span class="sxs-lookup"><span data-stu-id="25cd5-109">Because the TPM is implemented in hardware, it has finite resources.</span></span> <span data-ttu-id="25cd5-110">Il TCG definisce anche uno stack software che usa queste risorse per fornire operazioni attendibili per il software applicativo.</span><span class="sxs-lookup"><span data-stu-id="25cd5-110">The TCG also defines a software stack that makes use of these resources to provide trusted operations for application software.</span></span> <span data-ttu-id="25cd5-111">Tuttavia, non viene effettuato alcun provisioning per l'esecuzione side-by-side di un'implementazione di TSS con software del sistema operativo che può utilizzare anche risorse TPM.</span><span class="sxs-lookup"><span data-stu-id="25cd5-111">However, no provision is made for running a TSS implementation side-by-side with operating system software that may also be using TPM resources.</span></span> <span data-ttu-id="25cd5-112">La funzionalità TBS risolve questo problema abilitando ogni stack software che comunica con TBS per usare le risorse TPM per verificare la presenza di altri stack software che potrebbero essere in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="25cd5-112">The TBS feature solves this problem by enabling each software stack that communicates with TBS to use TPM resources checking for any other software stacks that may be running on the machine.</span></span>

<span data-ttu-id="25cd5-113">Le specifiche TPM e lo stack software TCG (TSS) sono disponibili all'indirizzo [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .</span><span class="sxs-lookup"><span data-stu-id="25cd5-113">The TPM specification and TCG Software Stack (TSS) specification are available at [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/).</span></span>

<span data-ttu-id="25cd5-114">TBS viene implementato come servizio out-of-process che accetta i comandi che usano un servizio RPC.</span><span class="sxs-lookup"><span data-stu-id="25cd5-114">TBS is implemented as an out-of-process service that accepts commands that use an RPC service.</span></span> <span data-ttu-id="25cd5-115">Una libreria collegata dinamicamente presenta l'interfaccia del linguaggio C e comunica con il servizio TBS.</span><span class="sxs-lookup"><span data-stu-id="25cd5-115">A dynamically linked library presents the C language interface and communicates with the TBS service.</span></span>

> [!Note]  
> <span data-ttu-id="25cd5-116">Il servizio TBS accetta solo le richieste RPC dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="25cd5-116">The TBS service only accepts RPC requests from the local machine.</span></span>

 

<span data-ttu-id="25cd5-117">Gli obiettivi principali di TBS sono:</span><span class="sxs-lookup"><span data-stu-id="25cd5-117">The primary goals of the TBS are to:</span></span>

-   <span data-ttu-id="25cd5-118">Fornire una condivisione efficiente di risorse TPM limitate, ad esempio slot chiave, slot di sessioni di autorizzazione e slot di trasporto.</span><span class="sxs-lookup"><span data-stu-id="25cd5-118">Provide efficient sharing of limited TPM resources, such as key slots, authorization sessions slots, and transport slots.</span></span>
-   <span data-ttu-id="25cd5-119">Fornire l'accesso in ordine di priorità e sincronizzato alle risorse TPM tra più istanze di stack di software TPM.</span><span class="sxs-lookup"><span data-stu-id="25cd5-119">Provide prioritized and synchronized access to TPM resources between multiple instances of TPM software stacks.</span></span>
-   <span data-ttu-id="25cd5-120">Fornire una gestione appropriata delle risorse TPM tra gli Stati di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="25cd5-120">Provide appropriate management of TPM resources across power states.</span></span>
-   <span data-ttu-id="25cd5-121">Impedire agli stack di software TPM di accedere ai comandi TPM che devono essere limitati a causa di limitazioni della piattaforma o requisiti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="25cd5-121">Prevent TPM software stacks from accessing TPM commands that should be restricted, either because of platform limitations or administrative requirements.</span></span>

<span data-ttu-id="25cd5-122">Nella figura seguente viene illustrata la relazione tra TBS e il TPM.</span><span class="sxs-lookup"><span data-stu-id="25cd5-122">The following illustration shows the relationship of the TBS to the TPM.</span></span>

![relazione di TBS in modalità utente con il TPM in modalità kernel](images/tbs-block-diagram-as11601.png)

 

 




