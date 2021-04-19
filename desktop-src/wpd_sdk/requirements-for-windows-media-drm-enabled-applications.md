---
description: Requisiti per le applicazioni Windows Media DRM-Enabled
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Requisiti per le applicazioni Windows Media DRM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320750"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a><span data-ttu-id="719d0-103">Requisiti per le applicazioni Windows Media DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="719d0-103">Requirements for Windows Media DRM-Enabled Applications</span></span>

<span data-ttu-id="719d0-104">Per creare un'applicazione Windows Media Digital Rights Management (DRM) abilitata, è necessario disporre delle intestazioni e delle librerie descritte nella sezione [requisiti generali per lo sviluppo di applicazioni](general-requirements-for-application-development.md) di questo documento.</span><span class="sxs-lookup"><span data-stu-id="719d0-104">To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document.</span></span> <span data-ttu-id="719d0-105">Inoltre, quando si apre il dispositivo, l'applicazione dovrà fornire proprietà aggiuntive nelle informazioni sul client.</span><span class="sxs-lookup"><span data-stu-id="719d0-105">In addition, the application will need to supply additional properties in the client information when opening the device.</span></span>

<span data-ttu-id="719d0-106">Nella tabella seguente sono descritte le due proprietà aggiuntive necessarie per abilitare i trasferimenti di contenuto protetti da DRM di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="719d0-106">The two additional properties that are required to enable Windows Media DRM-protected content transfers are described in the following table.</span></span>



| <span data-ttu-id="719d0-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="719d0-107">Property</span></span>                                      | <span data-ttu-id="719d0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="719d0-108">Description</span></span>                              |
|-----------------------------------------------|------------------------------------------|
| <span data-ttu-id="719d0-109">\_ \_ \_ chiave privata dell'applicazione \_ WMDRM \_ client WPD</span><span class="sxs-lookup"><span data-stu-id="719d0-109">WPD\_CLIENT\_WMDRM\_APPLICATION\_PRIVATE\_KEY</span></span> | <span data-ttu-id="719d0-110">Specifica la chiave privata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="719d0-110">Specifies the application's private key.</span></span> |
| <span data-ttu-id="719d0-111">\_ \_ \_ certificato applicazione WMDRM client \_ WPD</span><span class="sxs-lookup"><span data-stu-id="719d0-111">WPD\_CLIENT\_WMDRM\_APPLICATION\_CERTIFICATE</span></span>  | <span data-ttu-id="719d0-112">Specifica il certificato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="719d0-112">Specifies the application's certificate.</span></span> |



 

<span data-ttu-id="719d0-113">Queste proprietà devono essere specificate nelle informazioni sul client dell'applicazione quando il dispositivo viene aperto con il metodo [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .</span><span class="sxs-lookup"><span data-stu-id="719d0-113">These properties must be supplied in the application's client information when the device is opened with the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.</span></span> <span data-ttu-id="719d0-114">Quando queste proprietà vengono fornite, l'API WPD consente i trasferimenti di contenuto protetti.</span><span class="sxs-lookup"><span data-stu-id="719d0-114">When these properties are supplied, the WPD API allows protected content transfers.</span></span> <span data-ttu-id="719d0-115">Se l'applicazione ha fornito un certificato e una chiave privata, l'API creerà un canale sicuro per trasferire il contenuto WMDRM protetto al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="719d0-115">If the application has provided a certificate and private key, the API will create a secure channel to transfer protected WMDRM content to the device.</span></span>

<span data-ttu-id="719d0-116">Per informazioni sulla creazione e la distribuzione di applicazioni basate su Windows che supportano Windows Media DRM, vedere l'argomento relativo alle [applicazioni basate su Windows licensing](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .</span><span class="sxs-lookup"><span data-stu-id="719d0-116">For information about creating and distributing Windows-based applications that support Windows Media DRM, see the following [Licensing Windows-based Applications](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) topic.</span></span>

## <a name="transferring-content"></a><span data-ttu-id="719d0-117">Trasferimento di contenuto</span><span class="sxs-lookup"><span data-stu-id="719d0-117">Transferring Content</span></span>

