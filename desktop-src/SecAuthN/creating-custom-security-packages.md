---
description: Viene illustrato come creare un pacchetto di sicurezza personalizzato.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Creazione di pacchetti di sicurezza personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882661"
---
# <a name="creating-custom-security-packages"></a><span data-ttu-id="e2e59-103">Creazione di pacchetti di sicurezza personalizzati</span><span class="sxs-lookup"><span data-stu-id="e2e59-103">Creating Custom Security Packages</span></span>

## <a name="ssp-security-packages"></a><span data-ttu-id="e2e59-104">Pacchetti di sicurezza SSP</span><span class="sxs-lookup"><span data-stu-id="e2e59-104">SSP Security Packages</span></span>

<span data-ttu-id="e2e59-105">Se un pacchetto di sicurezza di un Security Support Provider personalizzato (SSP) verrà utilizzato esclusivamente per il supporto della sicurezza client/server, può implementare l'interfaccia di Microsoft [Security Support Provider](sspi.md).</span><span class="sxs-lookup"><span data-stu-id="e2e59-105">If a custom security support provider (SSP) security package will be used exclusively for client/server security support it can implement the Microsoft [Security Support Provider Interface](sspi.md).</span></span>

<span data-ttu-id="e2e59-106">L'esempio SampSSP fornito con Platform Software Development Kit (SDK) contiene un'implementazione di pacchetto di sicurezza SSP di esempio.</span><span class="sxs-lookup"><span data-stu-id="e2e59-106">The SampSSP sample shipped with the Platform Software Development Kit (SDK) contains a sample SSP security package implementation.</span></span>

## <a name="sspap-security-packages"></a><span data-ttu-id="e2e59-107">Pacchetti di sicurezza SSP/AP</span><span class="sxs-lookup"><span data-stu-id="e2e59-107">SSP/AP Security Packages</span></span>

<span data-ttu-id="e2e59-108">I [](/windows/desktop/SecGloss/s-gly) / [*pacchetti di autenticazione*](/windows/desktop/SecGloss/a-gly) Security Support Provider personalizzati (SSP/APS) contengono pacchetti di sicurezza che funzionano come pacchetti di autenticazione (APS) e provider di supporto per la sicurezza (SSP).</span><span class="sxs-lookup"><span data-stu-id="e2e59-108">Custom [*security support provider*](/windows/desktop/SecGloss/s-gly)/[*authentication packages*](/windows/desktop/SecGloss/a-gly) (SSP/APs) contain security packages that function as authentication packages (APs) and security support providers (SSPs).</span></span> <span data-ttu-id="e2e59-109">Questi pacchetti implementano API separate per supportare ogni ruolo.</span><span class="sxs-lookup"><span data-stu-id="e2e59-109">These packages implement separate APIs to support each role.</span></span>

<span data-ttu-id="e2e59-110">Poiché funziona come punto di accesso, un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) SSP/AP personalizzato deve fornire implementazioni per tutte le [funzioni implementate dai pacchetti di autenticazione](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e59-110">Because it functions as an AP, a custom SSP/AP [*security package*](/windows/desktop/SecGloss/s-gly) must provide implementations for all of the [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="e2e59-111">Per garantire un supporto integrato per la sicurezza, un pacchetto di sicurezza SSP/AP personalizzato deve fornire implementazioni per le [funzioni implementate da SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e59-111">To provide integrated security support, a custom SSP/AP security package must provide implementations for the [Functions implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="e2e59-112">Le [funzioni LSA chiamate da SSP/APS](authentication-functions.md) descrivono le funzioni di supporto disponibili per gli sviluppatori SSP/AP che vogliono interagire con LSA.</span><span class="sxs-lookup"><span data-stu-id="e2e59-112">[LSA Functions Called by SSP/APs](authentication-functions.md) describes the support functions available to the SSP/AP developers that want to interact with the LSA.</span></span>

<span data-ttu-id="e2e59-113">I pacchetti di sicurezza SSP/AP, per poter essere eseguiti sia come punto di accesso sia come provider di servizi condivisi, possono essere eseguiti come parte del sistema operativo e come parte di un'applicazione utente.</span><span class="sxs-lookup"><span data-stu-id="e2e59-113">SSP/AP security packages, in order to perform as both an AP and an SSP, may execute as part of the operating system and as part of a user application.</span></span> <span data-ttu-id="e2e59-114">Queste due modalità di esecuzione sono note rispettivamente come modalità LSA e modalità utente.</span><span class="sxs-lookup"><span data-stu-id="e2e59-114">These two modes of execution are known as LSA mode and user mode, respectively.</span></span> <span data-ttu-id="e2e59-115">Per informazioni dettagliate sui pacchetti di sicurezza personalizzati in modalità LSA, vedere [inizializzazione della modalità LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="e2e59-115">For details about custom security packages in LSA mode see [LSA Mode Initialization](lsa-mode-initialization.md).</span></span> <span data-ttu-id="e2e59-116">Per informazioni dettagliate sulla modalità utente, vedere [inizializzazione della modalità utente](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="e2e59-116">For details about user mode, see [User Mode Initialization](user-mode-initialization.md).</span></span>

<span data-ttu-id="e2e59-117">Se un pacchetto di sicurezza SSP/AP personalizzato offre servizi per le applicazioni client/server, deve fornire implementazioni per le funzioni descritte in [funzioni implementate da SSP/APS in modalità utente](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2e59-117">If a custom SSP/AP security package offers services for client/server applications it should provide implementations for the functions described in [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="e2e59-118">Le [funzioni LSA chiamate da SSP/APS in modalità utente](authentication-functions.md) descrivono le funzioni di supporto disponibili per un SSP/AP eseguito in un processo client o server.</span><span class="sxs-lookup"><span data-stu-id="e2e59-118">[LSA Functions Called By User-mode SSP/APs](authentication-functions.md) describes the support functions available to an SSP/AP executing in a client or server process.</span></span>

<span data-ttu-id="e2e59-119">Per informazioni sulla registrazione di una DLL SSP/AP, vedere la pagina relativa alla registrazione di DLL [SSP/AP](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="e2e59-119">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2e59-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2e59-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2e59-121">Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e2e59-121">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
