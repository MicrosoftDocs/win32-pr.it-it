---
title: Presentazione
description: Presentazione è il passaggio finale del processo UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855958"
---
# <a name="presentation"></a><span data-ttu-id="89c37-103">Presentazione</span><span class="sxs-lookup"><span data-stu-id="89c37-103">Presentation</span></span>

<span data-ttu-id="89c37-104">Presentazione è il passaggio finale del processo UPnP.</span><span class="sxs-lookup"><span data-stu-id="89c37-104">Presentation is the final step in the UPnP process.</span></span> <span data-ttu-id="89c37-105">Se un dispositivo ha un URL per la presentazione, un punto di controllo può recuperare una pagina da questo URL e caricare la pagina in un browser.</span><span class="sxs-lookup"><span data-stu-id="89c37-105">If a device has a URL for presentation, a control point can retrieve a page from this URL and load the page into a browser.</span></span> <span data-ttu-id="89c37-106">A seconda delle funzionalità della pagina di presentazione e del dispositivo, il punto di controllo può controllare il dispositivo e visualizzare lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89c37-106">Depending on the capabilities of the presentation page and the device, the control point can control the device and view the status of the device.</span></span>

<span data-ttu-id="89c37-107">Il percorso della risorsa, che viene passato a [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) durante la registrazione, è la posizione in cui si trovano tutti i file rilevanti per la presentazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89c37-107">The resource path, which is passed to [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) during registration, is where all the files relevant to the presentation of the device are located.</span></span> <span data-ttu-id="89c37-108">Gli sviluppatori di dispositivi possono fornire pagine separate per ogni dispositivo incorporato.</span><span class="sxs-lookup"><span data-stu-id="89c37-108">Device developers can provide separate pages for each embedded device.</span></span> <span data-ttu-id="89c37-109">L'URL di presentazione nel modello di descrizione del dispositivo può essere un URL assoluto o un URL relativo.</span><span class="sxs-lookup"><span data-stu-id="89c37-109">The presentation URL in the device description template can either be an absolute URL or a relative URL.</span></span> <span data-ttu-id="89c37-110">Per gli URL relativi, che sono relativi al percorso della risorsa, il modello di descrizione del dispositivo deve contenere un nome file.</span><span class="sxs-lookup"><span data-stu-id="89c37-110">For relative URLs, which are relative to the resource path, the device description template should contain a file name.</span></span> <span data-ttu-id="89c37-111">**IUPnPRegistrar** converte questo oggetto in un URL con il percorso effettivo.</span><span class="sxs-lookup"><span data-stu-id="89c37-111">**IUPnPRegistrar** converts this to a URL with the actual location.</span></span> <span data-ttu-id="89c37-112">Per gli URL assoluti, il percorso non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="89c37-112">For absolute URLs, the location is not modified.</span></span>

<span data-ttu-id="89c37-113">Per supportare gli script sul lato client all'interno di una pagina di presentazione, le informazioni aggiuntive vengono in genere aggiunte all'URL sotto forma di "stringa di query".</span><span class="sxs-lookup"><span data-stu-id="89c37-113">To support client side scripts within a presentation page, extra information is normally appended to the URL in the form of a "query string".</span></span> <span data-ttu-id="89c37-114">Le informazioni aggiuntive aggiunte sono l'URL del documento di descrizione del dispositivo e il UDN del dispositivo o del dispositivo incorporato.</span><span class="sxs-lookup"><span data-stu-id="89c37-114">The extra information that is appended is the URL to the device description document, and the UDN of the device or embedded device.</span></span> <span data-ttu-id="89c37-115">L'URL della descrizione del dispositivo può essere usato per caricare un documento di descrizione nello script, quindi controllare il dispositivo tramite i servizi.</span><span class="sxs-lookup"><span data-stu-id="89c37-115">The device description URL can be used to load a description document in the script, and then control the device through its services.</span></span> <span data-ttu-id="89c37-116">UDN viene usato per selezionare un dispositivo incorporato dal dispositivo radice.</span><span class="sxs-lookup"><span data-stu-id="89c37-116">The UDN is used to select an embedded device from the root device.</span></span>

