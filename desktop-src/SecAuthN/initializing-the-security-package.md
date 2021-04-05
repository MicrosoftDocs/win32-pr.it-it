---
description: Elenca e illustra i passaggi necessari per inizializzare un pacchetto di sicurezza.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Inizializzazione del pacchetto di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131182"
---
# <a name="initializing-the-security-package"></a><span data-ttu-id="3de91-103">Inizializzazione del pacchetto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="3de91-103">Initializing the Security Package</span></span>

<span data-ttu-id="3de91-104">Questi passaggi sono necessari prima di utilizzare SSPI:</span><span class="sxs-lookup"><span data-stu-id="3de91-104">These steps are necessary before using SSPI:</span></span>

1.  <span data-ttu-id="3de91-105">La funzione di inizializzazione deve essere chiamata per ottenere l'indirizzo della tabella delle funzioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="3de91-105">The initialization function must be called to obtain the address of the security function table.</span></span>

    <span data-ttu-id="3de91-106">Il client e il server chiamano [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) per un puntatore a una tabella di invio [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) .</span><span class="sxs-lookup"><span data-stu-id="3de91-106">The client and server call [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) for a pointer to a [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) dispatch table.</span></span> <span data-ttu-id="3de91-107">Questa tabella contiene i puntatori alle funzioni di callback dichiarate in SSPI. h.</span><span class="sxs-lookup"><span data-stu-id="3de91-107">This table contains pointers to callback functions declared in Sspi.h.</span></span> <span data-ttu-id="3de91-108">Questi puntatori forniscono l'accesso alle implementazioni della DLL delle varie funzioni SSPI.</span><span class="sxs-lookup"><span data-stu-id="3de91-108">These pointers provide access to the DLL's implementations of the various SSPI functions.</span></span>

2.  <span data-ttu-id="3de91-109">È necessario ottenere informazioni sui pacchetti di sicurezza supportati.</span><span class="sxs-lookup"><span data-stu-id="3de91-109">Information must be obtained about the supported security packages.</span></span>

    <span data-ttu-id="3de91-110">Sebbene la maggior parte delle applicazioni usi pacchetti di sicurezza che supportano le funzionalità predefinite o comuni, i pacchetti di sicurezza possono avere funzionalità univoche di interesse per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3de91-110">While most applications use security packages that support default or common capabilities, security packages can have unique capabilities of interest to the application.</span></span> <span data-ttu-id="3de91-111">Un'applicazione che necessita di funzionalità speciali può usare un pacchetto che offre tali funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3de91-111">An application needing special capabilities can use a package that offers those capabilities.</span></span> <span data-ttu-id="3de91-112">Per ulteriori informazioni, vedere [ottenere informazioni sui pacchetti di sicurezza](getting-information-about-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="3de91-112">For more information, see [Getting Information About Security Packages](getting-information-about-security-packages.md).</span></span>

<span data-ttu-id="3de91-113">A questo punto, l'applicazione ha inizializzato correttamente un SSP e ha scelto un pacchetto di sicurezza con funzionalità sufficienti.</span><span class="sxs-lookup"><span data-stu-id="3de91-113">At this point, the application has successfully initialized an SSP and chosen a security package with sufficient capabilities.</span></span>

<span data-ttu-id="3de91-114">Il pacchetto [*Negotiate*](../secgloss/n-gly.md) può essere usato in caso di accordo tra il client e il server in cui viene eseguito il [*pacchetto di sicurezza*](../secgloss/s-gly.md) da usare.</span><span class="sxs-lookup"><span data-stu-id="3de91-114">The [*Negotiate*](../secgloss/n-gly.md) package can be used where agreement between client and server about which [*security package*](../secgloss/s-gly.md) to use is done behind the scenes.</span></span> <span data-ttu-id="3de91-115">Se il pacchetto Negotiate non viene utilizzato, il client e il server devono accettare il pacchetto di sicurezza specifico da utilizzare prima di eseguire i passaggi di configurazione descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3de91-115">If the Negotiate package is not used, the client and server must agree on the specific security package to use before performing the setup steps above.</span></span>

 

 
