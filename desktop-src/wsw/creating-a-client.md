---
title: Creazione di un client
description: La creazione di un client per i servizi Web è molto semplificata in WWSAPI dall'API del modello di servizio e dallo strumento WsUtil.exe.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396851"
---
# <a name="creating-a-client"></a><span data-ttu-id="bdc4a-103">Creazione di un client</span><span class="sxs-lookup"><span data-stu-id="bdc4a-103">Creating a Client</span></span>

<span data-ttu-id="bdc4a-104">La creazione di un client per i servizi Web è molto semplificata in WWSAPI dall'API del [modello di servizio](service-model-layer-overview.md) e dallo strumento [WsUtil.exe](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc4a-104">Creating a client for Web services is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="bdc4a-105">Il modello di servizio fornisce un'API che consente al client di inviare e ricevere [messaggi](message.md) tramite un [canale](channel.md) come chiamate al metodo C.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-105">The Service Model provides an API that enables the client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="bdc4a-106">Lo strumento WsUtil genera intestazioni e helper per l'implementazione del client.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-106">The WsUtil tool generates headers and helpers for implementing the client.</span></span> <span data-ttu-id="bdc4a-107">Queste intestazioni includono i tipi e i prototipi di funzione per le funzioni C che rappresentano i servizi offerti dal servizio Web di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-107">These headers include the types and function prototypes for C functions representing the services offered by the target Web service.</span></span> <span data-ttu-id="bdc4a-108">Gli helper vengono utilizzati per creare il proxy del servizio, che contiene le informazioni di associazione e l' [indirizzo endpoint](endpoint-address.md) per il servizio.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-108">The helpers are used to create the service proxy, which contains the binding information and [endpoint address](endpoint-address.md) for the service.</span></span>

## <a name="using-wsutil-to-generate-headers-and-helpers"></a><span data-ttu-id="bdc4a-109">Uso di WsUtil per generare intestazioni e helper</span><span class="sxs-lookup"><span data-stu-id="bdc4a-109">Using WsUtil to Generate Headers and Helpers</span></span>

<span data-ttu-id="bdc4a-110">Per generare le intestazioni e gli helper, WsUtil apre e legge i file di metadati per il servizio di destinazione, ovvero i file WSDL e XSD, e li converte in intestazioni. Pertanto, è necessario recuperare i file di metadati per il servizio di destinazione in anticipo, ad esempio usando SvcUtil, una parte del Windows Communication Foundation.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-110">To generate the headers and helpers, WsUtil opens and reads the metadata files for the target service — wsdl and xsd files— and converts them into headers; therefore, it is necessary to retrieve the metadata files for the target service in advance, for example by using SvcUtil, a part of the Windows Communication Foundation.</span></span> <span data-ttu-id="bdc4a-111">Per motivi di sicurezza, è fondamentale che le copie di questi file siano affidabili.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-111">For security reasons, it is imperative that your copies of these files are trustworthy.</span></span> <span data-ttu-id="bdc4a-112">Per ulteriori informazioni, vedere la sezione "sicurezza" dell'argomento dello [strumento del compilatore WsUtil](wsutil-compiler-tool.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc4a-112">(For more information, see the "Security" section of the [WsUtil Compiler Tool](wsutil-compiler-tool.md) topic.)</span></span>

<span data-ttu-id="bdc4a-113">Per eseguire WsUtil, utilizzare la sintassi della riga di comando seguente se i file WSDL e XSD per il servizio si trovano nella propria directory: `WsUtil.exe *.wsdl *.xsd` .</span><span class="sxs-lookup"><span data-stu-id="bdc4a-113">To run WsUtil, use the following command-line syntax if the WSDL and XSD files for the service are in their own directory: `WsUtil.exe *.wsdl *.xsd`.</span></span> <span data-ttu-id="bdc4a-114">In alternativa, è possibile specificare i file in base al nome completo.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-114">Alternatively, you can specify the files by full name.</span></span>

