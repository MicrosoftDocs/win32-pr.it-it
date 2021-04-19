---
description: Un esperto è una libreria di collegamento dinamico (DLL) di Microsoft Win32 che analizza il traffico di rete raccolto da un provider di pacchetti di rete (NPP) e inserito in un file di acquisizione.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305944"
---
# <a name="expert"></a><span data-ttu-id="5de7e-103">Expert</span><span class="sxs-lookup"><span data-stu-id="5de7e-103">Expert</span></span>

<span data-ttu-id="5de7e-104">Un esperto è una libreria di collegamento dinamico (DLL) di Microsoft Win32 che analizza il traffico di rete raccolto da un [*provider di pacchetti di rete*](n.md) (NPP) e inserito in un file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="5de7e-104">An expert is a Microsoft Win32 dynamic-link library (DLL) that analyzes network traffic collected by a [*network packet provider*](n.md) (NPP), and placed in a capture file.</span></span> <span data-ttu-id="5de7e-105">Dopo l'acquisizione e l'archiviazione dei dati in un file di acquisizione, l'esperto lavora con un parser, noto anche come parser di protocollo, per analizzare i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="5de7e-105">After the data is captured and stored in a capture file, the expert works with a parser, also referred to as a protocol parser, to analyze the data in the file.</span></span> <span data-ttu-id="5de7e-106">Ad esempio, è possibile esaminare i frame del file di acquisizione e utilizzare un [*parser*](p.md) per riconoscere protocolli quali Server Message Block (SMB) o Transmission Control Protocol/Internet Protocol (TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="5de7e-106">For example, you can examine the frames of the capture file and use a [*parser*](p.md) to recognize protocols such as server message block (SMB), or Transmission Control Protocol/Internet Protocol (TCP/IP).</span></span>

<span data-ttu-id="5de7e-107">È possibile progettare un esperto per lavorare con tutti i parser di Network Monitor e tutti i parser creati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="5de7e-107">You can design an expert to work with all of the Network Monitor parsers, and any parsers that you create yourself.</span></span>

<span data-ttu-id="5de7e-108">Dopo che una corrispondenza richiesta di protocolli identifica un frame specifico, l'esperto estrae i dati dal frame.</span><span class="sxs-lookup"><span data-stu-id="5de7e-108">After a requested match of protocols identifies a specific frame, the expert extracts data from the frame.</span></span> <span data-ttu-id="5de7e-109">È possibile programmare l'esperto per manipolare le informazioni in dati utilizzabili visualizzati dal Network Monitor Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="5de7e-109">You can program the expert to manipulate information into usable data that the Network Monitor Event Viewer displays.</span></span>

<span data-ttu-id="5de7e-110">È possibile configurare un esperto in fase di esecuzione e quindi usare Network Monitor per salvare i dati di configurazione utente da riutilizzare con diversi file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="5de7e-110">You can configure an expert at run time, and then use Network Monitor to save user configuration data for reuse with different capture files.</span></span> <span data-ttu-id="5de7e-111">È possibile utilizzare un esperto per fornire i dati di correlazione e le risoluzioni personalizzate per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="5de7e-111">You can use an expert to provide correlation data and custom resolutions for end users.</span></span> <span data-ttu-id="5de7e-112">Per ulteriori informazioni sulla creazione di informazioni di configurazione basate su HTML, vedere la [pagina di riferimento evento](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="5de7e-112">For more information about the creation of HTML-based configuration information, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="5de7e-113">Durante l'installazione di Network Monitor, nella sottodirectory Experts vengono installate le dll Expert seguenti:</span><span class="sxs-lookup"><span data-stu-id="5de7e-113">During Network Monitor setup, the following expert DLLs are installed in the Experts sub-directory:</span></span>

-   <span data-ttu-id="5de7e-114">Coalesce.dll</span><span class="sxs-lookup"><span data-stu-id="5de7e-114">Coalesce.dll</span></span>
-   <span data-ttu-id="5de7e-115">Propdist.dll</span><span class="sxs-lookup"><span data-stu-id="5de7e-115">Propdist.dll</span></span>
-   <span data-ttu-id="5de7e-116">Protdist.dll</span><span class="sxs-lookup"><span data-stu-id="5de7e-116">Protdist.dll</span></span>
-   <span data-ttu-id="5de7e-117">Resptime.dll</span><span class="sxs-lookup"><span data-stu-id="5de7e-117">Resptime.dll</span></span>
-   <span data-ttu-id="5de7e-118">Tcpipe.dll</span><span class="sxs-lookup"><span data-stu-id="5de7e-118">Tcpipe.dll</span></span>
-   <span data-ttu-id="5de7e-119">Topuser.dll</span><span class="sxs-lookup"><span data-stu-id="5de7e-119">Topuser.dll</span></span>

<span data-ttu-id="5de7e-120">Quando si avvia Network Monitor, la funzione [**DllMain**](dllmain-expert.md) compila tutti gli esperti nella sottodirectory Experts.</span><span class="sxs-lookup"><span data-stu-id="5de7e-120">When you start Network Monitor, the [**DllMain**](dllmain-expert.md) function builds all experts in the experts subdirectory.</span></span> <span data-ttu-id="5de7e-121">Quando l'utente seleziona **esperti** dal menu **strumenti** dell'interfaccia utente di Network Monitor, Network Monitor carica le DLL di esperti.</span><span class="sxs-lookup"><span data-stu-id="5de7e-121">When the user selects **Experts** on the **Tools** menu of the Network Monitor UI, Network Monitor loads the expert DLLs.</span></span> <span data-ttu-id="5de7e-122">L'esperto viene chiamato attraverso il punto di ingresso dell' [esperto di registrazione](register-expert.md) per fornire i dettagli di base sull'esperto.</span><span class="sxs-lookup"><span data-stu-id="5de7e-122">The expert is called through the [Register Expert](register-expert.md) entry point to provide basic details about the expert.</span></span>

![finestra di dialogo esperti di Network Monitor](images/expick.png)

<span data-ttu-id="5de7e-124">Network Monitor chiama le funzioni seguenti per gestire l'esperto:</span><span class="sxs-lookup"><span data-stu-id="5de7e-124">Network Monitor calls the following functions to manage the expert:</span></span>

-   [<span data-ttu-id="5de7e-125">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="5de7e-125">**DllMain**</span></span>](dllmain-expert.md)
-   [<span data-ttu-id="5de7e-126">**Registra esperto**</span><span class="sxs-lookup"><span data-stu-id="5de7e-126">**Register Expert**</span></span>](register-expert.md)
-   [<span data-ttu-id="5de7e-127">**Correre**</span><span class="sxs-lookup"><span data-stu-id="5de7e-127">**Run**</span></span>](run.md)
-   [<span data-ttu-id="5de7e-128">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="5de7e-128">**Configure**</span></span>](configure.md)

<span data-ttu-id="5de7e-129">L'esperto deve implementare ognuna delle funzioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5de7e-129">The expert must implement each of the preceding functions.</span></span>

 

 



