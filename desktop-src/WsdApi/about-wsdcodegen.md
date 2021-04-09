---
description: Descrive i file di input utilizzati da WsdCodeGen e i file di output generati da WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Informazioni su WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049810"
---
# <a name="about-wsdcodegen"></a><span data-ttu-id="908b0-103">Informazioni su WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="908b0-103">About WsdCodeGen</span></span>

<span data-ttu-id="908b0-104">WsdCodeGen utilizza un file di configurazione XML per determinare il percorso dei metadati del servizio.</span><span class="sxs-lookup"><span data-stu-id="908b0-104">WsdCodeGen uses an XML configuration file to determine the location of the service metadata.</span></span> <span data-ttu-id="908b0-105">Il file di configurazione viene usato anche per definire i nomi di interfaccia, i GUID di interfaccia, i nomi delle classi, i nomi dei metodi e altri identificatori.</span><span class="sxs-lookup"><span data-stu-id="908b0-105">The configuration file is also used to define interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> <span data-ttu-id="908b0-106">Per ulteriori informazioni su questo file, vedere [WsdCodeGen Configuration file](wsdcodegen-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="908b0-106">For more information about this file, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).</span></span>

<span data-ttu-id="908b0-107">WsdCodeGen richiede due tipi di file di input: un file di configurazione XML e uno o più file di descrizione del servizio (file WSDL e/o XSD).</span><span class="sxs-lookup"><span data-stu-id="908b0-107">WsdCodeGen requires two types of input files: an XML configuration file and one or more service description files (WSDL and/or XSD files).</span></span> <span data-ttu-id="908b0-108">WsdCodeGen elabora questi file di input e genera due tipi di file di output: file di interfaccia e file di intestazione e di origine.</span><span class="sxs-lookup"><span data-stu-id="908b0-108">WsdCodeGen processes these input files and generates two type of output files: interface files and header/source files.</span></span>

## <a name="input-files"></a><span data-ttu-id="908b0-109">File di input</span><span class="sxs-lookup"><span data-stu-id="908b0-109">Input Files</span></span>



| <span data-ttu-id="908b0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="908b0-110">Type</span></span>                      | <span data-ttu-id="908b0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="908b0-111">Description</span></span>                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="908b0-112">File di configurazione</span><span class="sxs-lookup"><span data-stu-id="908b0-112">Configuration file</span></span>        | <span data-ttu-id="908b0-113">Un file XML che indica il percorso dei metadati del servizio e definisce i nomi delle interfacce, i GUID dell'interfaccia, i nomi delle classi, i nomi dei metodi e altri identificatori.</span><span class="sxs-lookup"><span data-stu-id="908b0-113">An XML file that indicates the location of the service metadata and defines interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> |
| <span data-ttu-id="908b0-114">File di descrizione del servizio</span><span class="sxs-lookup"><span data-stu-id="908b0-114">Service description files</span></span> | <span data-ttu-id="908b0-115">Uno o più file WSDL o XSD che descrivono i servizi da implementare nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="908b0-115">One or more WSDL or XSD files that describes the services to implement on the device.</span></span>                                                                           |



 

## <a name="output-files"></a><span data-ttu-id="908b0-116">File di output</span><span class="sxs-lookup"><span data-stu-id="908b0-116">Output Files</span></span>



| <span data-ttu-id="908b0-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="908b0-117">Type</span></span>                        | <span data-ttu-id="908b0-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="908b0-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="908b0-119">File di interfaccia</span><span class="sxs-lookup"><span data-stu-id="908b0-119">Interface files</span></span>             | <span data-ttu-id="908b0-120">File IDL (Interface Definition Language) che può essere usato con il compilatore MIDL per produrre un file di intestazione di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="908b0-120">An IDL (Interface Definition Language) file that can be used with the MIDL compiler to produce an interface header file.</span></span> <span data-ttu-id="908b0-121">I client WSDAPI e i servizi WSDAPI possono usare questo file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="908b0-121">WSDAPI clients and WSDAPI services can use this interface file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="908b0-122">Intestazione C++ e file di origine</span><span class="sxs-lookup"><span data-stu-id="908b0-122">C++ header and source files</span></span> | <span data-ttu-id="908b0-123">File C++ che descrivono le informazioni sul contratto di messaggio, lo spazio dei nomi e il tipo.</span><span class="sxs-lookup"><span data-stu-id="908b0-123">C++ files that describe the message contract, namespace, and type information.</span></span> <span data-ttu-id="908b0-124">Possono contenere codice proxy e/o codice stub.</span><span class="sxs-lookup"><span data-stu-id="908b0-124">They may contain proxy code and/or stub code.</span></span> <span data-ttu-id="908b0-125">Il codice proxy implementa un'interfaccia del servizio e converte le chiamate al metodo del servizio in operazioni WSDAPI che effettuano richieste di servizio.</span><span class="sxs-lookup"><span data-stu-id="908b0-125">Proxy code implements a service's interface and translates service method calls into WSDAPI operations that make service requests.</span></span> <span data-ttu-id="908b0-126">Il codice stub converte le richieste di servizio WSDAPI in codice che chiama i metodi del servizio.</span><span class="sxs-lookup"><span data-stu-id="908b0-126">Stub code translates WSDAPI service requests into code that calls service methods.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="908b0-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="908b0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="908b0-128">Generatore di codice dei servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="908b0-128">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="908b0-129">Uso di WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="908b0-129">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 



