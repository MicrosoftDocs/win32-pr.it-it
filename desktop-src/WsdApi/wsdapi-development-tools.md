---
description: Gli strumenti di sviluppo WSDAPI inclusi nel Windows SDK (WSD CodeGen, WSD debug host e WSD debug client) consentono agli sviluppatori di creare ed eseguire il debug di client e dispositivi basati su WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Strumenti di sviluppo WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309740"
---
# <a name="wsdapi-development-tools"></a><span data-ttu-id="1e33f-103">Strumenti di sviluppo WSDAPI</span><span class="sxs-lookup"><span data-stu-id="1e33f-103">WSDAPI Development Tools</span></span>

<span data-ttu-id="1e33f-104">Gli strumenti di sviluppo WSDAPI inclusi nel Windows SDK (WSD CodeGen, WSD debug host e WSD debug client) consentono agli sviluppatori di creare ed eseguire il debug di client e dispositivi basati su WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="1e33f-104">The WSDAPI development tools included in the Windows SDK (WSD CodeGen, WSD Debug Host, and WSD Debug Client) enable developers to create and debug WSDAPI-based clients and devices.</span></span> <span data-ttu-id="1e33f-105">Il codice sorgente per questi strumenti non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1e33f-105">The source code for these tools is not available.</span></span> <span data-ttu-id="1e33f-106">Gli strumenti SDK si trovano nella seguente directory: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="1e33f-106">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="1e33f-107">WSD CodeGen (wsdcodegen.exe) converte un contratto WSDL in codice C++ generato, che gli sviluppatori possono chiamare direttamente in.</span><span class="sxs-lookup"><span data-stu-id="1e33f-107">WSD CodeGen (wsdcodegen.exe) converts a WSDL contract into generated C++ code, which developers can call directly into.</span></span> <span data-ttu-id="1e33f-108">Gestisce la serializzazione dei dati e la rappresentazione Wire, in modo che gli sviluppatori possano concentrarsi sulla progettazione di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1e33f-108">It handles the data serialization and wire representation so developers can focus on designing applications.</span></span> <span data-ttu-id="1e33f-109">Per altre informazioni su WSD CodeGen, vedere [servizi Web nel generatore di codice](web-services-for-devices-code-generator.md)per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="1e33f-109">For more information about WSD CodeGen, see [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="1e33f-110">Questo strumento è disponibile nel Software Development Kit (SDK) di Microsoft Windows e in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="1e33f-110">This tool is available in the Microsoft Windows Software Development Kit (SDK) and in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="1e33f-111">Gli strumenti WSD debug host (wsddebug \_host.exe) e WSD debug client (wsddebug \_client.exe) consentono agli sviluppatori di eseguire il debug di client e host.</span><span class="sxs-lookup"><span data-stu-id="1e33f-111">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools help developers debug their clients and hosts.</span></span> <span data-ttu-id="1e33f-112">Questi strumenti possono essere usati per verificare e controllare WS-Discovery e il traffico di scambio dei metadati.</span><span class="sxs-lookup"><span data-stu-id="1e33f-112">These tools can be used to verify and inspect WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="1e33f-113">Per ulteriori informazioni sull'host di debug WSD e sul client di debug WSD, vedere [strumenti di debug](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1e33f-113">For more information about WSD Debug Host and WSD Debug Client, see [Debugging Tools](debugging-tools.md).</span></span> <span data-ttu-id="1e33f-114">Questi strumenti sono disponibili solo nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1e33f-114">These tools are available only in the Windows SDK.</span></span>

<span data-ttu-id="1e33f-115">È disponibile uno strumento di sviluppo aggiuntivo, denominato [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), disponibile solo in WDK.</span><span class="sxs-lookup"><span data-stu-id="1e33f-115">There is an additional development tool, named [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), that is available only in the WDK.</span></span> <span data-ttu-id="1e33f-116">Questo strumento viene utilizzato per il test di metodi di servizio, MTOM (Message Transmission Optimization Mechanism), allegati o WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="1e33f-116">This tool is used for testing service methods, Message Transmission Optimization Mechanism (MTOM), attachments or WS-Eventing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e33f-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e33f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e33f-118">Sviluppo di applicazioni WSD in Windows</span><span class="sxs-lookup"><span data-stu-id="1e33f-118">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="1e33f-119">Generatore di codice dei servizi Web nei dispositivi</span><span class="sxs-lookup"><span data-stu-id="1e33f-119">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="1e33f-120">Strumento di interoperabilità di base di WSDAPI (WSDBIT)</span><span class="sxs-lookup"><span data-stu-id="1e33f-120">WSDAPI Basic Interoperability Tool (WSDBIT)</span></span>](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[<span data-ttu-id="1e33f-121">Strumenti di debug</span><span class="sxs-lookup"><span data-stu-id="1e33f-121">Debugging Tools</span></span>](debugging-tools.md)
</dt> </dl>

 

 



