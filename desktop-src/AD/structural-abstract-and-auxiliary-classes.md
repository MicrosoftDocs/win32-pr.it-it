---
title: Classi strutturali, astratte e ausiliarie
description: L'attributo objectClassCategory di un oggetto classSchema può avere un valore, come elencato nella tabella seguente, che indica se la classe è strutturale, astratta o ausiliaria.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Classi strutturali, astratte e ausiliarie AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044090"
---
# <a name="structural-abstract-and-auxiliary-classes"></a><span data-ttu-id="67a94-104">Classi strutturali, astratte e ausiliarie</span><span class="sxs-lookup"><span data-stu-id="67a94-104">Structural, Abstract, and Auxiliary Classes</span></span>

<span data-ttu-id="67a94-105">L'attributo **objectClassCategory** di un oggetto **classSchema** può avere un valore, come elencato nella tabella seguente, che indica se la classe è strutturale, astratta o ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="67a94-105">The **objectClassCategory** attribute of a **classSchema** object can have a value, as listed in the following table, that indicates whether the class is structural, abstract, or auxiliary.</span></span>



| <span data-ttu-id="67a94-106">Valore</span><span class="sxs-lookup"><span data-stu-id="67a94-106">Value</span></span> | <span data-ttu-id="67a94-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67a94-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a94-108">1</span><span class="sxs-lookup"><span data-stu-id="67a94-108">1</span></span>     | <span data-ttu-id="67a94-109">Classe strutturale, che è l'unico tipo di classe in cui possono essere presenti istanze in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="67a94-109">A structural class, which is the only type of class that can have instances in Active Directory Domain Services.</span></span> <span data-ttu-id="67a94-110">Una classe strutturale può essere una sottoclasse di una classe astratta o strutturale.</span><span class="sxs-lookup"><span data-stu-id="67a94-110">A structural class can be a subclass of an abstract or structural class.</span></span> <span data-ttu-id="67a94-111">Una classe strutturale può includere un numero qualsiasi di classi ausiliarie nella relativa definizione.</span><span class="sxs-lookup"><span data-stu-id="67a94-111">A structural class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="67a94-112">2</span><span class="sxs-lookup"><span data-stu-id="67a94-112">2</span></span>     | <span data-ttu-id="67a94-113">Una classe astratta, ovvero un modello usato per derivare nuove classi astratte, ausiliarie e strutturali.</span><span class="sxs-lookup"><span data-stu-id="67a94-113">An abstract class, which is a template used to derive new abstract, auxiliary, and structural classes.</span></span> <span data-ttu-id="67a94-114">Una classe astratta può essere solo una sottoclasse di una classe astratta.</span><span class="sxs-lookup"><span data-stu-id="67a94-114">An abstract class can only be a subclass of an abstract class.</span></span> <span data-ttu-id="67a94-115">Impossibile creare un'istanza delle classi astratte in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="67a94-115">Abstract classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="67a94-116">Una classe astratta può includere un numero qualsiasi di classi ausiliarie nella relativa definizione.</span><span class="sxs-lookup"><span data-stu-id="67a94-116">An abstract class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="67a94-117">3</span><span class="sxs-lookup"><span data-stu-id="67a94-117">3</span></span>     | <span data-ttu-id="67a94-118">Una classe ausiliaria, che può essere inclusa nella definizione di una classe strutturale, astratta o ausiliaria, nel qual caso i valori **mustContain**, **systemMustContain**, **mayContain** e **systemMayContain** della classe ausiliaria vengono aggiunti a quelli della classe.</span><span class="sxs-lookup"><span data-stu-id="67a94-118">An auxiliary class, which can be included in the definition of a structural, abstract, or auxiliary class, in which case, the **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain** values of the auxiliary class are added to those of the class.</span></span> <span data-ttu-id="67a94-119">Una classe ausiliaria può essere una sottoclasse di una classe astratta o ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="67a94-119">An auxiliary class can be a subclass of an abstract or auxiliary class.</span></span> <span data-ttu-id="67a94-120">Non è possibile creare un'istanza delle classi ausiliarie in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="67a94-120">Auxiliary classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="67a94-121">Una classe ausiliaria può includere un numero qualsiasi di classi ausiliarie nella relativa definizione.</span><span class="sxs-lookup"><span data-stu-id="67a94-121">An auxiliary class can include any number of auxiliary classes in its definition.</span></span> |



 

<span data-ttu-id="67a94-122">Non confondere **objectClassCategory** con una [categoria di oggetti](object-class-and-object-category.md).</span><span class="sxs-lookup"><span data-stu-id="67a94-122">Do not confuse the **objectClassCategory** with an [object category](object-class-and-object-category.md).</span></span>

 

 




