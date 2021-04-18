---
title: Per aggiungere dati di script all'intestazione
description: Per aggiungere dati di script all'intestazione
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media Format SDK, aggiunta di dati di script alle intestazioni
- ASF (Advanced Systems Format), aggiunta di dati di script alle intestazioni
- ASF (Advanced Systems Format), aggiunta di dati di script a intestazioni
- script, aggiunta di dati alle intestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299522"
---
# <a name="to-add-script-data-to-the-header"></a><span data-ttu-id="b3742-107">Per aggiungere dati di script all'intestazione</span><span class="sxs-lookup"><span data-stu-id="b3742-107">To Add Script Data to the Header</span></span>

<span data-ttu-id="b3742-108">È possibile includere comandi script nell'intestazione di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="b3742-108">You can include script commands in the header of an ASF file.</span></span> <span data-ttu-id="b3742-109">Per scrivere comandi script nell'intestazione al momento della codifica, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="b3742-109">To write script commands to the header at the time of encoding, perform the following steps.</span></span> <span data-ttu-id="b3742-110">Eseguire questi passaggi prima di chiamare [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="b3742-110">Perform these steps prior to calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

1.  <span data-ttu-id="b3742-111">Ottenere un puntatore all'interfaccia **IWMHeaderInfo** chiamando **IWMWriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="b3742-111">Obtain a pointer to the **IWMHeaderInfo** interface by calling **IWMWriter::QueryInterface**.</span></span>
2.  <span data-ttu-id="b3742-112">Aggiungere ogni comando script desiderato chiamando [**IWMHeaderInfo:: addScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span><span class="sxs-lookup"><span data-stu-id="b3742-112">Add each desired script command by calling [**IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span></span> <span data-ttu-id="b3742-113">Ogni chiamata accetta le due stringhe separatamente e l'ora di presentazione da usare per il comando come parametri.</span><span class="sxs-lookup"><span data-stu-id="b3742-113">Each call takes the two strings separately and the presentation time to be used for the command as parameters.</span></span>

<span data-ttu-id="b3742-114">Quando un'applicazione legge il file, sarà necessario recuperare tutti i comandi di script.</span><span class="sxs-lookup"><span data-stu-id="b3742-114">When an application reads the file, it will need to retrieve all of the script commands.</span></span> <span data-ttu-id="b3742-115">Per trovare tutti i comandi script nell'intestazione di un file, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="b3742-115">To find all script commands in the header of a file, perform the following steps.</span></span> <span data-ttu-id="b3742-116">Questa operazione deve essere eseguita prima di avviare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b3742-116">This should be done before starting playback.</span></span>

1.  <span data-ttu-id="b3742-117">Ottenere un puntatore all'interfaccia **IWMHeaderInfo** dell'oggetto Reader (o oggetto Reader sincrono) chiamando il metodo **QueryInterface** di un'altra interfaccia nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b3742-117">Obtain a pointer to the **IWMHeaderInfo** interface of the reader object (or synchronous reader object) by calling the **QueryInterface** method of another interface in the object.</span></span>
2.  <span data-ttu-id="b3742-118">Ottenere il numero totale di script nell'intestazione chiamando [**IWMHeaderInfo:: GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span><span class="sxs-lookup"><span data-stu-id="b3742-118">Get the total number of scripts in the header by calling [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span></span>
3.  <span data-ttu-id="b3742-119">Eseguire il ciclo di tutti gli script nell'intestazione uno alla volta usando le chiamate a [**IWMHeaderInfo:: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span><span class="sxs-lookup"><span data-stu-id="b3742-119">Loop through all of the scripts in the header one at a time using calls to [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span></span>
4.  <span data-ttu-id="b3742-120">Creare un elenco di orari di presentazione in modo che l'applicazione possa rispondere ai comandi al momento opportuno.</span><span class="sxs-lookup"><span data-stu-id="b3742-120">Create a list of the presentation times so that your application can react to the commands at the appropriate time.</span></span>

> [!Note]  
> <span data-ttu-id="b3742-121">Quando si usa il DRM per crittografare un file, nessun comando di script può avere un tempo di presentazione pari a 0.</span><span class="sxs-lookup"><span data-stu-id="b3742-121">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b3742-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b3742-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3742-123">**Interfaccia IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="b3742-123">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="b3742-124">**Interfaccia IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="b3742-124">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="b3742-125">**Uso di comandi script**</span><span class="sxs-lookup"><span data-stu-id="b3742-125">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




