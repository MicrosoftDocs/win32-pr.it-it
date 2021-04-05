---
title: Cosa deve fare l'installazione
description: I nuovi attributi a cui si fa riferimento nel passaggio 3 devono essere indicati dal relativo OID perché il nuovo nome dell'attributo non è presente nella cache dello schema a questo punto.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Cosa deve fare l'installazione di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955125"
---
# <a name="what-the-installation-must-do"></a><span data-ttu-id="a86b8-104">Cosa deve fare l'installazione</span><span class="sxs-lookup"><span data-stu-id="a86b8-104">What the Installation Must Do</span></span>

<span data-ttu-id="a86b8-105">Le applicazioni che estendono lo schema devono applicare gli aggiornamenti come descritto nella procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="a86b8-105">Applications that extend the schema, must apply updates as described in the following procedure.</span></span>

<span data-ttu-id="a86b8-106">**Per applicare gli aggiornamenti quando si estende lo schema**</span><span class="sxs-lookup"><span data-stu-id="a86b8-106">**To apply updates when extending the schema**</span></span>

1.  <span data-ttu-id="a86b8-107">Aggiungere i nuovi attributi.</span><span class="sxs-lookup"><span data-stu-id="a86b8-107">Add the new attributes.</span></span>
2.  <span data-ttu-id="a86b8-108">Aggiungere le nuove classi.</span><span class="sxs-lookup"><span data-stu-id="a86b8-108">Add the new classes.</span></span>
3.  <span data-ttu-id="a86b8-109">Aggiungere i nuovi attributi alle classi.</span><span class="sxs-lookup"><span data-stu-id="a86b8-109">Add the new attributes to classes.</span></span>
4.  <span data-ttu-id="a86b8-110">Attivare un ricaricamento della cache.</span><span class="sxs-lookup"><span data-stu-id="a86b8-110">Trigger a cache reload.</span></span>

<span data-ttu-id="a86b8-111">I nuovi attributi a cui si fa riferimento nel passaggio 3 devono essere indicati dal relativo OID perché il nuovo nome dell'attributo non è presente nella cache dello schema a questo punto.</span><span class="sxs-lookup"><span data-stu-id="a86b8-111">New attributes referenced in Step 3 must be referred to by its OID because the new attribute name is not present in the schema cache at this point.</span></span>

<span data-ttu-id="a86b8-112">Il passaggio 4 non è necessario se le estensioni non verranno utilizzate immediatamente; le estensioni verranno visualizzate nella cache dello schema in circa 5 minuti, a seconda del carico di sistema.</span><span class="sxs-lookup"><span data-stu-id="a86b8-112">Step 4 is unnecessary if the extensions will not be used immediately; the extensions will appear in the schema cache in approximately 5 minutes, depending on system load.</span></span> <span data-ttu-id="a86b8-113">Per ulteriori informazioni sulla cache degli schemi e su come attivare un ricaricamento della cache, vedere [aggiornamento della cache dello schema](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="a86b8-113">For more information about the schema cache and how to trigger a cache reload, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>

 

 




