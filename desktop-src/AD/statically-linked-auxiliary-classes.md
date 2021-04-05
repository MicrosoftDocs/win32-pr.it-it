---
title: Classi ausiliarie collegate in modo statico
description: Una classe ausiliaria collegata in modo statico è una classe inclusa nell'attributo auxiliaryClass o systemAuxiliaryClass della definizione classSchema di una classe di oggetti nello schema.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Active Directory (classi ausiliarie) collegate in modo statico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707537"
---
# <a name="statically-linked-auxiliary-classes"></a><span data-ttu-id="a4dea-104">Classi ausiliarie collegate in modo statico</span><span class="sxs-lookup"><span data-stu-id="a4dea-104">Statically Linked Auxiliary Classes</span></span>

<span data-ttu-id="a4dea-105">Una classe ausiliaria collegata in modo statico è una classe inclusa nell'attributo **auxiliaryClass** o **SystemAuxiliaryClass** della definizione **classSchema** di una classe di oggetti nello schema.</span><span class="sxs-lookup"><span data-stu-id="a4dea-105">A statically linked auxiliary class is one that is included in the **auxiliaryClass** or **systemAuxiliaryClass** attribute of an object class's **classSchema** definition in the schema.</span></span> <span data-ttu-id="a4dea-106">Ciò significa che la classe ausiliaria fa parte di ogni istanza della classe a cui è associata.</span><span class="sxs-lookup"><span data-stu-id="a4dea-106">This means that the auxiliary class is part of every instance of the class with which it is associated.</span></span>

<span data-ttu-id="a4dea-107">Una classe ausiliaria può essere collegata in modo statico a una classe di oggetti quando la classe è definita, ovvero quando il relativo oggetto **classSchema** viene aggiunto al contenitore dello schema.</span><span class="sxs-lookup"><span data-stu-id="a4dea-107">An auxiliary class can be statically linked to an object class when the class is defined, that is, when its **classSchema** object is added to the schema container.</span></span> <span data-ttu-id="a4dea-108">Questa è l'unica volta in cui è possibile usare **systemAuxiliaryClass** . Dopo la creazione di un oggetto **classSchema** , non è possibile modificare l'attributo **systemAuxiliaryClass** .</span><span class="sxs-lookup"><span data-stu-id="a4dea-108">This is the only time that the **systemAuxiliaryClass** can be used; after a **classSchema** object is created, its **systemAuxiliaryClass** attribute cannot be modified.</span></span> <span data-ttu-id="a4dea-109">Una classe ausiliaria collegata in modo statico in questo momento può avere attributi obbligatori (**musthave**) e/o facoltativi (**Faran**).</span><span class="sxs-lookup"><span data-stu-id="a4dea-109">An auxiliary class that is statically linked at this time can have mandatory (**mustHave**) and/or optional (**mayHave**) attributes.</span></span>

<span data-ttu-id="a4dea-110">Un utente con privilegi con le autorizzazioni necessarie per estendere lo schema può aggiungere o rimuovere classi ausiliarie dall'attributo **systemAuxiliaryClass** di un oggetto **classSchema** esistente.</span><span class="sxs-lookup"><span data-stu-id="a4dea-110">A privileged user with the permissions required to extend the schema can add or remove auxiliary classes from the **systemAuxiliaryClass** attribute of an existing **classSchema** object.</span></span> <span data-ttu-id="a4dea-111">In questo modo viene aggiunta o rimossa la classe ausiliaria da tutte le istanze esistenti della classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="a4dea-111">Doing so adds or removes the auxiliary class from every existing instance of the object class.</span></span> <span data-ttu-id="a4dea-112">Una classe ausiliaria collegata in modo statico in questo momento può avere attributi facoltativi, ma non può avere attributi obbligatori.</span><span class="sxs-lookup"><span data-stu-id="a4dea-112">An auxiliary class that is statically linked at this time can have optional attributes, but cannot have mandatory attributes.</span></span> <span data-ttu-id="a4dea-113">Ciò è dovuto al fatto che possono esistere istanze della classe di oggetti. in questo caso, l'aggiunta di un nuovo attributo obbligatorio comporta la creazione di problemi.</span><span class="sxs-lookup"><span data-stu-id="a4dea-113">This is because there may be existing instances of the object class, in which case, adding a new mandatory attribute would create problems.</span></span> <span data-ttu-id="a4dea-114">Un utente con privilegi può quindi rimuovere una classe ausiliaria dall'attributo **auxiliaryClass** di un oggetto **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="a4dea-114">A privileged user can subsequently remove an auxiliary class from the **auxiliaryClass** attribute of a **classSchema** object.</span></span>

 

 