<span data-ttu-id="719d0-118">Per trasferire il contenuto protetto con WMDRM, usare [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="719d0-118">To transfer WMDRM protected content, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="719d0-119">Questo metodo può essere utilizzato sia per il contenuto protetto che per quello non crittografato senza opzioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="719d0-119">This method can be used for both protected and clear content without additional options.</span></span> <span data-ttu-id="719d0-120">L'API WPD seleziona automaticamente il canale protetto o non crittografato, a seconda che il contenuto sia protetto o deselezionato.</span><span class="sxs-lookup"><span data-stu-id="719d0-120">The WPD API will automatically select the protected or clear channel depending on whether the content is protected or clear.</span></span> <span data-ttu-id="719d0-121">Si interfaccia con il provider di contenuti WMDRM sicuro per elaborare le licenze WMDRM.</span><span class="sxs-lookup"><span data-stu-id="719d0-121">It interfaces with the WMDRM Secure Content Provider to process the WMDRM licenses.</span></span>

## <a name="transferring-known-clear-content"></a><span data-ttu-id="719d0-122">Trasferimento di contenuto chiaro noto</span><span class="sxs-lookup"><span data-stu-id="719d0-122">Transferring Known Clear Content</span></span>

<span data-ttu-id="719d0-123">Se l'applicazione è stata abilitata per la gestione del contenuto protetto, ma si sa che un file specifico non è protetto, è possibile indicare a WPD di ignorare l'elaborazione DRM impostando l' **\_ opzione API WPD usa l'opzione \_ \_ \_ Cancella \_ \_ flusso di dati** su true nell'input **IPortableDeviceValues** quando si chiama [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) per il contenuto non crittografato.</span><span class="sxs-lookup"><span data-stu-id="719d0-123">If you've enabled your application to handle protected content, but you know that a specific file is not protected, you can tell WPD to skip the DRM processing by setting **WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM** option to TRUE in the input **IPortableDeviceValues** when calling [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) for clear content.</span></span>

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a><span data-ttu-id="719d0-124">Accesso alle operazioni di misurazione mediante IWMDRMDeviceApp</span><span class="sxs-lookup"><span data-stu-id="719d0-124">Accessing Metering Operations using IWMDRMDeviceApp</span></span>

<span data-ttu-id="719d0-125">WPD fornisce un meccanismo per accedere alle API **IWMDRMDeviceApp** per gli aggiornamenti delle licenze e il recupero dei dati di misurazione.</span><span class="sxs-lookup"><span data-stu-id="719d0-125">WPD provides a mechanism to access the **IWMDRMDeviceApp** APIs for license updates and metering data retrieval.</span></span> <span data-ttu-id="719d0-126">Per accedere a questa API tramite WPD, chiamare **QueryInterface** su **IID \_ IWMDRMDeviceApp** da **IStream** restituito da [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="719d0-126">To access this API through WPD, call **QueryInterface** on **IID\_IWMDRMDeviceApp** from the **IStream** returned from [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="719d0-127">Questa istanza di **IWMDRMDeviceApp** è associata alla connessione **IPortableDevice** al dispositivo compatibile con WMDRM e non al contenuto specifico in cui è stato ottenuto il **IStream** .</span><span class="sxs-lookup"><span data-stu-id="719d0-127">This **IWMDRMDeviceApp** instance tied to the **IPortableDevice** connection to your WMDRM-compatible device, and not the specific content where the **IStream** was obtained.</span></span> <span data-ttu-id="719d0-128">WPD esegue internamente il wrapping delle API di misurazione e le rende accessibili per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="719d0-128">WPD internally wraps the metering APIs and makes it accessible to your application.</span></span> <span data-ttu-id="719d0-129">L'applicazione deve usare WMDRMDEVICEAPP \_ per usare \_ la \_ costante PTR del dispositivo WPD \_ per il parametro *IWMDMDevice* \* .</span><span class="sxs-lookup"><span data-stu-id="719d0-129">Your application should use the WMDRMDEVICEAPP\_USE\_WPD\_DEVICE\_PTR constant for the *IWMDMDevice*\* parameter.</span></span>

<span data-ttu-id="719d0-130">Il frammento di codice seguente illustra questo problema.</span><span class="sxs-lookup"><span data-stu-id="719d0-130">The following code snippet demonstrates this.</span></span>


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



<span data-ttu-id="719d0-131">Lo stesso prerequisito con la chiave privata dell'applicazione e il certificato si applica anche qui.</span><span class="sxs-lookup"><span data-stu-id="719d0-131">The same pre-requisite with the application private key and certificate applies here as well.</span></span> <span data-ttu-id="719d0-132">Se la chiave o il certificato non è valido o l'inizializzazione del sistema WMDRM non riesce, la chiamata **QueryInferface** avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="719d0-132">If the key/certificate is invalid or if the WMDRM system fails to initialize, the **QueryInferface** call will fail.</span></span>

<span data-ttu-id="719d0-133">Il metodo precedente per acquisire l'interfaccia **IWMDRMDeviceApp** dal puntatore **IStream** è semplicemente una praticità se l'applicazione sta già eseguendo un trasferimento di contenuto protetto precedente, prima di procedere con le operazioni di misurazione e sincronizzazione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="719d0-133">The above method to acquire the **IWMDRMDeviceApp** interface from the **IStream** pointer is just a convenience if your application is already doing a prior protected content transfer, before proceeding on to do metering and license synchronization operations.</span></span>

<span data-ttu-id="719d0-134">Il suggerimento per la maggior parte delle applicazioni che devono accedere a **IWMDRMDeviceApp** è l'inizializzazione diretta di **IWMDRMDeviceApp** in quanto questa operazione non richiede che l'applicazione trasferisca contenuti protetti o mantenga le interfacce di trasferimento per eseguire la misurazione dei dispositivi e la sincronizzazione delle licenze. Questo metodo richiede l'utilizzo di API Windows Media Gestione dispositivi (WMDM).</span><span class="sxs-lookup"><span data-stu-id="719d0-134">Our recommendation for most applications that need to access **IWMDRMDeviceApp** is to initialize **IWMDRMDeviceApp** directly as this does not require your application to transfer protected content or hold on to the transfer interfaces in order to do device metering and license sync. This method will require usage of Windows Media Device Manager (WMDM) APIs.</span></span> <span data-ttu-id="719d0-135">Per informazioni dettagliate e per il codice di esempio, vedere il white paper relativo all' [accesso alle API WMDRM da un WPD dell'applicazione](../windows-portable-devices.md) nel sito di whdc.</span><span class="sxs-lookup"><span data-stu-id="719d0-135">For details and sample code, refer to the [Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) whitepaper on the WHDC site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="719d0-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="719d0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="719d0-137">**Dispositivi portatili Windows**</span><span class="sxs-lookup"><span data-stu-id="719d0-137">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
