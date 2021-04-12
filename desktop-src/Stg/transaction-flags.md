---
title: Flag di transazione
description: Un oggetto può essere aperto in modalità diretta o transazionale.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221599"
---
# <a name="transaction-flags"></a><span data-ttu-id="81466-103">Flag di transazione</span><span class="sxs-lookup"><span data-stu-id="81466-103">Transaction Flags</span></span>

<span data-ttu-id="81466-104">Un oggetto può essere aperto in modalità diretta o transazionale.</span><span class="sxs-lookup"><span data-stu-id="81466-104">An object can be opened in either direct or transacted mode.</span></span> <span data-ttu-id="81466-105">Quando un oggetto viene aperto in modalità diretta, le modifiche vengono apportate immediatamente e in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="81466-105">When an object is opened in direct mode, changes are made immediately and permanently.</span></span> <span data-ttu-id="81466-106">Quando un oggetto viene aperto in modalità transazionale, le modifiche vengono memorizzate nel buffer, in modo che sia possibile eseguirne il commit o il ripristino in modo esplicito al termine della modifica.</span><span class="sxs-lookup"><span data-stu-id="81466-106">When an object is opened in transacted mode, changes are buffered so they can be explicitly committed or reverted once editing is complete.</span></span> <span data-ttu-id="81466-107">Le modifiche di cui è stato eseguito il commit vengono salvate nell'oggetto mentre le modifiche ripristinate vengono eliminate.</span><span class="sxs-lookup"><span data-stu-id="81466-107">Committed changes are saved to the object while reverted changes are discarded.</span></span> <span data-ttu-id="81466-108">La modalità diretta è la modalità di accesso predefinita.</span><span class="sxs-lookup"><span data-stu-id="81466-108">Direct mode is the default access mode.</span></span>

<span data-ttu-id="81466-109">La modalità transazionale non è necessaria in un oggetto di archiviazione padre per poterla utilizzare in un elemento annidato.</span><span class="sxs-lookup"><span data-stu-id="81466-109">Transacted mode is not required on a parent storage object in order to use it on a nested element.</span></span> <span data-ttu-id="81466-110">Una transazione per un elemento annidato, tuttavia, è annidata all'interno della transazione per il relativo oggetto di archiviazione padre.</span><span class="sxs-lookup"><span data-stu-id="81466-110">A transaction for a nested element, however, is nested within the transaction for its parent storage object.</span></span> <span data-ttu-id="81466-111">Di conseguenza, non è possibile eseguire il commit delle modifiche apportate a un oggetto figlio fino a quando non viene eseguito il commit delle modifiche apportate all'elemento padre e non viene eseguito il commit di entrambe le modifiche fino a quando l'oggetto di archiviazione radice (l'elemento padre di livello superiore)</span><span class="sxs-lookup"><span data-stu-id="81466-111">Therefore, changes made to a child object cannot be committed until those made to the parent are committed, and both remain uncommitted until the root storage object (the top-level parent) is actually written to disk.</span></span> <span data-ttu-id="81466-112">In altre parole, le modifiche si spostano verso l'esterno: gli oggetti interni pubblicano le modifiche apportate alle transazioni dei contenitori immediati.</span><span class="sxs-lookup"><span data-stu-id="81466-112">In other words, the changes move outward: inner objects publish changes to the transactions of their immediate containers.</span></span>

 

 