<span data-ttu-id="89c37-117">Il formato dell'URL di presentazione modificato è: l'URL di presentazione effettivo, un punto interrogativo ("?"), l'URL Descrizione dispositivo, un segno più ("+"), il dispositivo UDN.</span><span class="sxs-lookup"><span data-stu-id="89c37-117">The format of the modified presentation URL is: the actual presentation URL, a question mark ("?"), the device description URL, a plus sign ("+"), the device UDN.</span></span> <span data-ttu-id="89c37-118">Il punto interrogativo indica l'inizio della stringa di query.</span><span class="sxs-lookup"><span data-stu-id="89c37-118">The question mark denotes the start of the query string.</span></span>

<span data-ttu-id="89c37-119">Se l'URL di presentazione nel modello di descrizione del dispositivo è un URL assoluto e contiene già un punto interrogativo ("?"), le informazioni aggiuntive non vengono aggiunte all'URL della presentazione.</span><span class="sxs-lookup"><span data-stu-id="89c37-119">If the presentation URL in the device description template was an absolute URL and it already contained a question mark ("?"), then the extra information is not added to the presentation URL.</span></span>



| <span data-ttu-id="89c37-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89c37-120">Description</span></span>                        | <span data-ttu-id="89c37-121">URL</span><span class="sxs-lookup"><span data-stu-id="89c37-121">URL</span></span>                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c37-122">Nel modello di descrizione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="89c37-122">In the device description template</span></span> | <span data-ttu-id="89c37-123">**presentationURL** MyDevice.html **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="89c37-123">**presentationURL** MyDevice.html **/presentationURL**</span></span>                                                                                              |
| <span data-ttu-id="89c37-124">Generato dall'host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="89c37-124">Generated by the device host</span></span>       | <span data-ttu-id="89c37-125">**presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ...</span><span class="sxs-lookup"><span data-stu-id="89c37-125">**presentationURL**https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394…</span></span> <span data-ttu-id="89c37-126">+ UDN **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="89c37-126">+ UDN **/presentationURL**</span></span> |



 

<span data-ttu-id="89c37-127">Uno script lato client potrebbe dover estrarre l'URL della descrizione del dispositivo dall'URL di presentazione per caricare l'oggetto [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="89c37-127">A client-side script may have to extract the device description URL from the presentation URL to load the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) object.</span></span> <span data-ttu-id="89c37-128">Questa operazione viene eseguita prendendo la stringa di query e terminando il segno più ("+").</span><span class="sxs-lookup"><span data-stu-id="89c37-128">This is done by taking the query string, and terminating it at the plus sign ("+").</span></span>


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



<span data-ttu-id="89c37-129">Nel caso di una pagina di presentazione per un dispositivo incorporato, sono necessarie alcune operazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89c37-129">In the case of a presentation page for an embedded device, some additional work is required.</span></span> <span data-ttu-id="89c37-130">Dopo aver caricato il [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), lo script deve ottenere la raccolta di dispositivi incorporati, quindi selezionare il dispositivo che corrisponde a UDN nella stringa di query.</span><span class="sxs-lookup"><span data-stu-id="89c37-130">After loading the [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), the script must obtain the collection of embedded devices, then select the device that matches the UDN in the query string.</span></span> <span data-ttu-id="89c37-131">Lo script seguente mostra come selezionare il dispositivo incorporato per la pagina di presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="89c37-131">The following script shows how to select the embedded device for the current presentation page.</span></span> <span data-ttu-id="89c37-132">Si presuppone che LightDesc sia già caricato.</span><span class="sxs-lookup"><span data-stu-id="89c37-132">It assumes LightDesc is already loaded.</span></span>


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




