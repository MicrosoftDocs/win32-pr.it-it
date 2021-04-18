---
title: Registrazione di plug-in di conversione
description: Registrazione di plug-in di conversione
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player, plug-in di conversione
- Plug-in di Windows Media Player, conversione
- plug-in, conversione
- plug-in di conversione, registrazione
- Registro di sistema, plug-in di conversione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298063"
---
# <a name="registering-conversion-plug-ins"></a><span data-ttu-id="acc05-108">Registrazione di plug-in di conversione</span><span class="sxs-lookup"><span data-stu-id="acc05-108">Registering Conversion Plug-ins</span></span>

<span data-ttu-id="acc05-109">I formati di terze parti devono essere registrati prima che Windows Media Player possa creare un'istanza e usare il plug-in di conversione.</span><span class="sxs-lookup"><span data-stu-id="acc05-109">Third-party formats must be registered before Windows Media Player can instantiate and use the conversion plug-in.</span></span> <span data-ttu-id="acc05-110">Per registrare il file per la conversione, è necessario registrare l'estensione del nome file associata al formato.</span><span class="sxs-lookup"><span data-stu-id="acc05-110">To register your file for conversion, you must register the file name extension associated with your format.</span></span>

<span data-ttu-id="acc05-111">L'elenco delle estensioni di file registrate viene mantenuto come un set di chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="acc05-111">The list of registered file name extensions is maintained as a set of registry keys.</span></span> <span data-ttu-id="acc05-112">Per informazioni dettagliate sulla registrazione di formati di terze parti, vedere [impostazioni del registro di sistema per l'estensione del nome file](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="acc05-112">For details about registering third-party formats, see [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="acc05-113">Nella tabella seguente sono elencate le impostazioni relative ai valori del registro di sistema per registrare un formato di terze parti per la conversione tramite un plug-in di conversione.</span><span class="sxs-lookup"><span data-stu-id="acc05-113">The following table lists the registry value settings to register a third-party format for conversion by using a conversion plug-in.</span></span>



| <span data-ttu-id="acc05-114">Valore</span><span class="sxs-lookup"><span data-stu-id="acc05-114">Value</span></span>                  | <span data-ttu-id="acc05-115">Impostazione</span><span class="sxs-lookup"><span data-stu-id="acc05-115">Setting</span></span>                                                     |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="acc05-116">**Runtime**</span><span class="sxs-lookup"><span data-stu-id="acc05-116">**Runtime**</span></span>            | <span data-ttu-id="acc05-117">13</span><span class="sxs-lookup"><span data-stu-id="acc05-117">13</span></span>                                                          |
| <span data-ttu-id="acc05-118">**Autorizzazioni**</span><span class="sxs-lookup"><span data-stu-id="acc05-118">**Permissions**</span></span>        | <span data-ttu-id="acc05-119">8 (autorizzazione per la libreria).</span><span class="sxs-lookup"><span data-stu-id="acc05-119">8 (Permission for the library).</span></span>                             |
| <span data-ttu-id="acc05-120">**ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="acc05-120">**ConvertPluginCLSID**</span></span> | <span data-ttu-id="acc05-121">ID della classe del plug-in di conversione, nel formato del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="acc05-121">The class ID of the conversion plug-in, in registry format.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="acc05-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acc05-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acc05-123">**Riferimento alla programmazione di plug-in di conversione**</span><span class="sxs-lookup"><span data-stu-id="acc05-123">**Conversion Plug-ins Programming Reference**</span></span>](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




