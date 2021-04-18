---
description: Supporto del proxy per le origini di rete
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Supporto del proxy per le origini di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309023"
---
# <a name="proxy-support-for-network-sources"></a><span data-ttu-id="7b3dd-103">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="7b3dd-103">Proxy Support for Network Sources</span></span>

<span data-ttu-id="7b3dd-104">Un server proxy è un server intermedio tra la rete Intranet e Internet, che instrada le richieste dall'applicazione client al server multimediale e recupera i file dal server multimediale.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-104">A proxy server is an intermediate server between your intranet and the Internet, which routes requests from the client application to the media server and retrieves files from the media server.</span></span>

<span data-ttu-id="7b3dd-105">Media Foundation crea in modo implicito un oggetto *localizzatore proxy* quando un'applicazione client tenta di accedere a un URL di origine.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-105">Media Foundation implicitly creates a *proxy locator* object when a client application tries to access a source URL.</span></span> <span data-ttu-id="7b3dd-106">L'oggetto localizzatore proxy espone l'interfaccia [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="7b3dd-106">The proxy locator object exposes the [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) interface.</span></span> <span data-ttu-id="7b3dd-107">Durante la risoluzione del codice sorgente, Media Foundation controlla l'archivio delle proprietà passato al metodo del resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-107">During source resolution, Media Foundation checks the property store passed to the source resolver method.</span></span>

<span data-ttu-id="7b3dd-108">Se l'archivio delle proprietà contiene la proprietà [ \_ PROXYLOCATORFACTORY di MFNETSOURCE](mfnetsource-proxylocatorfactory-property.md) impostata su un oggetto factory del localizzatore proxy implementato dall'applicazione, richiama il metodo [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) per creare un localizzatore proxy con impostazioni di configurazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-108">If the property store contains the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property set to a proxy locator factory object implemented by the application then, it invokes the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method to create a proxy locator with custom configuration settings.</span></span>

<span data-ttu-id="7b3dd-109">Se l'archivio delle proprietà non è impostato, Media Foundation crea il localizzatore proxy con la configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-109">If the property store is not set, then Media Foundation creates the proxy locator with default configuration.</span></span> <span data-ttu-id="7b3dd-110">Queste impostazioni sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b3dd-110">These settings are as follows:</span></span>

-   <span data-ttu-id="7b3dd-111">Se è impostato un criterio utente, il localizzatore proxy usa le impostazioni specificate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-111">If user policy is set, then the proxy locator uses settings specified in the registry.</span></span>

-   <span data-ttu-id="7b3dd-112">Per HTTP, il localizzatore proxy usa le impostazioni del proxy del browser.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-112">For HTTP, the proxy locator uses browser proxy settings.</span></span>

-   <span data-ttu-id="7b3dd-113">Per RTSP, il localizzatore proxy è configurato in modo da ignorare i server proxy durante la connessione al server multimediale.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-113">For RTSP, the proxy locator is configured to bypass proxy servers when connecting to the media server.</span></span>

<span data-ttu-id="7b3dd-114">Questa configurazione predefinita può essere modificata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-114">This default configuration can be changed by the application.</span></span> <span data-ttu-id="7b3dd-115">Gli argomenti seguenti contengono informazioni sulle impostazioni di configurazione per un localizzatore proxy:</span><span class="sxs-lookup"><span data-stu-id="7b3dd-115">The following topics contain information about the configuration settings for a proxy locator:</span></span>

-   [<span data-ttu-id="7b3dd-116">Impostazioni di configurazione del localizzatore proxy</span><span class="sxs-lookup"><span data-stu-id="7b3dd-116">Proxy Locator Configuration Settings</span></span>](proxy-locator-configuration-settings.md)

-   [<span data-ttu-id="7b3dd-117">Come configurare il localizzatore proxy</span><span class="sxs-lookup"><span data-stu-id="7b3dd-117">How to Configure the Proxy Locator</span></span>](how-to-configure-the-proxy-locator.md)

<span data-ttu-id="7b3dd-118">Media Foundation Inizializza il localizzatore proxy per l'URL di origine specificato nel [resolver di origine](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="7b3dd-118">Media Foundation initializes the proxy locator for the source URL specified to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="7b3dd-119">Il localizzatore proxy rileva un server proxy da usare in base alle impostazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-119">The proxy locator detects a proxy server to use based on configuration settings.</span></span> <span data-ttu-id="7b3dd-120">Quando il localizzatore proxy tenta il set di un server proxy, registra il risultato dell'esito positivo o negativo nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-120">When the proxy locator attempts the set a proxy server, it records the success or failure result in the registry.</span></span> <span data-ttu-id="7b3dd-121">Questo valore viene verificato durante il successivo processo di rilevamento del proxy.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-121">This value is checked during the next proxy detection process.</span></span> <span data-ttu-id="7b3dd-122">Se è noto che un determinato server proxy ha causato errori in passato, il localizzatore proxy lo ignora.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-122">If a certain proxy server is known to have caused failures in the past, the proxy locator skips it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b3dd-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b3dd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b3dd-124">Attributi e proprietà</span><span class="sxs-lookup"><span data-stu-id="7b3dd-124">Attributes and Properties</span></span>](attributes-and-properties.md)
</dt> <dt>

[<span data-ttu-id="7b3dd-125">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b3dd-125">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



