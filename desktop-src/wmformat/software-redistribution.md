---
title: Ridistribuzione del software
description: Ridistribuzione del software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media Format SDK, ridistribuzione software
- ASF (Advanced Systems Format), ridistribuzione del software
- ASF (formato avanzato dei sistemi), ridistribuzione del software
- Windows Media Format SDK, ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ASF (formato avanzato dei sistemi), ridistribuzione
- ridistribuzione del software, informazioni
- ridistribuzione, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709475"
---
# <a name="software-redistribution"></a><span data-ttu-id="a3562-111">Ridistribuzione del software</span><span class="sxs-lookup"><span data-stu-id="a3562-111">Software Redistribution</span></span>

<span data-ttu-id="a3562-112">L'inclusione di software in formato Windows Media in un'installazione di applicazione è nota come ridistribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3562-112">The inclusion of Windows Media Format software in an application setup is known as redistribution.</span></span> <span data-ttu-id="a3562-113">Windows Media Format SDK include un pacchetto di installazione che può essere incluso nella configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3562-113">The Windows Media Format SDK includes an installation package which can be included with your application setup.</span></span> <span data-ttu-id="a3562-114">Il pacchetto di installazione è un file eseguibile denominato wmfdist95.exe.</span><span class="sxs-lookup"><span data-stu-id="a3562-114">The installation package is an executable file named wmfdist95.exe.</span></span> <span data-ttu-id="a3562-115">Quando si installa Windows Media Format SDK, il pacchetto di installazione viene copiato nella \\ cartella Redist della directory di installazione (c: \\ WMSDK \\ wmfsdk per impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="a3562-115">When you install the Windows Media Format SDK, the installation package is copied to the \\Redist folder of the install directory (c:\\wmsdk\\wmfsdk by default).</span></span>

<span data-ttu-id="a3562-116">Nelle sezioni seguenti vengono fornite le procedure e altre informazioni per la configurazione della ridistribuzione software.</span><span class="sxs-lookup"><span data-stu-id="a3562-116">The following sections provide procedures and other information for software redistribution setup.</span></span>



| <span data-ttu-id="a3562-117">Sezione</span><span class="sxs-lookup"><span data-stu-id="a3562-117">Section</span></span>                                                                            | <span data-ttu-id="a3562-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3562-118">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3562-119">Per creare una configurazione di ridistribuzione</span><span class="sxs-lookup"><span data-stu-id="a3562-119">To Create a Redistribution Setup</span></span>](to-create-a-redistribution-setup.md)           | <span data-ttu-id="a3562-120">Viene descritta la procedura per la creazione di una configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3562-120">Describes the procedure for creating an application setup.</span></span>                                                                                                                       |
| [<span data-ttu-id="a3562-121">Rilevamento dello stato di installazione</span><span class="sxs-lookup"><span data-stu-id="a3562-121">Detecting Setup Status</span></span>](detecting-setup-status.md)                               | <span data-ttu-id="a3562-122">Fornisce il codice di esempio che controlla lo stato di installazione del registro di sistema per determinare se è necessario installare il pacchetto di ridistribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3562-122">Provides example code that checks the registry for installation status to determine whether the redistribution package needs to be installed.</span></span>                                    |
| [<span data-ttu-id="a3562-123">Codice di esempio per l'installazione della ridistribuzione</span><span class="sxs-lookup"><span data-stu-id="a3562-123">Example Code for Redistribution Setup</span></span>](example-code-for-redistribution-setup.md) | <span data-ttu-id="a3562-124">Fornisce il codice di esempio che può essere utilizzato nella routine di installazione per eseguire i pacchetti di ridistribuzione in modalità non interattiva e notificare la routine di installazione quando il computer deve essere riavviato.</span><span class="sxs-lookup"><span data-stu-id="a3562-124">Provides example code that can be used in your setup routine to run the redistribution packages in quiet mode and notify your setup routine when the computer must be restarted.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a3562-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3562-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3562-126">**Considerazioni sui progetti**</span><span class="sxs-lookup"><span data-stu-id="a3562-126">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




