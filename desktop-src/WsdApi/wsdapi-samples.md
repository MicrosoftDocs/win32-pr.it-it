---
description: Sono disponibili due esempi WSDAPI con la Windows SDK per Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Esempi di WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754959"
---
# <a name="wsdapi-samples"></a><span data-ttu-id="b9783-103">Esempi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="b9783-103">WSDAPI Samples</span></span>

<span data-ttu-id="b9783-104">Sono disponibili due esempi WSDAPI con la Windows SDK per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b9783-104">There are two WSDAPI samples included with the Windows SDK for Windows Server 2008.</span></span> <span data-ttu-id="b9783-105">Il codice sorgente per gli esempi è disponibile in <Windows SDK Install Folder> \\ esempi \\ Web \\ wsdapi.</span><span class="sxs-lookup"><span data-stu-id="b9783-105">The source code for the samples can be found in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI.</span></span> <span data-ttu-id="b9783-106">Questa versione dell'SDK è disponibile nell' [area download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="b9783-106">This version of the SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span> <span data-ttu-id="b9783-107">Gli esempi non sono disponibili in Windows Vista SDK.</span><span class="sxs-lookup"><span data-stu-id="b9783-107">The samples are not available in the Windows Vista SDK.</span></span>

<span data-ttu-id="b9783-108">L'esempio quotation Stock (disponibile in <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ stockquote) illustra un servizio con la funzionalità di messaggistica di base.</span><span class="sxs-lookup"><span data-stu-id="b9783-108">The stock quote sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\StockQuote) demonstrates a service with basic messaging functionality.</span></span> <span data-ttu-id="b9783-109">L'esempio di servizio file (disponibile in <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ FileService) illustra un servizio con funzionalità avanzate, ad esempio la messaggistica asincrona, gli allegati e gli eventi.</span><span class="sxs-lookup"><span data-stu-id="b9783-109">The file service sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\FileService) demonstrates a service with advanced functionality, such as asynchronous messaging, attachments, and eventing.</span></span>

<span data-ttu-id="b9783-110">Entrambi gli esempi includono i seguenti tipi di file.</span><span class="sxs-lookup"><span data-stu-id="b9783-110">Both samples include the following types of files.</span></span>

-   <span data-ttu-id="b9783-111">File WSDL contenenti le descrizioni del servizio.</span><span class="sxs-lookup"><span data-stu-id="b9783-111">WSDL files that contain the service descriptions.</span></span>
-   <span data-ttu-id="b9783-112">[File di configurazione WsdCodeGen](wsdcodegen-configuration-file.md) usati per generare il codice wsdapi.</span><span class="sxs-lookup"><span data-stu-id="b9783-112">[WsdCodeGen configuration files](wsdcodegen-configuration-file.md) used to generate WSDAPI code.</span></span>
-   <span data-ttu-id="b9783-113">File di origine e intestazione C++ generati.</span><span class="sxs-lookup"><span data-stu-id="b9783-113">Generated C++ header and source files.</span></span>
-   <span data-ttu-id="b9783-114">File di implementazione del servizio e del client.</span><span class="sxs-lookup"><span data-stu-id="b9783-114">Client and service implementation files.</span></span>
-   <span data-ttu-id="b9783-115">File di progetto e di soluzione di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b9783-115">Visual Studio project and solution files.</span></span>

<span data-ttu-id="b9783-116">Entrambi gli esempi implementano gli host di dispositivi ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), i proxy di dispositivo ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) e i proxy del servizio ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span><span class="sxs-lookup"><span data-stu-id="b9783-116">Both samples implement device hosts ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), device proxies ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)), and service proxies ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span></span> <span data-ttu-id="b9783-117">Nell'esempio relativo al servizio file viene inoltre illustrato l'utilizzo della messaggistica asincrona ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), degli allegati ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) e degli eventi.</span><span class="sxs-lookup"><span data-stu-id="b9783-117">In addition, the file service sample demonstrates the use of asynchronous messaging ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), attachments ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) and eventing.</span></span>

<span data-ttu-id="b9783-118">I file FileServiceContract. vcproj e StockQuoteContract. vcproj inclusi negli esempi chiamano [WsdCodeGen](web-services-for-devices-code-generator.md) per generare file di origine e intestazione C++ dal file WSDL specificato nel file di configurazione WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="b9783-118">The FileServiceContract.vcproj and StockQuoteContract.vcproj files included with the samples call [WsdCodeGen](web-services-for-devices-code-generator.md) to generate C++ header and source files from the WSDL file specified in the WsdCodeGen configuration file.</span></span> <span data-ttu-id="b9783-119">Ciò significa che se il file di configurazione WSDL o WsdCodeGen di esempio viene modificato e il progetto di esempio viene ricompilato, WsdCodeGen genera automaticamente nuovi file di intestazione e di origine che riflettono le modifiche.</span><span class="sxs-lookup"><span data-stu-id="b9783-119">This means that if the sample WSDL or WsdCodeGen configuration file is changed and the sample project is rebuilt, WsdCodeGen automatically generates new header and source files that reflect the changes.</span></span> <span data-ttu-id="b9783-120">Questo è il metodo preferito per la compilazione di applicazioni WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="b9783-120">This is the preferred method for building WSDAPI applications.</span></span> <span data-ttu-id="b9783-121">WsdCodeGen viene in genere chiamato dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b9783-121">WsdCodeGen is usually called from the command line.</span></span> <span data-ttu-id="b9783-122">Aprire il \* file. vcproj pertinente per visualizzare le chiamate alla riga di comando di WsdCodeGen di esempio.</span><span class="sxs-lookup"><span data-stu-id="b9783-122">Open the relevant \*.vcproj file to view the example WsdCodeGen command line calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9783-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9783-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9783-124">Sviluppo di applicazioni WSD in Windows</span><span class="sxs-lookup"><span data-stu-id="b9783-124">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