<span data-ttu-id="bdc4a-115">WsUtil genera in genere due file per ogni file di metadati: un'intestazione e un file C.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-115">WsUtil generally generates two files for each metadata file: a header and a C file.</span></span> <span data-ttu-id="bdc4a-116">Aggiungere questi file al progetto di codifica e usare \# le istruzioni include per includerli nel codice del client.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-116">Add these files to your coding project, and use \#include statements to include them in the code for your client.</span></span> <span data-ttu-id="bdc4a-117">I file XSD rappresentano i tipi e i file WSDL rappresentano le operazioni.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-117">(The XSD files represent types, and the WSDL files represent operations.)</span></span>

## <a name="creating-the-service-proxy"></a><span data-ttu-id="bdc4a-118">Creazione del proxy del servizio</span><span class="sxs-lookup"><span data-stu-id="bdc4a-118">Creating the Service Proxy</span></span>

<span data-ttu-id="bdc4a-119">L'intestazione generata da WsUtil contiene una routine di supporto per la creazione del proxy del servizio con l'associazione necessaria.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-119">The header generated by WsUtil contains a helper routine for creating the service proxy with the required binding.</span></span> <span data-ttu-id="bdc4a-120">Questa routine è inclusa nella sezione "routine helper del criterio" del file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-120">This routine is included in the "Policy helper routines" section of the generated header file.</span></span> <span data-ttu-id="bdc4a-121">Ad esempio, l'intestazione generata per il servizio di calcolatrice illustrato nell'esempio [httpcalculatorclientexample](httpcalculatorclientexample.md) conterrà il prototipo di funzione seguente.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-121">For example, the generated header for the calculator service illustrated in the [httpcalculatorclientexample](httpcalculatorclientexample.md) example will contain the following function prototype.</span></span>


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



<span data-ttu-id="bdc4a-122">Incorporare questo helper nel codice e passare un handle [del \_ \_ proxy del servizio WS](ws-service-proxy.md) per ricevere l'handle per il proxy del servizio creato.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-122">Incorporate this helper in your code and pass a [WS\_SERVICE\_PROXY](ws-service-proxy.md) handle to receive the handle to the created service proxy.</span></span> <span data-ttu-id="bdc4a-123">Nello scenario più semplice, in cui solo un handle del proxy del servizio e un oggetto Error vengono passati alla funzione, la chiamata ha un aspetto simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-123">In the simplest scenario, in which only a service proxy handle and an error object are passed to the function, the call looks like the following.</span></span>


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



<span data-ttu-id="bdc4a-124">Per creare la parte dell'indirizzo del proxy del servizio, chiamare [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) con un handle per il proxy del servizio e un puntatore a un [**\_ \_ Indirizzo WS endpoint**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) che contiene l'indirizzo dell'endpoint del servizio a cui si desidera connettersi.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-124">To create the address portion of the service proxy, call [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) with a handle to the service proxy and a pointer to a [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) containing the service endpoint address to which you wish to connect.</span></span>

## <a name="implementing-the-client-with-function-prototypes"></a><span data-ttu-id="bdc4a-125">Implementazione del client con i prototipi di funzione</span><span class="sxs-lookup"><span data-stu-id="bdc4a-125">Implementing the Client with Function Prototypes</span></span>

<span data-ttu-id="bdc4a-126">Le intestazioni generate dai file WSDL del servizio contengono anche i prototipi di funzione C che rappresentano i servizi disponibili dal servizio Web e specifici dell'associazione necessaria.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-126">The headers generated from the service WSDL files also contain C function prototypes representing the services available from the Web service and specific to the binding required.</span></span> <span data-ttu-id="bdc4a-127">Ad esempio, un'intestazione generata per il servizio di calcolatrice illustrato in HttpCalculatorServiceExample conterrà il prototipo seguente per l'operazione di moltiplicazione di tale servizio.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-127">For example, a header generated for the calculator service illustrated in HttpCalculatorServiceExample will contain the following prototype for that service's multiplication operation.</span></span>

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

<span data-ttu-id="bdc4a-128">È possibile copiare i prototipi e usarli come modelli per codificare le chiamate di funzione nel client, in ogni caso passando l'handle al proxy del servizio.</span><span class="sxs-lookup"><span data-stu-id="bdc4a-128">You can copy the prototypes and use them as templates for coding the function calls in your client, in each case passing the handle to service proxy.</span></span> <span data-ttu-id="bdc4a-129">Al termine del proxy del servizio, chiamare [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="bdc4a-129">When you are finished with the service proxy, call [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span></span>

 

 




