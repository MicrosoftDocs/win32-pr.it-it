---
description: Accesso alle proprietà dell'oggetto servizio
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Accesso alle proprietà dell'oggetto servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306656"
---
# <a name="accessing-service-object-properties"></a><span data-ttu-id="87042-103">Accesso alle proprietà dell'oggetto servizio</span><span class="sxs-lookup"><span data-stu-id="87042-103">Accessing Service Object Properties</span></span>

<span data-ttu-id="87042-104">Un'applicazione può leggere e scrivere proprietà per un singolo oggetto in un servizio, per più oggetti identificati da identificatori di oggetto o per più oggetti dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="87042-104">An application can read and write properties for a single object on a service, for multiple objects identified by object identifiers, or for multiple objects of the same type.</span></span> <span data-ttu-id="87042-105">Nell'argomento [recupero delle proprietà dell'oggetto](retrieving-content-object-properties.md) vengono descritte le proprietà di lettura per un singolo oggetto in un servizio.</span><span class="sxs-lookup"><span data-stu-id="87042-105">The [Retrieving Object Properties](retrieving-content-object-properties.md) topic describes reading properties for a single object on a service.</span></span> <span data-ttu-id="87042-106">Nell'argomento [scrittura delle proprietà dell'oggetto](writing-content-object-properties.md) viene descritta la scrittura delle proprietà per un singolo oggetto in un servizio.</span><span class="sxs-lookup"><span data-stu-id="87042-106">The [Writing Object Properties](writing-content-object-properties.md) topic describes writing properties for a single object on a service.</span></span>

<span data-ttu-id="87042-107">Per una descrizione del recupero delle proprietà per più oggetti, vedere la sezione [attività avanzate](advanced-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="87042-107">Refer to the [Advanced Tasks](advanced-tasks.md) section for a description of property retrieval for multiple objects.</span></span>

## <a name="when-to-use-service-property-definitions"></a><span data-ttu-id="87042-108">Quando utilizzare le definizioni delle proprietà del servizio</span><span class="sxs-lookup"><span data-stu-id="87042-108">When to use Service Property Definitions</span></span>

<span data-ttu-id="87042-109">Le chiamate all'API WPD usate per il recupero e l'impostazione delle proprietà degli oggetti per un servizio sono le stesse chiamate per recuperare le proprietà dell'oggetto per un dispositivo (per un esempio, confrontare "recupero delle proprietà per un singolo oggetto").</span><span class="sxs-lookup"><span data-stu-id="87042-109">The WPD API calls used for retrieving and setting object properties for a service are the same as the calls for retrieving object properties for a device (compare "Retrieving Properties for a Single Object" for an example).</span></span> <span data-ttu-id="87042-110">La differenza principale consiste nel fatto che per eseguire query sulle proprietà degli oggetti viene utilizzato un set diverso di PROPERTYKEYs.</span><span class="sxs-lookup"><span data-stu-id="87042-110">The key difference is that a different set of PROPERTYKEYs are used to query object properties.</span></span> <span data-ttu-id="87042-111">Per WpdServiceApiSample, vengono usati PROPERTYKEYs del servizio del dispositivo (ad esempio, **pkey \_ GenericObj \_ Name**); per i WpdApiSample, vengono usati WPD PROPERTYKEYs, ad esempio il **\_ \_ nome dell'oggetto WPD**.</span><span class="sxs-lookup"><span data-stu-id="87042-111">For the WpdServiceApiSample, device service PROPERTYKEYs are used (such as **PKEY\_GenericObj\_Name**); for the WpdApiSample, WPD PROPERTYKEYs are used (such as **WPD\_OBJECT\_NAME**).</span></span>

<span data-ttu-id="87042-112">Il servizio Device PROPERTYKEYs è definito in BridgeDeviceServices. h (incluso in ogni file di intestazione del servizio) e rappresenta il set comune di PROPERTYKEYS usato dalle applicazioni di servizi per dispositivi e dall'implementazione del firmware nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87042-112">Device service PROPERTYKEYs are defined in BridgeDeviceServices.h (included by each service header file), and represent the common set of PROPERTYKEYS employed by both device services applications and the firmware implementation on the device.</span></span> <span data-ttu-id="87042-113">In questo modo è possibile ottenere un set coerente di definizioni in tutto lo stack del dispositivo con una conversione minima, raggruppare PROPERTYKEYs in base al servizio e consentire la definizione più semplice dei nuovi servizi senza dover aggiornare lo schema di WPD.</span><span class="sxs-lookup"><span data-stu-id="87042-113">This allows a consistent set of definitions throughout the device stack with minimal translation, groups PROPERTYKEYs based on the service, and enables new services to be more easily defined without having to update the WPD schema.</span></span>

<span data-ttu-id="87042-114">Il set di PROPERTYKEYs usato dipende dalle esigenze dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="87042-114">The set of PROPERTYKEYs used will depend on your application's needs:</span></span>

-   <span data-ttu-id="87042-115">Se l'applicazione sta comunicando con il dispositivo chiamando [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), usare il PROPERTYKEYs definito in portabledevice. h.</span><span class="sxs-lookup"><span data-stu-id="87042-115">If your application is communicating with the device by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use the PROPERTYKEYs defined in PortableDevice.h.</span></span> <span data-ttu-id="87042-116">Un esempio di tale applicazione è WpdApiSample.</span><span class="sxs-lookup"><span data-stu-id="87042-116">An example of such an application is the WpdApiSample.</span></span>
-   <span data-ttu-id="87042-117">Se l'applicazione sta comunicando con servizi dispositivo chiamando [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), usare il PROPERTYKEYS definito in BridgeDeviceServices. h.</span><span class="sxs-lookup"><span data-stu-id="87042-117">If your application is communicating with device services by calling [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use the PROPERTYKEYS defined in BridgeDeviceServices.h.</span></span> <span data-ttu-id="87042-118">Un esempio di tale applicazione è WpdServicesApiSample.</span><span class="sxs-lookup"><span data-stu-id="87042-118">An example of such an application is the WpdServicesApiSample.</span></span>
-   <span data-ttu-id="87042-119">Se si sta scrivendo un'applicazione complessa che deve supportare un ibrido di servizi per dispositivi e del dispositivo (ciò significa che l'applicazione chiama sia **IPortableDevice:: Open** che **IPortableDeviceService:: Open**), è necessario usare il PROPERTYKEYs WPD quando si usa IPortableDevice e le interfacce derivate e il servizio del dispositivo PROPERTYKEYs quando si usano [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) e le interfacce derivate.</span><span class="sxs-lookup"><span data-stu-id="87042-119">If you are writing a complex application that needs to support a hybrid of both device services and the device (this means your application calls both **IPortableDevice::Open** and **IPortableDeviceService::Open**), you will need to use the WPD PROPERTYKEYs when using IPortableDevice and its derived interfaces, and device service PROPERTYKEYs when using [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) and its derived interfaces.</span></span>

<span data-ttu-id="87042-120">La maggior parte delle applicazioni WPD deve rientrare nella prima o nella seconda categoria.</span><span class="sxs-lookup"><span data-stu-id="87042-120">Most WPD applications should fall into the first or second category.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87042-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87042-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87042-122">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="87042-122">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="87042-123">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="87042-123">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="87042-124">Recupero delle proprietà dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="87042-124">Retrieving Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="87042-125">Scrittura delle proprietà di un oggetto</span><span class="sxs-lookup"><span data-stu-id="87042-125">Writing Object Properties</span></span>](writing-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="87042-126">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="87042-126">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



