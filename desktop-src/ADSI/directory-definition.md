---
title: Definizione directory
description: Il componente provider di esempio utilizza una struttura di directory relativamente semplice per chiarire la relazione tra i componenti e per mostrare i requisiti minimi necessari per essere un provider ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855325"
---
# <a name="directory-definition"></a><span data-ttu-id="42ae4-103">Definizione directory</span><span class="sxs-lookup"><span data-stu-id="42ae4-103">Directory Definition</span></span>

<span data-ttu-id="42ae4-104">Il componente provider di esempio utilizza una struttura di directory relativamente semplice per chiarire la relazione tra i componenti e per mostrare i requisiti minimi necessari per essere un provider ADSI.</span><span class="sxs-lookup"><span data-stu-id="42ae4-104">The example provider component uses a relatively simple directory design to clarify the relationship between components and to show the minimum requirements necessary to be an ADSI provider.</span></span>

<span data-ttu-id="42ae4-105">"Directory" per il componente provider di esempio è costituito da due nodi radice: "Seattle" e "Toronto".</span><span class="sxs-lookup"><span data-stu-id="42ae4-105">The "directory" for the example provider component consists of two root nodes: "Seattle" and "Toronto".</span></span> <span data-ttu-id="42ae4-106">Seattle contiene altri due sottolivelli, "Bellevue" e "Redmond".</span><span class="sxs-lookup"><span data-stu-id="42ae4-106">Seattle contains two more sublevels, "Bellevue" and "Redmond".</span></span> <span data-ttu-id="42ae4-107">Ognuna di queste voci contiene diversi account utente.</span><span class="sxs-lookup"><span data-stu-id="42ae4-107">Each of these entries contains several user accounts.</span></span> <span data-ttu-id="42ae4-108">La voce "Toronto" non ha altri sottolivelli, ma contiene direttamente diversi account utente.</span><span class="sxs-lookup"><span data-stu-id="42ae4-108">The "Toronto" entry has no further sublevels, but directly contains several user accounts.</span></span> <span data-ttu-id="42ae4-109">Nella figura seguente vengono illustrati questi due nodi radice connessi a una rete.</span><span class="sxs-lookup"><span data-stu-id="42ae4-109">The following figure shows these two root nodes connected to a network.</span></span>

![definizione directory](images/dssmdo.png)

<span data-ttu-id="42ae4-111">In termini gerarchici, il nodo dello spazio dei nomi contiene "Seattle" e "Toronto".</span><span class="sxs-lookup"><span data-stu-id="42ae4-111">In hierarchical terms, the Namespace node contains "Seattle" and "Toronto".</span></span> <span data-ttu-id="42ae4-112">"Seattle" contiene "Bellevue" e "Redmond".</span><span class="sxs-lookup"><span data-stu-id="42ae4-112">"Seattle" contains "Bellevue" and "Redmond".</span></span> <span data-ttu-id="42ae4-113">"Bellevue" e "Redmond" contengono ognuno un set di account utente.</span><span class="sxs-lookup"><span data-stu-id="42ae4-113">"Bellevue" and "Redmond" each contain a set of user accounts.</span></span> <span data-ttu-id="42ae4-114">"Toronto" contiene direttamente gli account utente senza nodi organizzativi intermedi.</span><span class="sxs-lookup"><span data-stu-id="42ae4-114">"Toronto" directly contains the user accounts with no intermediate organizational nodes.</span></span>

<span data-ttu-id="42ae4-115">Il componente provider di esempio rappresenta questa struttura con solo due Active Directory tipi di oggetto: un oggetto contenitore e un oggetto foglia.</span><span class="sxs-lookup"><span data-stu-id="42ae4-115">The example provider component represents this structure with only two Active Directory object types: a container object and a leaf object.</span></span> <span data-ttu-id="42ae4-116">"Seattle", "Toronto", "Bellevue" e "Redmond" sono oggetti contenitore e ogni account utente è un oggetto foglia.</span><span class="sxs-lookup"><span data-stu-id="42ae4-116">"Seattle", "Toronto", "Bellevue", and "Redmond" are container objects and each user account is a leaf object.</span></span>

<span data-ttu-id="42ae4-117">Il componente provider di esempio crea una classe di schema denominata "unità organizzativa" per un tipo di oggetto contenitore e una classe di schema denominata "User" per un account utente.</span><span class="sxs-lookup"><span data-stu-id="42ae4-117">The example provider component creates a schema class called "Organizational Unit" for a container object type and a schema class called "User" for a user account.</span></span>

<span data-ttu-id="42ae4-118">Le proprietà per ogni classe dello schema, i relativi metodi e le regole che regolano le relazioni di contenimento per questi oggetti sono tutte definite nella [gestione dello schema](schema-management.md).</span><span class="sxs-lookup"><span data-stu-id="42ae4-118">The properties for each schema class, their methods, and the rules that govern the containment relationships for these objects are all defined in [Schema Management](schema-management.md).</span></span>

 

 




