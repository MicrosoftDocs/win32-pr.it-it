---
description: Gli script e le applicazioni scritti per i sistemi operativi a 32 bit dovrebbero continuare a funzionare correttamente.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Fornire dati WMI in una piattaforma a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527745"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="274e2-103">Fornire dati WMI in una piattaforma a 64 bit</span><span class="sxs-lookup"><span data-stu-id="274e2-103">Providing WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="274e2-104">Gli script e le applicazioni scritti per i sistemi operativi a 32 bit dovrebbero continuare a funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="274e2-104">Scripts and applications written for 32-bit operating systems should continue to run properly.</span></span> <span data-ttu-id="274e2-105">Se è presente un provider a 32 bit, è possibile valutare se è necessario scrivere una versione a 64 bit per l'operazione side-by-side.</span><span class="sxs-lookup"><span data-stu-id="274e2-105">If you have an existing 32-bit provider, you can evaluate whether you need to write a 64-bit version for side-by-side operation.</span></span> <span data-ttu-id="274e2-106">In genere, entrambe le versioni non sono necessarie e la versione a 64 bit può servire sia il client locale che quello remoto a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="274e2-106">Generally, both versions are not necessary and the 64-bit version can service both 32-bit and 64-bit local or remote clients.</span></span> <span data-ttu-id="274e2-107">Tuttavia, per la modalità di compatibilità delle applicazioni a 32 bit, utilizzare il provider WMI esistente a 32 bit in un sistema a 64 bit eseguito in modalità WOW64 a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="274e2-107">However, for 32-bit application compatibility mode, use your existing 32-bit WMI provider on a 64-bit system that runs in the 32-bit WOW64 mode.</span></span>

<span data-ttu-id="274e2-108">In rari casi, sia i provider a 32 bit che quelli a 64 bit devono essere eseguiti side-by-side nei sistemi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="274e2-108">In rare situations, both the 32-bit and 64-bit providers must run side-by-side on 64-bit systems.</span></span> <span data-ttu-id="274e2-109">In questo caso, la versione appropriata del provider che viene caricata varia a seconda che il chiamante sia a 32 bit o a 64 bit e locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="274e2-109">In this case, the appropriate version of provider that is loaded depends on whether the caller is 32-bit or 64-bit and local or remote.</span></span> <span data-ttu-id="274e2-110">Un chiamante che utilizza i flag di contesto dell'oggetto connessione, **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture**, può richiedere che WMI carichi un provider non predefinito.</span><span class="sxs-lookup"><span data-stu-id="274e2-110">A caller using the connection object context flags, **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture**, can request that WMI load a nondefault provider.</span></span> <span data-ttu-id="274e2-111">Per altre informazioni, vedere [ottenere e fornire dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="274e2-111">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="274e2-112">Nel caso insolito in cui è necessario eseguire i provider a 32 bit e a 64 bit side-by-Side, è necessario assicurarsi che gli scenari di installazione e disinstallazione vengano gestiti con cautela.</span><span class="sxs-lookup"><span data-stu-id="274e2-112">In the unusual case that you must run both the 32-bit and 64-bit providers side-by-side, then you must ensure that install and uninstall scenarios are handled carefully.</span></span> <span data-ttu-id="274e2-113">Poiché WMI dispone solo di un [*repository*](gloss-w.md) e le versioni a 32 bit e 64 bit di [**mofcomp.exe**](mofcomp.md) inserire i dati nello stesso repository. non esiste alcuna distinzione tra un file con estensione MOF a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="274e2-113">This is because WMI has only one [*repository*](gloss-w.md) and both the 32-bit and 64-bit versions of [**mofcomp.exe**](mofcomp.md) put the data in the same repository; there is no distinction between a 32-bit or a 64-bit .mof file.</span></span> <span data-ttu-id="274e2-114">La reinstallazione di una versione del provider non è danneggiata: verranno compilati i file con estensione MOF e le classi archiviate nel repository.</span><span class="sxs-lookup"><span data-stu-id="274e2-114">Reinstalling one version of the provider will not hurt: the .mof files will be compiled and the classes stored in the repository.</span></span> <span data-ttu-id="274e2-115">Tuttavia, una seconda disinstallazione che elimina uno spazio dei nomi può interferire con il funzionamento dell'altro provider.</span><span class="sxs-lookup"><span data-stu-id="274e2-115">However, a second uninstall that deletes a namespace can interfere with the operation of the other provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="274e2-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="274e2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="274e2-117">Ottenere e fornire dati in un computer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="274e2-117">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[<span data-ttu-id="274e2-118">Richiesta di dati WMI in una piattaforma a 64 bit</span><span class="sxs-lookup"><span data-stu-id="274e2-118">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="274e2-119">Invio di dati a WMI</span><span class="sxs-lookup"><span data-stu-id="274e2-119">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> </dl>

 

 



