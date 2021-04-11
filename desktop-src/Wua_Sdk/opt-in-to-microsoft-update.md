---
description: È possibile scegliere un computer nel servizio Microsoft Update e quindi registrare il servizio con Aggiornamenti automatici.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128271"
---
# <a name="opt-in-to-microsoft-update"></a><span data-ttu-id="6263b-103">Opt-In Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="6263b-103">Opt-In to Microsoft Update</span></span>

<span data-ttu-id="6263b-104">È possibile scegliere un computer nel servizio Microsoft Update e quindi registrare il servizio con Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="6263b-104">You can opt a computer in to the Microsoft Update service and then register that service with Automatic Updates.</span></span>

<span data-ttu-id="6263b-105">Nell'esempio di scripting in questo argomento viene illustrato come utilizzare Windows Update Agent (WUA) per registrare il servizio Microsoft Update con Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="6263b-105">The scripting sample in this topic shows you how to use Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="6263b-106">In alternativa, per registrare il servizio, l'utente può visitare Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="6263b-106">Alternatively, to register the service, the user can visit Microsoft Update.</span></span>

<span data-ttu-id="6263b-107">Prima di provare a eseguire l'esempio, verificare che la versione di WUA installata nel computer sia la versione 7.0.6000 o una versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6263b-107">Before you attempt to run this sample, verify that the version of WUA that is installed on the computer is version 7.0.6000 or a later version.</span></span> <span data-ttu-id="6263b-108">Per ulteriori informazioni su come determinare la versione di WUA installata, vedere [determinazione della versione corrente di WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="6263b-108">For more information about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>

## <a name="example"></a><span data-ttu-id="6263b-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="6263b-109">Example</span></span>

<span data-ttu-id="6263b-110">Nell'esempio di scripting seguente viene illustrato come utilizzare l'agente di Windows Update (WUA) per registrare il servizio Microsoft Update con Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="6263b-110">The following scripting sample shows you how to use the Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="6263b-111">L'esempio consente l'elaborazione posticipata o offline, se necessario.</span><span class="sxs-lookup"><span data-stu-id="6263b-111">The sample allows deferred or offline processing if needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6263b-112">Questo script ha lo scopo di illustrare l'uso delle API dell'agente Windows Update e fornisce un esempio di come gli sviluppatori possono usare queste API per risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="6263b-112">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="6263b-113">Questo script non è destinato al codice di produzione e lo script non è supportato da Microsoft (anche se sono supportate le API di Windows Update Agent sottostanti).</span><span class="sxs-lookup"><span data-stu-id="6263b-113">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



<span data-ttu-id="6263b-114">Nelle versioni precedenti di WUA (una versione minima di WUA di 7.0.6000), è possibile semplificare il processo di consenso esplicito usando un'impostazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6263b-114">In earlier versions of WUA (a minimum WUA version of 7.0.6000), you can simplify the opt-in process by using a registry setting.</span></span> <span data-ttu-id="6263b-115">Dopo la configurazione della chiave e dei valori del registro di sistema, il Microsoft Update processo di consenso esplicito si verifica alla successiva esecuzione di una ricerca da parte di WUA.</span><span class="sxs-lookup"><span data-stu-id="6263b-115">After the registry key and values are configured, the Microsoft Update opt-in process occurs the next time WUA performs a search.</span></span> <span data-ttu-id="6263b-116">Il processo di consenso esplicito può essere attivato da Aggiornamenti automatici o da un chiamante dell'API.</span><span class="sxs-lookup"><span data-stu-id="6263b-116">The opt-in process may be triggered by Automatic Updates or by an API caller.</span></span>

<span data-ttu-id="6263b-117">Il percorso completo della chiave del registro di sistema e i valori da impostare per il processo di consenso esplicito, ad esempio, sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6263b-117">For example, the full path of the registry key and values to set for the opt-in process are as follows:</span></span>

<span data-ttu-id="6263b-118">**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **PendingServiceRegistration** \\ **7971f918-A847-4430-9279-4a52d1efe18d**</span><span class="sxs-lookup"><span data-stu-id="6263b-118">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**WindowsUpdate**\\**PendingServiceRegistration**\\**7971f918-a847-4430-9279-4a52d1efe18d**</span></span>

<span data-ttu-id="6263b-119">**ClientApplicationID** = app personale</span><span class="sxs-lookup"><span data-stu-id="6263b-119">**ClientApplicationID** = My App</span></span>

<span data-ttu-id="6263b-120">**RegisterWithAU** = 1</span><span class="sxs-lookup"><span data-stu-id="6263b-120">**RegisterWithAU** = 1</span></span>

> [!Note]
>
> <span data-ttu-id="6263b-121">La chiave del registro di sistema viene rispettata una volta solo quando WUA viene aggiornato da una versione precedente alla versione 7.0.6000 alla versione 7.0.6000 o a una versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6263b-121">The registry key is respected once only when WUA is updated from a version that is earlier than version 7.0.6000 to version 7.0.6000 or to a later version.</span></span> <span data-ttu-id="6263b-122">Quando si sovrascrivono i valori del registro di sistema esistenti, è consigliabile utilizzare la massima discrezione, in quanto la sovrascrittura dei valori può modificare il risultato di una richiesta di registrazione</span><span class="sxs-lookup"><span data-stu-id="6263b-122">We recommend discretion when overwriting existing registry values because overwriting the values may change the result of an earlier service registration request.</span></span>
>
> <span data-ttu-id="6263b-123">Per creare questa chiave del registro di sistema sono necessarie credenziali amministrative.</span><span class="sxs-lookup"><span data-stu-id="6263b-123">Creating this registry key requires administrative credentials.</span></span> <span data-ttu-id="6263b-124">Per Windows Vista, il chiamante deve creare la chiave del registro di sistema in un processo con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="6263b-124">For Windows Vista, the caller must create the registry key in an elevated process.</span></span>

 

 

 



