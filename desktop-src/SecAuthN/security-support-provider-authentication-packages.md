---
description: Il sistema operativo Windows supporta l'autenticazione usando i pacchetti di sicurezza che funzionano sia come provider di supporto della sicurezza che come pacchetti di autenticazione.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Security Support Provider/pacchetti di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311603"
---
# <a name="security-support-providerauthentication-packages"></a><span data-ttu-id="90cf2-103">Security Support Provider/pacchetti di autenticazione</span><span class="sxs-lookup"><span data-stu-id="90cf2-103">Security Support Provider/Authentication Packages</span></span>

<span data-ttu-id="90cf2-104">Il sistema operativo Windows supporta l'autenticazione usando i [*pacchetti di sicurezza*](../secgloss/s-gly.md) che funzionano sia come provider di [*supporto della sicurezza*](../secgloss/s-gly.md) che come pacchetti di [*autenticazione*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="90cf2-104">The Windows operating system supports authentication using [*security packages*](../secgloss/s-gly.md) that function as both [*security support providers*](../secgloss/s-gly.md) and as [*authentication packages*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="90cf2-105">I pacchetti di sicurezza forniscono i servizi di supporto del processo di accesso di un pacchetto di autenticazione di Windows e forniscono servizi di autenticazione alle applicazioni implementando un set di funzioni di cui è stato eseguito il mapping all'interfaccia SSPI ( [Security Support Provider Interface](sspi.md) ).</span><span class="sxs-lookup"><span data-stu-id="90cf2-105">Security packages provide the logon process support services of a Windows authentication package and also provide authentication services to applications by implementing a set of functions that are mapped to the [Security Support Provider Interface](sspi.md) (SSPI).</span></span>

<span data-ttu-id="90cf2-106">Un pacchetto di sicurezza che funge da pacchetto di autenticazione e implementa la funzionalità richiesta da [*SSPI*](../secgloss/s-gly.md) è denominato pacchetto di Security Support Provider/autenticazione (SSP/AP).</span><span class="sxs-lookup"><span data-stu-id="90cf2-106">A security package that functions as an authentication package and implements the functionality required by [*SSPI*](../secgloss/s-gly.md) is called a security support provider/authentication package (SSP/AP).</span></span>

<span data-ttu-id="90cf2-107">Per ulteriori informazioni sui pacchetti di sicurezza, vedere [pacchetti SSP forniti da Microsoft](ssp-packages-provided-by-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="90cf2-107">For more information about security packages, see [SSP Packages Provided by Microsoft](ssp-packages-provided-by-microsoft.md).</span></span> <span data-ttu-id="90cf2-108">Per informazioni sullo sviluppo di SSP/APs personalizzati, vedere [pacchetti di sicurezza personalizzati](custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="90cf2-108">For information about developing custom SSP/APs, see [Custom Security Packages](custom-security-packages.md).</span></span>

 

 
