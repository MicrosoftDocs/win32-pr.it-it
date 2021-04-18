---
description: Se il servizio Web XML a cui si vuole accedere è stato creato esponendo un'applicazione COM+, provare ad accedervi in modalità oggetto attivato dal client (CAO), che evita la generazione in fase di esecuzione di un proxy e migliora le prestazioni usando connessioni permanenti.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Accesso ai servizi Web XML in modalità CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304741"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a><span data-ttu-id="39eb8-103">Accesso ai servizi Web XML in modalità CAO</span><span class="sxs-lookup"><span data-stu-id="39eb8-103">Accessing XML Web Services in CAO Mode</span></span>

<span data-ttu-id="39eb8-104">Se il servizio Web XML a cui si vuole accedere è stato creato esponendo un'applicazione COM+, provare ad accedervi in modalità oggetto attivato dal client (CAO), che evita la generazione in fase di esecuzione di un proxy e migliora le prestazioni usando connessioni permanenti.</span><span class="sxs-lookup"><span data-stu-id="39eb8-104">If the XML web service you want to access was created by exposing a COM+ application, consider accessing it in client-activated object (CAO) mode, which avoids the run-time generation of a proxy and increases performance by using persistent connections.</span></span> <span data-ttu-id="39eb8-105">Per accedere a un servizio Web XML in modalità CAO, [esportare](exporting-a-soap-enabled-application.md) prima di tutto l'applicazione abilitata per SOAP corrispondente dal server in modalità proxy e quindi [importare](importing-a-soap-enabled-application.md) l'applicazione nel client da cui si desidera accedere all'applicazione come servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="39eb8-105">To access an XML web service in CAO mode, first [export](exporting-a-soap-enabled-application.md) the corresponding SOAP-enabled application from your server in proxy mode and then [import](importing-a-soap-enabled-application.md) the application into the client from which you want to access the application as an XML web service.</span></span> <span data-ttu-id="39eb8-106">È quindi possibile creare un'istanza dei componenti dell'applicazione nel client esattamente come i componenti delle applicazioni locali, ad esempio usando **GetObject** e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="39eb8-106">The application's components can then be instantiated on the client just like the components of local applications—for example, using **GetObject** and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="user-interface"></a><span data-ttu-id="39eb8-107">Interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="39eb8-107">User Interface</span></span>

<span data-ttu-id="39eb8-108">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="39eb8-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="39eb8-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="39eb8-109">Visual Basic</span></span>

<span data-ttu-id="39eb8-110">Nell'Visual Basic frammento di codice seguente viene illustrato l'utilizzo di un componente di un'applicazione COM+ che è stato esposto come un servizio Web XML in modalità CAO.</span><span class="sxs-lookup"><span data-stu-id="39eb8-110">The following Visual Basic code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a><span data-ttu-id="39eb8-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="39eb8-111">C/C++</span></span>

<span data-ttu-id="39eb8-112">Nel frammento di codice seguente viene illustrato l'utilizzo di un componente di un'applicazione COM+ che è stato esposto come un servizio Web XML in modalità CAO.</span><span class="sxs-lookup"><span data-stu-id="39eb8-112">The following code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a><span data-ttu-id="39eb8-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="39eb8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39eb8-114">Accesso ai servizi Web XML in modalità WKO</span><span class="sxs-lookup"><span data-stu-id="39eb8-114">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="39eb8-115">Panoramica del servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="39eb8-115">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="39eb8-116">Creazione di servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="39eb8-116">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="39eb8-117">Protezione dei servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="39eb8-117">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 
