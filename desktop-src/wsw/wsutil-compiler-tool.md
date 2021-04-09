---
title: Strumento compilatore WsUtil
description: Lo strumento compilatore di servizi Web Windows, WsUtil.exe, supporta il modello di servizio e la serializzazione dei tipi di dati. Elabora documenti WSDL, XML Schema e criteri e genera intestazioni e file di origine C.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Servizi Web dello strumento del compilatore WsUtil per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963577"
---
# <a name="wsutil-compiler-tool"></a><span data-ttu-id="358d4-107">Strumento compilatore WsUtil</span><span class="sxs-lookup"><span data-stu-id="358d4-107">WsUtil Compiler tool</span></span>

<span data-ttu-id="358d4-108">Lo strumento compilatore di servizi Web Windows, WsUtil.exe, supporta il [modello di servizio](service-model-layer-overview.md) e la [serializzazione](serialization.md) dei tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="358d4-108">The Windows Web Services compiler tool, WsUtil.exe, supports the [service model](service-model-layer-overview.md) and [serialization](serialization.md) of data types.</span></span> <span data-ttu-id="358d4-109">Elabora documenti WSDL, XML Schema e criteri e genera intestazioni e file di origine C.</span><span class="sxs-lookup"><span data-stu-id="358d4-109">It processes WSDL, XML schema and policy documents, and generates C headers and source files.</span></span> <span data-ttu-id="358d4-110">Questo strumento è simile allo strumento compilatore WSDL per il codice gestito, ma è invece destinato al codice nativo.</span><span class="sxs-lookup"><span data-stu-id="358d4-110">This tool is similar to WSDL compiler tool for managed code but is aimed at native code instead.</span></span>

<span data-ttu-id="358d4-111">Per supportare il [modello di servizio](service-model-layer-overview.md), WsUtil.exe genera intestazioni da usare sia per il client che per il servizio.</span><span class="sxs-lookup"><span data-stu-id="358d4-111">To support the [service model](service-model-layer-overview.md), WsUtil.exe generates headers to be used for both client and service.</span></span> <span data-ttu-id="358d4-112">Genera il file proxy C per il lato client e i file stub C per il lato del servizio, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="358d4-112">It generates C proxy file for the client side, and C stub files for the service side, as needed.</span></span>

<span data-ttu-id="358d4-113">Per supportare la [serializzazione](serialization.md), il compilatore genera intestazioni per le descrizioni di elementi per le definizioni di elementi globali e tutte le informazioni relative alla definizione dei tipi nei file proxy utilizzati dal motore di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="358d4-113">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all the type definition information in the proxy files that is consumed by the serialization engine.</span></span>


<span data-ttu-id="358d4-114">Per le opzioni della riga di comando per l'elaborazione di file WSDL, file di XML Schema e file di criteri del servizio Web, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="358d4-114">For command line options for processing WSDL files, XML Schema files, and web service policy files, see the following topics:</span></span>

