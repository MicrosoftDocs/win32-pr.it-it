---
description: Dopo aver sviluppato una libreria di collegamento dinamico (SSP/AP) del pacchetto di Security Support Provider/autenticazione contenente uno o più pacchetti di sicurezza personalizzati, è necessario registrarla.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registrazione di dll SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756425"
---
# <a name="registering-sspap-dlls"></a><span data-ttu-id="30c20-103">Registrazione di dll SSP/AP</span><span class="sxs-lookup"><span data-stu-id="30c20-103">Registering SSP/AP DLLs</span></span>

<span data-ttu-id="30c20-104">Dopo lo sviluppo [](../secgloss/s-gly.md)di una / libreria di collegamento dinamico (SSP/AP) del [*pacchetto di autenticazione*](../secgloss/a-gly.md) Security Support Provider contenente uno o più pacchetti di [*sicurezza*](../secgloss/s-gly.md)personalizzati, è necessario registrarla.</span><span class="sxs-lookup"><span data-stu-id="30c20-104">After developing a [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) dynamic-link library (SSP/AP DLL) containing one or more custom [*security packages*](../secgloss/s-gly.md), you must register it.</span></span> <span data-ttu-id="30c20-105">A tale scopo, aggiungere il nome della DLL SSP/AP personalizzata ai dati del valore del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="30c20-105">To do so, add the name of your custom SSP/AP DLL to the data of the following registry value:</span></span>

<span data-ttu-id="30c20-106">**HKEY \_ \_** Pacchetti di \\  \\  \\  \\  \\ **sicurezza** LSA per il controllo CurrentControlSet di sistema del computer locale</span><span class="sxs-lookup"><span data-stu-id="30c20-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Security Packages**</span></span>

<span data-ttu-id="30c20-107">I dati per questo valore del registro di sistema sono un elenco dei nomi di dll SSP/AP, senza l'estensione "dll".</span><span class="sxs-lookup"><span data-stu-id="30c20-107">The data for this registry value is a list of the names of SSP/AP DLLs, without the ".dll" extension.</span></span> <span data-ttu-id="30c20-108">Il tipo di dati per questo elenco **è \_ reg \_ multisz** , quindi deve essere presente un carattere null (' \\ 0') tra ogni nome di dll presente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="30c20-108">The data type for this list is **REG\_MULTI\_SZ** so there must be a null character ('\\0') between each DLL name in the list.</span></span>

<span data-ttu-id="30c20-109">In genere, le dll SSP/AP sono archiviate nella directory% SystemRoot%/system32.</span><span class="sxs-lookup"><span data-stu-id="30c20-109">Typically, SSP/AP DLLs are stored in the %systemroot%/system32 directory.</span></span> <span data-ttu-id="30c20-110">Se questo è il percorso della DLL SSP/AP personalizzata, non includere il percorso come parte del nome della DLL.</span><span class="sxs-lookup"><span data-stu-id="30c20-110">If this is the path to your custom SSP/AP DLL then do not include the path as part of the DLL name.</span></span> <span data-ttu-id="30c20-111">Se, tuttavia, la DLL si trova in un percorso diverso, includere il percorso completo della DLL nel nome.</span><span class="sxs-lookup"><span data-stu-id="30c20-111">If, however, the DLL is in a different path, include the complete path to the DLL in the name.</span></span>

<span data-ttu-id="30c20-112">Ogni volta che il sistema viene avviato, LSA carica le dll SSP/AP in questo elenco ed esegue la sequenza di inizializzazione descritta nell' [inizializzazione in modalità LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="30c20-112">Each time the system starts, the LSA loads the SSP/AP DLLs in this list and performs the initialization sequence described in [LSA-Mode Initialization](lsa-mode-initialization.md).</span></span>

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a><span data-ttu-id="30c20-113">Registrazione di un pacchetto di sicurezza personalizzato come SSP TLS predefinito</span><span class="sxs-lookup"><span data-stu-id="30c20-113">Registering a custom security package as the default TLS SSP</span></span>

<span data-ttu-id="30c20-114">Dopo aver sviluppato un Security Support Provider TLS personalizzato e averlo registrato come descritto in precedenza, è necessario registrarlo anche come "SSP TLS predefinito".</span><span class="sxs-lookup"><span data-stu-id="30c20-114">After developing a custom TLS security support provider and registering it as described above, you must also register it as the “default TLS SSP.”</span></span> <span data-ttu-id="30c20-115">A tale scopo, popolare il nome del pacchetto SSP personalizzato con i dati del valore del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="30c20-115">To do so, populate the package name of your custom SSP to the data of the following registry value:</span></span>

<span data-ttu-id="30c20-116">**HKEY \_ \_** \\  \\  \\  \\  \\ **SSP TLS predefinito** del sistema CurrentControlSet del computer locale</span><span class="sxs-lookup"><span data-stu-id="30c20-116">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Default TLS SSP**</span></span>

<span data-ttu-id="30c20-117">I dati per questo valore del registro di sistema sono il nome del pacchetto SSP, non il nome della dll.</span><span class="sxs-lookup"><span data-stu-id="30c20-117">The data for this registry value is the package name of SSP, not the dll name.</span></span> <span data-ttu-id="30c20-118">Il tipo di dati per è **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="30c20-118">The data type for this is **REG\_SZ**.</span></span>

<span data-ttu-id="30c20-119">Le applicazioni in modalità utente che usano "SSP TLS predefinito" utilizzeranno il valore predefinito registrato qui.</span><span class="sxs-lookup"><span data-stu-id="30c20-119">User mode applications which use “default TLS SSP” will use the default registered here.</span></span> <span data-ttu-id="30c20-120">Questa modifica non avrà alcun effetto sulle applicazioni in modalità kernel o sulle applicazioni in modalità utente che usano "provider del protocollo di sicurezza unificato Microsoft" o altri nomi di SSP TLS specifici.</span><span class="sxs-lookup"><span data-stu-id="30c20-120">Kernel mode applications or user mode applications which use “Microsoft Unified Security Protocol Provider” or other specific TLS SSP names will not be impacted by this change.</span></span>

> [!Note]  
> <span data-ttu-id="30c20-121">Le informazioni del registro di sistema riguardano solo le DLL SSP/AP.</span><span class="sxs-lookup"><span data-stu-id="30c20-121">This registry information pertains to SSP/AP DLL's only.</span></span> <span data-ttu-id="30c20-122">Per informazioni sulla registrazione dei provider di supporto per la sicurezza (SSP), vedere [scrittura e installazione di un Security Support Provider](writing-and-installing-a-security-support-provider.md).</span><span class="sxs-lookup"><span data-stu-id="30c20-122">For information about registering security support providers (SSPs), see [Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md).</span></span> <span data-ttu-id="30c20-123">Per informazioni sulle differenze tra le dll SSP/AP e SSP, vedere [SSP/APS](ssp-aps-versus-ssps.md)e SSP.</span><span class="sxs-lookup"><span data-stu-id="30c20-123">For information about the differences between SSP/AP and SSP DLLs, see [SSP/APs vs. SSPs](ssp-aps-versus-ssps.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="30c20-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30c20-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30c20-125">Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="30c20-125">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
