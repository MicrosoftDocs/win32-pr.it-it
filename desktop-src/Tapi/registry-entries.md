---
description: I terminali collegabili sono classificati in superclassi terminal.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Voci del registro di sistema (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319871"
---
# <a name="registry-entries-telephony-api"></a><span data-ttu-id="acdc0-103">Voci del registro di sistema (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="acdc0-103">Registry Entries (Telephony API)</span></span>

<span data-ttu-id="acdc0-104">I terminali collegabili sono classificati in superclassi terminal.</span><span class="sxs-lookup"><span data-stu-id="acdc0-104">The pluggable terminals are classified into Terminal Superclasses.</span></span> <span data-ttu-id="acdc0-105">Ogni superclasse terminal include una voce nel registro di sistema con la seguente chiave:</span><span class="sxs-lookup"><span data-stu-id="acdc0-105">Each Terminal Superclass has an entry in the registry under the following key:</span></span>

<span data-ttu-id="acdc0-106">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **telefonia** \\ **TerminalManager**</span><span class="sxs-lookup"><span data-stu-id="acdc0-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Telephony**\\**TerminalManager**</span></span>

<span data-ttu-id="acdc0-107">Sotto la chiave della superclasse terminale sono presenti voci per ogni terminale collegabile all'interno della superclasse terminal.</span><span class="sxs-lookup"><span data-stu-id="acdc0-107">Below the Terminal Superclass key are entries for each pluggable terminal within the Terminal Superclass.</span></span>

<span data-ttu-id="acdc0-108">La voce per ogni superclasse terminal è identificata da un CLSID della superclasse terminale.</span><span class="sxs-lookup"><span data-stu-id="acdc0-108">The entry for each Terminal Superclass is identified by a Terminal Superclass CLSID.</span></span> <span data-ttu-id="acdc0-109">Si tratta di un identificatore univoco per una classe terminale.</span><span class="sxs-lookup"><span data-stu-id="acdc0-109">This is a unique identifier for a terminal class.</span></span> <span data-ttu-id="acdc0-110">La classe terminal ha un attributo facoltativo: Name, che è un nome descrittivo per la classe terminal.</span><span class="sxs-lookup"><span data-stu-id="acdc0-110">The terminal class has an optional attribute: name, which is a friendly name for the terminal class.</span></span> <span data-ttu-id="acdc0-111">Ogni terminale innestabile è identificato da una classe di terminali CLSID; ovvero un GUID.</span><span class="sxs-lookup"><span data-stu-id="acdc0-111">Each pluggable terminal is identified by a CLSID Terminal class; that is, a GUID.</span></span> <span data-ttu-id="acdc0-112">Gli attributi per il terminale collegabile sono archiviati in valori di chiave del terminale di collegamento.</span><span class="sxs-lookup"><span data-stu-id="acdc0-112">The attributes for pluggable terminal are stored into pluggable terminal key values.</span></span> <span data-ttu-id="acdc0-113">Gli attributi per un terminale collegabile sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="acdc0-113">The attributes for a pluggable terminal are the following.</span></span>



| <span data-ttu-id="acdc0-114">Classe Terminal</span><span class="sxs-lookup"><span data-stu-id="acdc0-114">Terminal class</span></span> | <span data-ttu-id="acdc0-115">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="acdc0-115">Key name</span></span> | <span data-ttu-id="acdc0-116">Identificatore pubblico</span><span class="sxs-lookup"><span data-stu-id="acdc0-116">Public identifier</span></span>                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="acdc0-117">Nome</span><span class="sxs-lookup"><span data-stu-id="acdc0-117">Name</span></span>           | <span data-ttu-id="acdc0-118">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="acdc0-118">REG\_SZ</span></span>  | <span data-ttu-id="acdc0-119">Nome descrittivo del terminale</span><span class="sxs-lookup"><span data-stu-id="acdc0-119">Terminal friendly name</span></span>                                                            |
| <span data-ttu-id="acdc0-120">Company</span><span class="sxs-lookup"><span data-stu-id="acdc0-120">Company</span></span>        | <span data-ttu-id="acdc0-121">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="acdc0-121">REG\_SZ</span></span>  | <span data-ttu-id="acdc0-122">Nome azienda</span><span class="sxs-lookup"><span data-stu-id="acdc0-122">Company name</span></span>                                                                      |
| <span data-ttu-id="acdc0-123">Versione</span><span class="sxs-lookup"><span data-stu-id="acdc0-123">Version</span></span>        | <span data-ttu-id="acdc0-124">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="acdc0-124">REG\_SZ</span></span>  | <span data-ttu-id="acdc0-125">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="acdc0-125">Version information</span></span>                                                               |
| <span data-ttu-id="acdc0-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="acdc0-126">CLSID</span></span>          | <span data-ttu-id="acdc0-127">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="acdc0-127">REG\_SZ</span></span>  | <span data-ttu-id="acdc0-128">CLSID terminale (usato nel metodo COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) )</span><span class="sxs-lookup"><span data-stu-id="acdc0-128">Terminal CLSID (used in COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method)</span></span> |
| <span data-ttu-id="acdc0-129">Indicazioni</span><span class="sxs-lookup"><span data-stu-id="acdc0-129">Directions</span></span>     | <span data-ttu-id="acdc0-130">DWORD</span><span class="sxs-lookup"><span data-stu-id="acdc0-130">DWORD</span></span>    | <span data-ttu-id="acdc0-131">Direzione del terminale</span><span class="sxs-lookup"><span data-stu-id="acdc0-131">Terminal direction</span></span>                                                                |
| <span data-ttu-id="acdc0-132">MediaTypes</span><span class="sxs-lookup"><span data-stu-id="acdc0-132">MediaTypes</span></span>     | <span data-ttu-id="acdc0-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="acdc0-133">DWORD</span></span>    | <span data-ttu-id="acdc0-134">Tipi di supporti terminali supportati</span><span class="sxs-lookup"><span data-stu-id="acdc0-134">Terminal media types supported</span></span>                                                    |



 

<span data-ttu-id="acdc0-135">Per una classe terminal gli attributi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="acdc0-135">For a terminal class the attributes are the following.</span></span>



| <span data-ttu-id="acdc0-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="acdc0-136">CLSID</span></span> | <span data-ttu-id="acdc0-137">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="acdc0-137">Key name</span></span> | <span data-ttu-id="acdc0-138">Identificatore pubblico</span><span class="sxs-lookup"><span data-stu-id="acdc0-138">Public identifier</span></span>            |
|-------|----------|------------------------------|
| <span data-ttu-id="acdc0-139">Nome</span><span class="sxs-lookup"><span data-stu-id="acdc0-139">Name</span></span>  | <span data-ttu-id="acdc0-140">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="acdc0-140">REG\_SZ</span></span>  | <span data-ttu-id="acdc0-141">Nome descrittivo della classe Terminal</span><span class="sxs-lookup"><span data-stu-id="acdc0-141">Terminal class friendly name</span></span> |



 

 

 
