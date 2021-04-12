---
title: Negozi online privati
description: Negozi online privati
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player Online Stores, privato
- negozi online, privati
- digitare 1 negozi online, privato
- digitare 2 archivi online, privato
- negozi online privati
- Registro di sistema, archivi online privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396358"
---
# <a name="private-online-stores"></a><span data-ttu-id="65894-109">Negozi online privati</span><span class="sxs-lookup"><span data-stu-id="65894-109">Private Online Stores</span></span>

<span data-ttu-id="65894-110">Windows Media Player 10 o versioni successive supporta i negozi online privati; ovvero archivi visibili solo a determinati utenti.</span><span class="sxs-lookup"><span data-stu-id="65894-110">Windows Media Player 10 or later supports private online stores; that is, stores that are visible only to certain users.</span></span> <span data-ttu-id="65894-111">Perché un archivio online privato sia visibile all'utente corrente, è necessario che sia presente una voce che rappresenta l'archivio online privato nella seguente chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="65894-111">For a private online store to be visible to the current user, there must be an entry that represents the private online store under the following registry key.</span></span>

<span data-ttu-id="65894-112">HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ PrivateServices</span><span class="sxs-lookup"><span data-stu-id="65894-112">HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\PrivateServices</span></span>

<span data-ttu-id="65894-113">La voce del registro di sistema obbligatoria deve avere il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="65894-113">The required registry entry must have the following format.</span></span>



| <span data-ttu-id="65894-114">Nome</span><span class="sxs-lookup"><span data-stu-id="65894-114">Name</span></span>                                                         | <span data-ttu-id="65894-115">Type</span><span class="sxs-lookup"><span data-stu-id="65894-115">Type</span></span>           | <span data-ttu-id="65894-116">valore</span><span class="sxs-lookup"><span data-stu-id="65894-116">Value</span></span>                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="65894-117">Qualsiasi nome scelto dall'utente che crea la voce del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="65894-117">Any name chosen by the person who creates the registry entry</span></span> | <span data-ttu-id="65894-118">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="65894-118">**REG\_DWORD**</span></span> | <span data-ttu-id="65894-119">Un numero, fornito da Microsoft, che identifica lo Store online privato</span><span class="sxs-lookup"><span data-stu-id="65894-119">A number, provided by Microsoft, that identifies the private online store</span></span> |



 

<span data-ttu-id="65894-120">Il controllo ActiveX di Windows Media Player 10 supporta i negozi online privati solo se il controllo è in esecuzione in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="65894-120">The Windows Media Player 10 ActiveX control supports private online stores only if the control is running in remote mode.</span></span> <span data-ttu-id="65894-121">Il controllo ActiveX di Windows Media Player 11 supporta i negozi online privati indipendentemente dal fatto che il controllo sia in esecuzione in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="65894-121">The Windows Media Player 11 ActiveX control supports private online stores regardless of whether the control is running in remote mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65894-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65894-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65894-123">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="65894-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