-   [<span data-ttu-id="358d4-115">Strumento compilatore servizio Web</span><span class="sxs-lookup"><span data-stu-id="358d4-115">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
-   [<span data-ttu-id="358d4-116">WSDL e contratti di servizio</span><span class="sxs-lookup"><span data-stu-id="358d4-116">WSDL and Service Contracts</span></span>](wsdl-support.md)
-   [<span data-ttu-id="358d4-117">Supporto degli schemi</span><span class="sxs-lookup"><span data-stu-id="358d4-117">Schema support</span></span>](schema-support.md)
-   [<span data-ttu-id="358d4-118">Supporto dei criteri</span><span class="sxs-lookup"><span data-stu-id="358d4-118">Policy support</span></span>](policy-support.md)

## <a name="security"></a><span data-ttu-id="358d4-119">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="358d4-119">Security</span></span>

<span data-ttu-id="358d4-120">Quando si usa WsUtil, tenere presente i problemi seguenti e osservare le precauzioni appropriate:</span><span class="sxs-lookup"><span data-stu-id="358d4-120">When you use WsUtil, be aware of the following issues and observe the appropriate precautions:</span></span>

-   <span data-ttu-id="358d4-121">Wsutil non recupera i metadati XML sulla rete e WSUTIL non risolve le istruzioni Import e/o include nei file di metadati di input.</span><span class="sxs-lookup"><span data-stu-id="358d4-121">Wsutil does not retrieve XML metadata over the network, and wsutil does not resolve import and/or include statements in the input metadata files.</span></span> <span data-ttu-id="358d4-122">Wsutil apre e legge i file di criteri WSDL, XSD e.</span><span class="sxs-lookup"><span data-stu-id="358d4-122">Wsutil opens and reads wsdl, xsd, and policy files.</span></span> <span data-ttu-id="358d4-123">I metadati XML non sono resistenti alle manomissioni.</span><span class="sxs-lookup"><span data-stu-id="358d4-123">XML metadata is not tamper resistant.</span></span> <span data-ttu-id="358d4-124">Assicurarsi di usare solo i file WSDL, XSD e Policy acquisiti da un'origine attendibile e assicurarsi di proteggere i file dalla manomissione prima e dopo l'uso.</span><span class="sxs-lookup"><span data-stu-id="358d4-124">Ensure that you only use wsdl, xsd and policy files are acquired from trusted source and make sure to protect the files from tampering before and after using them.</span></span> <span data-ttu-id="358d4-125">Esaminare attentamente il contenuto dei file di input e verificare che il contenuto dei file sia sicuro per l'utilizzo nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="358d4-125">Carefully review the contents of the input files and validate that the contents of files are safe for use in the application.</span></span> <span data-ttu-id="358d4-126">Wsutil.exe non esegue alcuna verifica dell'autenticità dei file di metadati.</span><span class="sxs-lookup"><span data-stu-id="358d4-126">Wsutil.exe does not do any verification of authenticity of the metadata files.</span></span>
-   <span data-ttu-id="358d4-127">Wsutil genera file di intestazione e Stub, che non sono resistenti alle manomissioni.</span><span class="sxs-lookup"><span data-stu-id="358d4-127">Wsutil generates header and stub files, which are not tamper resistant.</span></span> <span data-ttu-id="358d4-128">È necessario impostare i diritti di accesso a livello corretti per i file di origine generati da wsutil.exe per impedire l'accesso unauthoritized a tali file.</span><span class="sxs-lookup"><span data-stu-id="358d4-128">You need to set the correct level access rights on source files generated by wsutil.exe to prevent unauthoritized access to those files.</span></span> <span data-ttu-id="358d4-129">Wsutil usa System. IO. StreamWriter per creare i file di output.</span><span class="sxs-lookup"><span data-stu-id="358d4-129">Wsutil uses System.IO.StreamWriter to create the output files.</span></span>
-   <span data-ttu-id="358d4-130">Gli utenti devono tenere presente che WSUTIL può sovrascrivere i file locali e devono prestare attenzione a specificare nomi e directory sicuri per i file di output usando l'opzione/out.</span><span class="sxs-lookup"><span data-stu-id="358d4-130">Users need to be aware that Wsutil can overwrite their local files, and they should be careful to specify safe file names and directories for output files using the /out switch.</span></span>
-   <span data-ttu-id="358d4-131">Wsutil o wsutilhelper.dll caricati in wsutil.exe, possono terminare in modo imprevisto o utilizzare una grande quantità di risorse di sistema quando sono sotto attacco o durante l'elaborazione di una quantità molto elevata di metadati di input.</span><span class="sxs-lookup"><span data-stu-id="358d4-131">Wsutil or wsutilhelper.dll loaded in wsutil.exe, may terminate unexpectedly or consume large amount of system resources when under attack or in processing a very large amount of input metadata.</span></span> <span data-ttu-id="358d4-132">Lo strumento è progettato per essere utilizzato in fase di sviluppo. solo questo strumento deve essere utilizzato solo come strumento per la fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="358d4-132">The tool is designed to be used during development time only This tool should be used as a development time tool only.</span></span> <span data-ttu-id="358d4-133">Potrebbe non essere possibile utilizzare il livello intermedio per elaborare le informazioni sui criteri.</span><span class="sxs-lookup"><span data-stu-id="358d4-133">It may not be safe for use in the middle tier to process policy information.</span></span>
-   <span data-ttu-id="358d4-134">Wsutilhelper.dll DLL Helper viene caricata in wsutil.exe gestite per elaborare le informazioni sui criteri.</span><span class="sxs-lookup"><span data-stu-id="358d4-134">Wsutilhelper.dll helper DLL is loaded into managed wsutil.exe to process policy information.</span></span> <span data-ttu-id="358d4-135">Assicurarsi che non esistano file binari dannosi con lo stesso nome di file nel percorso binario.</span><span class="sxs-lookup"><span data-stu-id="358d4-135">User should make sure no malicious binary with same filename exists in the binary path.</span></span> <span data-ttu-id="358d4-136">Analogamente, l'utente deve assicurarsi che nell'ambiente di compilazione il percorso binario sia configurato correttamente, in modo che non esistano file binari dannosi con lo stesso nome "wsutil.exe".</span><span class="sxs-lookup"><span data-stu-id="358d4-136">Similarly, user should make sure in the build environment, the binary path is setup correctly that there is no malicious binary with same "wsutil.exe" name exists.</span></span>
-   <span data-ttu-id="358d4-137">Wsutil genera l'annotazione SAL per le operazioni e i campi della struttura, quando possibile.</span><span class="sxs-lookup"><span data-stu-id="358d4-137">Wsutil generates SAL annotation for operations and structure fields when possible.</span></span> <span data-ttu-id="358d4-138">L'utente dei file generati da WSUTIL deve seguire il requisito specificato tramite l'annotazione SAL.</span><span class="sxs-lookup"><span data-stu-id="358d4-138">User of wsutil generated files should follow the requirement specified through SAL annotation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="358d4-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="358d4-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="358d4-140">Panoramica del livello del modello di servizio</span><span class="sxs-lookup"><span data-stu-id="358d4-140">Service Model Layer Overview</span></span>](service-model-layer-overview.md)
</dt> <dt>

[<span data-ttu-id="358d4-141">Serializzazione</span><span class="sxs-lookup"><span data-stu-id="358d4-141">Serialization</span></span>](serialization.md)
</dt> <dt>

[<span data-ttu-id="358d4-142">Strumento compilatore servizio Web</span><span class="sxs-lookup"><span data-stu-id="358d4-142">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
</dt> <dt>

[<span data-ttu-id="358d4-143">Supporto WSDL</span><span class="sxs-lookup"><span data-stu-id="358d4-143">WSDL support</span></span>](wsdl-support.md)
</dt> <dt>

[<span data-ttu-id="358d4-144">Supporto degli schemi</span><span class="sxs-lookup"><span data-stu-id="358d4-144">Schema support</span></span>](schema-support.md)
</dt> <dt>

[<span data-ttu-id="358d4-145">Supporto dei criteri</span><span class="sxs-lookup"><span data-stu-id="358d4-145">Policy Support</span></span>](policy-support.md)
</dt> </dl>

 

 




