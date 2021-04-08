---
title: Uso di comandi script
description: Uso di comandi script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows Media Format SDK, comandi script
- ASF (Advanced Systems Format), comandi script
- ASF (Advanced Systems Format), comandi script
- script, comandi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044797"
---
# <a name="using-script-commands"></a><span data-ttu-id="b60b7-107">Uso di comandi script</span><span class="sxs-lookup"><span data-stu-id="b60b7-107">Using Script Commands</span></span>

<span data-ttu-id="b60b7-108">Windows Media Format SDK supporta l'uso di comandi script per comunicare le azioni dell'applicazione nei file ASF.</span><span class="sxs-lookup"><span data-stu-id="b60b7-108">The Windows Media Format SDK supports the use of script commands to communicate application actions in ASF files.</span></span> <span data-ttu-id="b60b7-109">Ogni comando di script è costituito da due stringhe, la prima stringa è il tipo di comando, il secondo è costituito dai dati del comando.</span><span class="sxs-lookup"><span data-stu-id="b60b7-109">Each script command is made up of two strings, the first string is the type of command, the second is the command data.</span></span> <span data-ttu-id="b60b7-110">Ad esempio, è possibile usare il tipo di script "URL" e passare un URL Internet valido come dati del comando.</span><span class="sxs-lookup"><span data-stu-id="b60b7-110">For example, you can use the script type "URL" and pass a valid Internet URL as the command data.</span></span> <span data-ttu-id="b60b7-111">Quando un'applicazione di lettura che supporta i comandi script di tipo "URL" riceve questo comando, l'indirizzo specificato verrà aperto in una finestra del browser.</span><span class="sxs-lookup"><span data-stu-id="b60b7-111">When a reading application that supports script commands of type "URL" receives this command, it will open the specified address in a browser window.</span></span>

<span data-ttu-id="b60b7-112">Windows Media Format SDK fornisce due opzioni per la distribuzione di script nei file ASF.</span><span class="sxs-lookup"><span data-stu-id="b60b7-112">The Windows Media Format SDK provides two options for delivering script in ASF files.</span></span> <span data-ttu-id="b60b7-113">È possibile creare un flusso di script oppure è possibile includere i comandi di script nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="b60b7-113">You can create a script stream or you can include script commands in the header of the file.</span></span> <span data-ttu-id="b60b7-114">I flussi di script sono utili perché i comandi di script vengono recapitati nell'ordine temporale della presentazione.</span><span class="sxs-lookup"><span data-stu-id="b60b7-114">Script streams are useful because the script commands are delivered in presentation time order.</span></span> <span data-ttu-id="b60b7-115">Se si usano i comandi script nell'intestazione del file, l'applicazione dovrà recuperare tutti i comandi di script prima di avviare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b60b7-115">If you use script commands in the file header, your application will need to retrieve all of the script commands before starting playback.</span></span> <span data-ttu-id="b60b7-116">È necessario tenere traccia dei tempi di presentazione dei comandi script e rispondere al momento giusto.</span><span class="sxs-lookup"><span data-stu-id="b60b7-116">You must keep track of the presentation times of script commands and respond to them at the right time.</span></span>

<span data-ttu-id="b60b7-117">Nelle sezioni seguenti viene descritto come includere comandi script in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="b60b7-117">The following sections describe how to include script commands in an ASF file.</span></span>



| <span data-ttu-id="b60b7-118">Sezione</span><span class="sxs-lookup"><span data-stu-id="b60b7-118">Section</span></span>                                                                                                                | <span data-ttu-id="b60b7-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b60b7-119">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="b60b7-120">Per usare un flusso di script</span><span class="sxs-lookup"><span data-stu-id="b60b7-120">To Use a Script Stream</span></span>](to-use-a-script-stream.md)                                                                   | <span data-ttu-id="b60b7-121">Viene descritto come includere comandi script in un flusso di script.</span><span class="sxs-lookup"><span data-stu-id="b60b7-121">Describes how to include script commands in a script stream.</span></span> |
| [<span data-ttu-id="b60b7-122">Per aggiungere dati di script all'intestazione</span><span class="sxs-lookup"><span data-stu-id="b60b7-122">To Add Script Data to the Header</span></span>](to-add-script-data-to-the-header.md)                                               | <span data-ttu-id="b60b7-123">Viene descritto come includere i comandi script nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="b60b7-123">Describes how to include script commands in the file header.</span></span> |
| [<span data-ttu-id="b60b7-124">Uso di comandi script supportati da Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="b60b7-124">Using Script Commands Supported by Windows Media Player</span></span>](using-script-commands-supported-by-windows-media-player.md) | <span data-ttu-id="b60b7-125">Descrive i comandi script usati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b60b7-125">Describes the script commands used by Windows Media Player.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="b60b7-126">Nelle versioni precedenti di Windows Media Format SDK, i flussi di script venivano usati per aprire indirizzi Web corrispondenti al contenuto di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="b60b7-126">In previous versions of the Windows Media Format SDK, script streams were used to open Web addresses corresponding to the content of an ASF file.</span></span> <span data-ttu-id="b60b7-127">È ora possibile usare i flussi Web per lavorare con le pagine Web sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="b60b7-127">You can now use Web streams to work with synchronized Web pages.</span></span> <span data-ttu-id="b60b7-128">Per altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b60b7-128">For more information.</span></span> <span data-ttu-id="b60b7-129">vedere [flussi Web](web-streams.md).</span><span class="sxs-lookup"><span data-stu-id="b60b7-129">see [Web Streams](web-streams.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b60b7-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b60b7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b60b7-131">**Comandi script**</span><span class="sxs-lookup"><span data-stu-id="b60b7-131">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="b60b7-132">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="b60b7-132">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




