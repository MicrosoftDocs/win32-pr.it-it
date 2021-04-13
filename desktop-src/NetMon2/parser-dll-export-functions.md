---
description: Le funzioni, elencate nella tabella seguente, sono punti di ingresso per le dll del parser. Le funzioni sono i punti di ingresso per le chiamate dal sistema operativo e Network Monitor.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Funzioni di esportazione DLL del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401602"
---
# <a name="parser-dll-export-functions"></a><span data-ttu-id="81c9d-104">Funzioni di esportazione DLL del parser</span><span class="sxs-lookup"><span data-stu-id="81c9d-104">Parser DLL Export Functions</span></span>

<span data-ttu-id="81c9d-105">Le funzioni, elencate nella tabella seguente, sono punti di ingresso per le dll del parser.</span><span class="sxs-lookup"><span data-stu-id="81c9d-105">The functions, listed in the following table, are entry points for parser DLLs.</span></span> <span data-ttu-id="81c9d-106">Le funzioni sono i punti di ingresso per le chiamate dal sistema operativo e Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="81c9d-106">The functions are the entry points for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="81c9d-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="81c9d-107">Function</span></span>                                           | <span data-ttu-id="81c9d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81c9d-108">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81c9d-109">Parser DllMain</span><span class="sxs-lookup"><span data-stu-id="81c9d-109">DllMain Parser</span></span>](dllmain-parser.md)               | <span data-ttu-id="81c9d-110">Indica alla DLL del parser che è caricata o scaricata.</span><span class="sxs-lookup"><span data-stu-id="81c9d-110">Indicates to the parser DLL that it is loaded or unloaded.</span></span> <span data-ttu-id="81c9d-111">Il sistema operativo chiama la funzione del **parser DllMain** quando un processo carica o Scarica la dll.</span><span class="sxs-lookup"><span data-stu-id="81c9d-111">The operating system calls the **DllMain Parser** function when a process loads or unloads the DLL.</span></span> |
| [<span data-ttu-id="81c9d-112">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="81c9d-112">AttachProperties</span></span>](attachproperties.md)           | <span data-ttu-id="81c9d-113">Notifica al parser di alleghi eventuali proprietà presenti in un frame.</span><span class="sxs-lookup"><span data-stu-id="81c9d-113">Notifies the parser to attach any properties that exist in a frame.</span></span>                                                                                            |
| [<span data-ttu-id="81c9d-114">Annullamento registrazione</span><span class="sxs-lookup"><span data-stu-id="81c9d-114">Deregister</span></span>](deregister.md)                       | <span data-ttu-id="81c9d-115">Notifica al parser di eseguire la pulizia.</span><span class="sxs-lookup"><span data-stu-id="81c9d-115">Notifies the parser to clean up.</span></span>                                                                                                                               |
| [<span data-ttu-id="81c9d-116">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="81c9d-116">FormatProperties</span></span>](formatproperties.md)           | <span data-ttu-id="81c9d-117">Notifica al parser di prendere tutte le istanze di proprietà in e di compilare il membro **szPropertyText** di ogni struttura **PROPERTYINST** .</span><span class="sxs-lookup"><span data-stu-id="81c9d-117">Notifies the parser to take all of the property instances in and build the **szPropertyText** member of each **PROPERTYINST** structure.</span></span>                       |
| [<span data-ttu-id="81c9d-118">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="81c9d-118">RecognizeFrame</span></span>](recognizeframe.md)               | <span data-ttu-id="81c9d-119">Determina se il parser può interpretare i dati del frame non elaborati con il protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="81c9d-119">Determines whether the parser can interpret the unprocessed frame data with the specified protocol.</span></span>                                                            |
| [<span data-ttu-id="81c9d-120">Registra parser</span><span class="sxs-lookup"><span data-stu-id="81c9d-120">Register Parser</span></span>](register-parser.md)             | <span data-ttu-id="81c9d-121">Determina le informazioni di base sul parser all'interno della DLL.</span><span class="sxs-lookup"><span data-stu-id="81c9d-121">Determines basic information about the parser within the DLL.</span></span> <span data-ttu-id="81c9d-122">Network Monitor chiama la funzione **Register parser** .</span><span class="sxs-lookup"><span data-stu-id="81c9d-122">Network Monitor calls the **Register Parser** function.</span></span>                                          |
| [<span data-ttu-id="81c9d-123">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="81c9d-123">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md) | <span data-ttu-id="81c9d-124">Installa un parser automaticamente.</span><span class="sxs-lookup"><span data-stu-id="81c9d-124">Installs a parser automatically.</span></span>                                                                                                                               |



 

<span data-ttu-id="81c9d-125">Network Monitor fornisce le funzioni di supporto e le strutture che possono essere chiamate dal parser.</span><span class="sxs-lookup"><span data-stu-id="81c9d-125">Network Monitor provides structures and helper functions that the parser can call.</span></span>



| <span data-ttu-id="81c9d-126">Per altre informazioni su</span><span class="sxs-lookup"><span data-stu-id="81c9d-126">For more information about</span></span>                          | <span data-ttu-id="81c9d-127">Vedere</span><span class="sxs-lookup"><span data-stu-id="81c9d-127">See</span></span>                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="81c9d-128">Funzioni helper che possono essere chiamate da esperti e analizzatori.</span><span class="sxs-lookup"><span data-stu-id="81c9d-128">Helper functions that experts and parsers can call.</span></span> | [<span data-ttu-id="81c9d-129">Funzioni comuni di esperti e parser</span><span class="sxs-lookup"><span data-stu-id="81c9d-129">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="81c9d-130">Funzioni helper che possono essere chiamate solo dai parser.</span><span class="sxs-lookup"><span data-stu-id="81c9d-130">Helper functions that only parsers can call.</span></span>        | [<span data-ttu-id="81c9d-131">Funzioni del parser</span><span class="sxs-lookup"><span data-stu-id="81c9d-131">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="81c9d-132">Strutture utilizzate dalle funzioni del parser.</span><span class="sxs-lookup"><span data-stu-id="81c9d-132">Structures that parser functions use.</span></span>               | [<span data-ttu-id="81c9d-133">Strutture del parser</span><span class="sxs-lookup"><span data-stu-id="81c9d-133">Parser Structures</span></span>](parser-structures.md)                                   |



 

 

 



