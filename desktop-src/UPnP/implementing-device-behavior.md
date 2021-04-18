---
title: Implementazione del comportamento del dispositivo
description: Il comportamento di un dispositivo viene definito dai servizi esposti.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb702adf3ccb0f21bc71f08e98427cca15495f3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321002"
---
# <a name="implementing-device-behavior"></a><span data-ttu-id="a40a7-103">Implementazione del comportamento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="a40a7-103">Implementing Device Behavior</span></span>

<span data-ttu-id="a40a7-104">Il comportamento di un dispositivo viene definito dai servizi esposti.</span><span class="sxs-lookup"><span data-stu-id="a40a7-104">The behavior of a device is defined by the services it exposes.</span></span> <span data-ttu-id="a40a7-105">Ogni servizio dispone di una descrizione del servizio che ne elenca le azioni e le variabili di stato.</span><span class="sxs-lookup"><span data-stu-id="a40a7-105">Each service has a service description that lists its actions and state variables.</span></span> <span data-ttu-id="a40a7-106">Insieme, queste descrizioni del servizio costituiscono l'interfaccia del servizio, che definisce il modo in cui un punto di controllo può interagire con un servizio.</span><span class="sxs-lookup"><span data-stu-id="a40a7-106">Taken together, these service descriptions make up the service interface, which defines the way in which a control point can interact with a service.</span></span> <span data-ttu-id="a40a7-107">Ogni servizio deve avere almeno un'azione.</span><span class="sxs-lookup"><span data-stu-id="a40a7-107">Each service must have at least one action.</span></span>

<span data-ttu-id="a40a7-108">Per implementare un servizio, un dispositivo ospitato deve fornire un oggetto Component Object Model (COM) che espone l'interfaccia per il servizio.</span><span class="sxs-lookup"><span data-stu-id="a40a7-108">To implement a service, a hosted device must provide a Component Object Model (COM) object that exposes the interface for the service.</span></span> <span data-ttu-id="a40a7-109">Nella descrizione del servizio, le interfacce del servizio sono specificate in UPnP Template Language (UTL); Tuttavia, le interfacce oggetto COM vengono in genere specificate in IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="a40a7-109">In the service description, the service interfaces are specified in UPnP Template Language (UTL); however, COM object interfaces typically are specified in Interface Definition Language (IDL).</span></span> <span data-ttu-id="a40a7-110">È inoltre possibile specificare l'interfaccia COM in una libreria dei tipi o in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="a40a7-110">You can also specify the COM interface in a type library or header file.</span></span> <span data-ttu-id="a40a7-111">Il Software Development Kit (SDK) della piattaforma include lo strumento Utl2idl, che converte una descrizione del servizio in UTL in un'interfaccia COM in IDL.</span><span class="sxs-lookup"><span data-stu-id="a40a7-111">The Platform Software Development Kit (SDK) includes the Utl2idl tool, which translates a service description in UTL to a COM interface in IDL.</span></span>

<span data-ttu-id="a40a7-112">Gli esempi seguenti illustrano questo processo di conversione.</span><span class="sxs-lookup"><span data-stu-id="a40a7-112">The following samples illustrate this conversion process.</span></span> <span data-ttu-id="a40a7-113">La descrizione del servizio viene fornita dallo sviluppatore del dispositivo ed è scritta in UTL.</span><span class="sxs-lookup"><span data-stu-id="a40a7-113">The service description is provided by the device developer and is written in UTL.</span></span>

``` syntax
<?xml version="1.0" ?> 
  <scpd xmlns="urn:schemas-upnp-org:service-1-0">

    <specVersion>
      <major>1</major> 
      <minor>0</minor> 
    </specVersion>

    <serviceStateTable>
      <stateVariable>
        <name>Power</name> 
        <dataType>Boolean</dataType> 
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>Level</name> 
        <dataType>i4</dataType> 
        <allowedValueRange>
          <minimum>0</minimum> 
            <maximum>10</maximum> 
            <step>1</step> 
        </allowedValueRange>
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>State</name> 
        <dataType>string</dataType> 
        <allowedValueList>
          <allowedValue>ON</allowedValue> 
          <allowedValue>OFF</allowedValue> 
          <allowedValue>DIMMED</allowedValue> 
        </allowedValueList>
        <defaultValue>OFF</defaultValue> 
      </stateVariable>
    </serviceStateTable>

    <actionList>
      <action>
        <name>PowerOn</name> 
      </action>

      <action>
        <name>PowerOff</name> 
      </action>

      <action>
        <name>SetLevel</name> 
        <argumentList>
          <argument>
            <name>NewLevel</name> 
            <relatedStateVariable>Level</relatedStateVariable> 
            <direction>in</direction> 
          </argument>
          <argument>
            <name>NewState</name> 
            <relatedStateVariable>State</relatedStateVariable> 
            <direction>out</direction> 
          </argument>
        </argumentList>
      </action>

      <action>
        <name>IncreaseLevel</name> 
      </action>

      <action>
        <name>DecreaseLevel</name> 
      </action>
    </actionList>
</scpd>
```

