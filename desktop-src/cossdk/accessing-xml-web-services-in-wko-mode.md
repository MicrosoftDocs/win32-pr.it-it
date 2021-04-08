---
description: È possibile accedere e utilizzare qualsiasi servizio Web XML, anche se il servizio Web XML non è stato creato utilizzando COM+ o anche Microsoft Windows, purché il servizio Web XML pubblichi una descrizione WSDL della relativa sintassi.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Accesso ai servizi Web XML in modalità WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748194"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a><span data-ttu-id="d78c1-103">Accesso ai servizi Web XML in modalità WKO</span><span class="sxs-lookup"><span data-stu-id="d78c1-103">Accessing XML Web Services in WKO Mode</span></span>

<span data-ttu-id="d78c1-104">È possibile accedere e utilizzare qualsiasi servizio Web XML, anche se il servizio Web XML non è stato creato utilizzando COM+ o anche Microsoft Windows, purché il servizio Web XML pubblichi una descrizione WSDL della relativa sintassi.</span><span class="sxs-lookup"><span data-stu-id="d78c1-104">You can access and use any XML web service, even if that XML web service was not created using COM+ or even Microsoft Windows, as long as the XML Web Service publishes a WSDL description of its syntax.</span></span> <span data-ttu-id="d78c1-105">È sufficiente creare un'istanza del componente usando il moniker SOAP: WSDL = URL, dove URL è l'URL della descrizione WSDL del servizio Web XML a cui si vuole accedere.</span><span class="sxs-lookup"><span data-stu-id="d78c1-105">Just create an instance of the component by using the soap:wsdl=URL moniker, where URL is the URL of the WSDL description of the XML web service you want to access.</span></span> <span data-ttu-id="d78c1-106">Si tratta della modalità WKO (well-known Object) per l'accesso ai servizi Web XML.</span><span class="sxs-lookup"><span data-stu-id="d78c1-106">This is the well-known object (WKO) mode of accessing XML web services.</span></span>

<span data-ttu-id="d78c1-107">È possibile chiamare i metodi dell'oggetto senza alcuna considerazione speciale.</span><span class="sxs-lookup"><span data-stu-id="d78c1-107">The object's methods can be called without any special considerations.</span></span> <span data-ttu-id="d78c1-108">È possibile accedere al servizio Web XML tramite una query SOAP e la risposta viene interpretata in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="d78c1-108">The XML web service is accessed via a SOAP query, and the response is interpreted transparently.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="d78c1-109">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="d78c1-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="d78c1-110">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="d78c1-110">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="d78c1-111">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d78c1-111">Visual Basic</span></span>

<span data-ttu-id="d78c1-112">Il seguente frammento di codice di Microsoft Visual Basic illustra l'uso di un servizio Web XML in modalità WKO.</span><span class="sxs-lookup"><span data-stu-id="d78c1-112">The following Microsoft Visual Basic code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



<span data-ttu-id="d78c1-113">In questo frammento di codice, che illustra l'utilizzo di un componente di un'applicazione COM+ esposta come un servizio Web XML, nomeserver è il nome di dominio completo del server che offre il servizio Web XML. vroot è la directory radice virtuale IIS dalla quale viene esposto il servizio Web XML. e progID è il ProgID del componente che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="d78c1-113">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="cc"></a><span data-ttu-id="d78c1-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="d78c1-114">C/C++</span></span>

<span data-ttu-id="d78c1-115">Nel frammento di codice seguente viene illustrato l'utilizzo di un servizio Web XML in modalità WKO.</span><span class="sxs-lookup"><span data-stu-id="d78c1-115">The following code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



<span data-ttu-id="d78c1-116">In questo frammento di codice, che illustra l'utilizzo di un componente di un'applicazione COM+ esposta come un servizio Web XML, nomeserver è il nome di dominio completo del server che offre il servizio Web XML. vroot è la directory radice virtuale IIS dalla quale viene esposto il servizio Web XML. e progID è il ProgID del componente che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="d78c1-116">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="d78c1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d78c1-117">Remarks</span></span>

<span data-ttu-id="d78c1-118">Quando si accede per la prima volta a un servizio Web XML in modalità WKO, COM+ genera un client proxy e lo compila in background.</span><span class="sxs-lookup"><span data-stu-id="d78c1-118">When an XML web service is first accessed in WKO mode, COM+ generates a proxy client and compiles it in the background.</span></span> <span data-ttu-id="d78c1-119">Questa generazione in fase di esecuzione e la mancanza di connessioni permanenti in modalità WKO generano prestazioni significativamente ridotte rispetto alla modalità CAO.</span><span class="sxs-lookup"><span data-stu-id="d78c1-119">This run-time generation and the lack of persistent connections in WKO mode results in significantly reduced performance in comparison to CAO mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d78c1-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d78c1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d78c1-121">Accesso ai servizi Web XML in modalità CAO</span><span class="sxs-lookup"><span data-stu-id="d78c1-121">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="d78c1-122">Panoramica del servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="d78c1-122">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="d78c1-123">Creazione di servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="d78c1-123">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="d78c1-124">Protezione dei servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="d78c1-124">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



