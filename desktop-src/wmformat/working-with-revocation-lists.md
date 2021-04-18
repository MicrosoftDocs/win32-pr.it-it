---
title: Utilizzo degli elenchi di revoche
description: Utilizzo degli elenchi di revoche
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows Media Format SDK, elenchi di revoche
- ASF (Advanced Systems Format), elenchi di revoche
- ASF (Advanced Systems Format), elenchi di revoche
- elenchi di revoche
- Digital Rights Management (DRM), elenchi di revoche
- DRM (Digital Rights Management), elenchi di revoche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516579"
---
# <a name="working-with-revocation-lists"></a><span data-ttu-id="1c4aa-109">Utilizzo degli elenchi di revoche</span><span class="sxs-lookup"><span data-stu-id="1c4aa-109">Working with Revocation Lists</span></span>

<span data-ttu-id="1c4aa-110">Per rispondere alle violazioni della sicurezza e garantire che le applicazioni dei giocatori note siano interrotte o compromesse non possano riprodurre o usare file protetti, ogni licenza rilasciata contiene un elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-110">To respond to security breaches and to ensure that player applications known to be broken or compromised cannot play or use protected files, each license that is issued contains a revocation list.</span></span> <span data-ttu-id="1c4aa-111">Un elenco di revoche contiene i certificati dell'applicazione di tutte le applicazioni del lettore note come interrotte o danneggiate.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-111">A revocation list contains the application certificates of all those player applications known to be broken or corrupted.</span></span> <span data-ttu-id="1c4aa-112">Quando viene ricevuta una nuova licenza, il componente DRM dell'applicazione Player verifica la presenza di un elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-112">When a new license is received, the DRM component of the player application checks for a revocation list.</span></span> <span data-ttu-id="1c4aa-113">Se ne viene trovato uno più recente rispetto a quello attualmente presente nel computer, viene archiviato l'elenco più recente.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-113">If one is found that is newer than the one currently on the computer, the newer list is stored.</span></span> <span data-ttu-id="1c4aa-114">Alla successiva riproduzione di un file ASF protetto da parte del consumer, il componente DRM confronta l'applicazione Player con l'elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-114">The next time the consumer plays a protected ASF file, the DRM component compares the player application to the revocation list.</span></span> <span data-ttu-id="1c4aa-115">Se l'applicazione del lettore viene revocata, il componente DRM Invia un messaggio di errore all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-115">If the player application is revoked, the DRM component sends an error message to the application.</span></span>

<span data-ttu-id="1c4aa-116">Le applicazioni Player possono ricevere un messaggio di errore di revoca negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="1c4aa-116">Player applications can receive a revocation error message in the following scenarios:</span></span>

-   <span data-ttu-id="1c4aa-117">Il messaggio di errore viene ricevuto dopo che l'applicazione chiama il metodo [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) per un file protetto.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-117">The error message is received after the application calls the [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) method for a protected file.</span></span> <span data-ttu-id="1c4aa-118">La chiamata ha esito negativo con il codice **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revocato, fornito alla funzione di callback **OnStatus** con \_ \_ lo stato della licenza WMT Acquire.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-118">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the **OnStatus** callback function with WMT\_ACQUIRE\_LICENSE status.</span></span> <span data-ttu-id="1c4aa-119">Se questo codice **HRESULT** viene ignorato, gli errori continueranno a verificarsi.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-119">If this **HRESULT** code is ignored, errors will continue to occur.</span></span>
-   <span data-ttu-id="1c4aa-120">Il messaggio di errore viene ricevuto quando l'applicazione crea il lettore abilitato per DRM e chiama il metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) per un file protetto.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-120">The error message is received when the application creates the DRM-enabled reader and calls the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method for a protected file.</span></span> <span data-ttu-id="1c4aa-121">La chiamata ha esito negativo con il codice **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revocato, fornito al metodo [**IWMSTATUSCALLBACK:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback con WMT \_ opened status.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-121">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method with WMT\_OPENED status.</span></span> <span data-ttu-id="1c4aa-122">Quando un'applicazione lettore riceve questo messaggio di errore, l'applicazione deve informare gli utenti finali e fornire un modo per ripristinare le funzionalità al lettore.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-122">When a player application receives this error message, the application should notify end users and provide a way for them to restore functionality to their player.</span></span> <span data-ttu-id="1c4aa-123">Ad esempio, l'applicazione può aprire un URL in cui gli utenti finali possono scaricare un aggiornamento per l'applicazione compromessa.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-123">For example, the application can open a URL where end users can download an upgrade for the compromised application.</span></span>

<span data-ttu-id="1c4aa-124">**Nota** Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="1c4aa-124">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c4aa-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c4aa-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c4aa-126">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="1c4aa-126">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="1c4aa-127">**Gestione degli eventi di acquisizione delle licenze**</span><span class="sxs-lookup"><span data-stu-id="1c4aa-127">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> </dl>

 

 