<span data-ttu-id="a40a7-114">Il passaggio successivo consiste nell'eseguire lo strumento Utl2idl.</span><span class="sxs-lookup"><span data-stu-id="a40a7-114">The next step is to run the Utl2idl tool.</span></span> <span data-ttu-id="a40a7-115">Produce il file IDL che contiene l'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="a40a7-115">It produces the IDL file that contains the COM interface.</span></span> <span data-ttu-id="a40a7-116">Per ulteriori informazioni sui file IDL e sulla parola chiave **Interface** , vedere [**l'interfaccia e**](/windows/desktop/Midl/interface) il file di definizione dell' [interfaccia (IDL)](/windows/desktop/Midl/interface-definition-idl-file) in riferimento a MIDL.</span><span class="sxs-lookup"><span data-stu-id="a40a7-116">For more information about IDL files and the **interface** keyword, see [Interface Definition (IDL) File](/windows/desktop/Midl/interface-definition-idl-file) and [**interface**](/windows/desktop/Midl/interface) in the MIDL reference.</span></span>

``` syntax
#include <windows.h>
typedef [v1_enum] enum SCPD_DISPIDS
{
     DISPID_POWER = 1,
     DISPID_LEVEL,
     DISPID_STATE,
     DISPID_POWERON,
     DISPID_POWEROFF,
     DISPID_SETLEVEL,
     DISPID_INCREASELEVEL,
     DISPID_DECREASELEVEL
} SCPD_DISPIDS;

[
     uuid(68369839-960d-4c8c-8d0d-c319c69e73be),
     oleautomation,
     pointer_default(unique)
]
interface IUPnPService_scpd : IUnknown 
{
     [propget, id(DISPID_POWER), helpstring("Property Power")]
     HRESULT Power(
          [out, retval] VARIANT_BOOL *pPower);

     [propget, id(DISPID_LEVEL), helpstring("Property Level")]
     HRESULT Level(
          [out, retval] long *pLevel);

     [propget, id(DISPID_STATE), helpstring("Property State")]
     HRESULT State(
          [out, retval] BSTR *pState);

     [ id(DISPID_POWERON), helpstring("Method PowerOn")]
     HRESULT PowerOn();

     [ id(DISPID_POWEROFF), helpstring("Method PowerOff")]
     HRESULT PowerOff();

     [ id(DISPID_SETLEVEL), helpstring("Method SetLevel")]
     HRESULT SetLevel(
          [in] long NewLevel,
          [in, out] BSTR *pNewState;
                                
     [ id(DISPID_INCREASELEVEL), helpstring("Method IncreaseLevel")]
     HRESULT IncreaseLevel();

     [ id(DISPID_DECREASELEVEL), helpstring("Method DecreaseLevel")]
     HRESULT DecreaseLevel();
};
```

> [!Note]
> <span data-ttu-id="a40a7-117">Il valore restituito è il primo \[ \] parametro out nell'elenco di argomenti nella descrizione del servizio. Tuttavia, viene elencato come ultimo parametro dopo la conversione.</span><span class="sxs-lookup"><span data-stu-id="a40a7-117">The return value is the first \[out\] parameter in the list of arguments in the service description; however, it is listed as the last parameter after translation.</span></span>
> 
> <span data-ttu-id="a40a7-118">Tutti gli altri parametri rimangono nello stesso ordine.</span><span class="sxs-lookup"><span data-stu-id="a40a7-118">All other parameters remain in the same order.</span></span>

 

<span data-ttu-id="a40a7-119">Per fornire la funzionalità del servizio, implementare questa interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="a40a7-119">To provide the functionality of the service, implement this COM interface.</span></span>

## <a name="obtaining-information-about-an-endpoint"></a><span data-ttu-id="a40a7-120">Recupero di informazioni su un endpoint</span><span class="sxs-lookup"><span data-stu-id="a40a7-120">Obtaining Information About an Endpoint</span></span>

<span data-ttu-id="a40a7-121">Nel framework UPnP, le informazioni sull'endpoint includono informazioni su una richiesta e la relativa origine.</span><span class="sxs-lookup"><span data-stu-id="a40a7-121">In the UPnP framework, endpoint information includes information about a request and its source.</span></span> <span data-ttu-id="a40a7-122">Un dispositivo può esaminare queste informazioni per prendere una decisione sulla richiesta.</span><span class="sxs-lookup"><span data-stu-id="a40a7-122">A device can examine this information in order to make a decision about the request.</span></span>

<span data-ttu-id="a40a7-123">Facoltativamente, le informazioni sull'endpoint sono disponibili per il servizio implementato.</span><span class="sxs-lookup"><span data-stu-id="a40a7-123">Endpoint information is optionally available to the implemented service.</span></span> <span data-ttu-id="a40a7-124">L'host del dispositivo ha accesso alle informazioni sull'endpoint; Tuttavia, per impostazione predefinita, l'host del dispositivo non comunica le informazioni al servizio implementato.</span><span class="sxs-lookup"><span data-stu-id="a40a7-124">The device host has access to endpoint information; however, the device host does not communicate the information to the implemented service by default.</span></span> <span data-ttu-id="a40a7-125">È possibile abilitare l'host del dispositivo a condividere le informazioni sull'endpoint con il servizio implementato modificando l'interfaccia COM nel file IDL (prodotto dallo strumento Utl2idl).</span><span class="sxs-lookup"><span data-stu-id="a40a7-125">You can enable the device host to share the endpoint information with the implemented service by modifying the COM interface in the IDL file (produced by the Utl2idl tool).</span></span> <span data-ttu-id="a40a7-126">È possibile aggiungere un \[ \] parametro in a ogni metodo che richiede informazioni sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a40a7-126">You can add an \[in\] parameter to each method that requires endpoint information.</span></span> <span data-ttu-id="a40a7-127">Il \[ parametro in aggiuntivo \] deve essere il primo nell'elenco di argomenti, un puntatore a un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e denominato in modo esplicito **punkRemoteEndpointInfo**.</span><span class="sxs-lookup"><span data-stu-id="a40a7-127">The additional \[in\] parameter must be the first one in the list of arguments, a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, and explicitly named **punkRemoteEndpointInfo**.</span></span> <span data-ttu-id="a40a7-128">Le modifiche al codice XML del servizio non sono necessarie o sono consigliate.</span><span class="sxs-lookup"><span data-stu-id="a40a7-128">Modifications to the Service XML are not required, or recommended.</span></span> <span data-ttu-id="a40a7-129">Nell'esempio seguente viene illustrata la nuova definizione del metodo **PowerOn** quando viene modificata in modo da ricevere informazioni sull'endpoint:</span><span class="sxs-lookup"><span data-stu-id="a40a7-129">The following example shows the new definition of the **PowerOn** method when it is amended so that it receives endpoint information:</span></span>

<span data-ttu-id="a40a7-130">"HRESULT PowerOn ( \[ in \] IUnknown \* punkRemoteEndpointInfo);"</span><span class="sxs-lookup"><span data-stu-id="a40a7-130">"HRESULT PowerOn(\[in\] IUnknown \*punkRemoteEndpointInfo);"</span></span>

<span data-ttu-id="a40a7-131">Un puntatore a un oggetto informazioni endpoint, un'interfaccia [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) , viene passato tramite questo nuovo parametro dall'host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a40a7-131">A pointer to an endpoint information object, an [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface, is passed through this new parameter by the device host.</span></span> <span data-ttu-id="a40a7-132">L'interfaccia **IUPnPRemoteEndpointInfo** fornisce tre metodi per l'accesso alle informazioni sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a40a7-132">The **IUPnPRemoteEndpointInfo** interface provides three methods for accessing the endpoint information.</span></span> <span data-ttu-id="a40a7-133">È necessario chiamare il metodo appropriato per ottenere le informazioni sull'endpoint richieste dall'implementazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="a40a7-133">You must call the appropriate method to get the endpoint information that is required by the service implementation.</span></span>

<span data-ttu-id="a40a7-134">In alternativa alla modifica manuale dell'interfaccia COM, è possibile usare lo strumento Utl2idl con l'opzione **-ci** .</span><span class="sxs-lookup"><span data-stu-id="a40a7-134">As an alternative to manual modification of the COM interface, you can use the Utl2idl tool with the **-ci** switch.</span></span> <span data-ttu-id="a40a7-135">Questa opzione consente allo strumento di aggiungere il parametro informazioni endpoint a ognuno dei metodi dell'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="a40a7-135">This switch causes the tool to add the endpoint information parameter to each of the methods in the COM interface.</span></span> <span data-ttu-id="a40a7-136">L'uso dell'opzione **-ci** non semplifica la modifica dei singoli metodi.</span><span class="sxs-lookup"><span data-stu-id="a40a7-136">Using the **-ci** switch does not facilitate modification of individual methods.</span></span> <span data-ttu-id="a40a7-137">Se le informazioni sull'endpoint non sono necessarie per tutti i metodi di un'interfaccia, è necessario aggiungere il parametro manualmente per produrre le implementazioni più efficienti.</span><span class="sxs-lookup"><span data-stu-id="a40a7-137">If endpoint information is not needed by all methods of an interface, you should add the parameter manually in order to produce the most efficient implementations.</span></span>

## <a name="implementing-a-service-object"></a><span data-ttu-id="a40a7-138">Implementazione di un oggetto servizio</span><span class="sxs-lookup"><span data-stu-id="a40a7-138">Implementing a Service Object</span></span>

<span data-ttu-id="a40a7-139">È necessario usare lo strumento Utl2idl per tradurre la descrizione di ogni servizio di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a40a7-139">You must use the Utl2idl tool to translate each service description of a device.</span></span>

<span data-ttu-id="a40a7-140">Un oggetto che fornisce la funzionalità per un servizio viene definito [*oggetto servizio*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a40a7-140">An object that provides the functionality for a service is referred to as a [*service object*](s-gly.md).</span></span> <span data-ttu-id="a40a7-141">Oltre a fornire la funzionalità del servizio, gli oggetti servizio gestiscono gli errori usando l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a40a7-141">In addition to providing service functionality, service objects handle errors by using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a40a7-142">Per altre informazioni, vedere [uso dell'API host del dispositivo con la tecnologia UPnP](using-the-device-host-api-with-upnp-technology.md).</span><span class="sxs-lookup"><span data-stu-id="a40a7-142">For more information, see [Using the Device Host API with UPnP Technology](using-the-device-host-api-with-upnp-technology.md).</span></span>

<span data-ttu-id="a40a7-143">Per garantire la compatibilità con Visual Basic, che non supporta \[ \] i parametri out, i parametri **/Direction** della **direzione** out nella descrizione del servizio vengono convertiti in \[ parametri out in \] IDL.</span><span class="sxs-lookup"><span data-stu-id="a40a7-143">To ensure compatibility with Visual Basic, which does not support \[out\] parameters, the **direction** out **/direction** parameters in the service description are converted to \[in, out\] parameters in IDL.</span></span> <span data-ttu-id="a40a7-144">Il server deve liberarsi \[ nei parametri out \] .</span><span class="sxs-lookup"><span data-stu-id="a40a7-144">The server must free these \[in, out\] parameters.</span></span>

## <a name="implementing-a-device-control-object"></a><span data-ttu-id="a40a7-145">Implementazione di un oggetto controllo dispositivo</span><span class="sxs-lookup"><span data-stu-id="a40a7-145">Implementing a Device Control Object</span></span>

<span data-ttu-id="a40a7-146">Oltre a implementare oggetti servizio, è necessario implementare un [*oggetto controllo dispositivo*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a40a7-146">In addition to implementing service objects, you must implement a [*device control object*](d-gly.md).</span></span> <span data-ttu-id="a40a7-147">Un oggetto controllo dispositivo è il punto centrale di gestione e controllo per gli oggetti servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a40a7-147">A device control object is the central point of management and control for the device's service objects.</span></span> <span data-ttu-id="a40a7-148">Al momento della registrazione, l'oggetto controllo dispositivo viene passato all'host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a40a7-148">At registration time, the device control object is passed to the device host.</span></span> <span data-ttu-id="a40a7-149">Quando viene ricevuta una sottoscrizione o una richiesta di controllo di un evento per uno dei servizi del dispositivo, l'host del dispositivo chiama questo oggetto controllo dispositivo per ottenere l'oggetto servizio pertinente.</span><span class="sxs-lookup"><span data-stu-id="a40a7-149">When an event subscription or control request arrives for one of the device's services, the device host calls into this device control object to obtain the relevant service object.</span></span> <span data-ttu-id="a40a7-150">A questo punto, l'oggetto controllo dispositivo crea un'istanza dell'oggetto servizio o restituisce l'interfaccia di un'istanza esistente dell'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="a40a7-150">At that time, the device control object either creates an instance of the service object or returns the interface of an existing instance of the service object.</span></span>

<span data-ttu-id="a40a7-151">È possibile registrare una descrizione del dispositivo su più computer o più volte nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="a40a7-151">You can register a device description on multiple computers or multiple times on the same computer.</span></span> <span data-ttu-id="a40a7-152">Poiché il nome univoco del dispositivo (UDN) deve essere diverso per ogni istanza del dispositivo, l'host del dispositivo genera un UDN univoco per ogni dispositivo e dispositivo incorporato ogni volta che il dispositivo viene registrato.</span><span class="sxs-lookup"><span data-stu-id="a40a7-152">Because the Unique Device Name (UDN) must be different for each instance of the device, the device host generates a unique UDN for each device and embedded device each time the device is registered.</span></span> <span data-ttu-id="a40a7-153">Usare il UDN specificato nel modello di descrizione del dispositivo per ottenere il UDN effettivo generato dall'host del dispositivo e associato al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a40a7-153">Use the UDN specified in the device description template to obtain the actual UDN generated by the device host and associated with the device.</span></span> <span data-ttu-id="a40a7-154">Per annullare la registrazione di un dispositivo, è necessario usare l'ID fornito dal framework UPnP quando il dispositivo è stato registrato.</span><span class="sxs-lookup"><span data-stu-id="a40a7-154">To unregister a device, you must use the ID provided by the UPnP framework when the device was registered.</span></span>

<span data-ttu-id="a40a7-155">Gli oggetti controllo dispositivo devono implementare l'interfaccia [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="a40a7-155">Device control objects must implement the [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) interface.</span></span> <span data-ttu-id="a40a7-156">L'host del dispositivo richiama il metodo [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) dell'oggetto controllo del dispositivo, passando la descrizione del dispositivo basata su UPnP che l'host del dispositivo ha pubblicato in precedenza per il dispositivo e una stringa di inizializzazione specificata in fase di registrazione. vedere [registrazione di un dispositivo ospitato con l'host del dispositivo](registering-a-hosted-device-with-the-device-host.md).</span><span class="sxs-lookup"><span data-stu-id="a40a7-156">The device host invokes the [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method of the device control object, passing in the UPnP-based device description that the device host previously published for the device and an initialization string that was specified at registration time (see [Registering a Hosted Device with the Device Host](registering-a-hosted-device-with-the-device-host.md)).</span></span> <span data-ttu-id="a40a7-157">Da questa descrizione del dispositivo, l'oggetto controllo dispositivo legge il UDNs assegnato a ognuno dei dispositivi nell'albero del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a40a7-157">From this device description, the device control object reads the UDNs assigned to each of the devices in the device tree.</span></span> <span data-ttu-id="a40a7-158">Per ottenere queste informazioni, è anche possibile usare il metodo [**IUPnPRegistrar:: GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) .</span><span class="sxs-lookup"><span data-stu-id="a40a7-158">You can also use the [**IUPnPRegistrar::GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) method to obtain this information.</span></span>

<span data-ttu-id="a40a7-159">Quando l'host del dispositivo richiede un puntatore a un oggetto servizio che implementa un determinato servizio, richiama il metodo [**IUPnPDeviceControl:: GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) sull'oggetto controllo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a40a7-159">When the device host requires a pointer to a service object that implements a particular service, it invokes the [**IUPnPDeviceControl::GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) method on the device control object.</span></span> <span data-ttu-id="a40a7-160">L'host del dispositivo passa il UDN e l'ID del servizio per il quale richiede un oggetto servizio e l'indirizzo di un puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in corrispondenza del quale si prevede che il metodo restituisca un puntatore all'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="a40a7-160">The device host passes the UDN and the service ID of the service for which it is requesting a service object and the address of an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer at which the method is expected to return a pointer to the service object.</span></span> <span data-ttu-id="a40a7-161">Il parametro UDN è necessario perché l'oggetto controllo dispositivo gestisce i servizi per l'intero albero dei dispositivi, inclusi i dispositivi annidati.</span><span class="sxs-lookup"><span data-stu-id="a40a7-161">The UDN parameter is necessary because the device control object manages services for the entire device tree, including nested devices.</span></span> <span data-ttu-id="a40a7-162">Se l'host del dispositivo richiede un dispositivo annidato, **GetServiceObject** usa il UDN per identificarlo.</span><span class="sxs-lookup"><span data-stu-id="a40a7-162">If the device host requests a nested device, **GetServiceObject** uses the UDN to identify it.</span></span>

 

 