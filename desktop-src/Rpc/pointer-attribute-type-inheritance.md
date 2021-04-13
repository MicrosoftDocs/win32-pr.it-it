---
title: Ereditarietà del tipo di Pointer-Attribute
description: In base alla specifica DCE, ogni file IDL deve definire gli attributi per i relativi puntatori.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399541"
---
# <a name="pointer-attribute-type-inheritance"></a><span data-ttu-id="d2014-103">Ereditarietà del tipo di Pointer-Attribute</span><span class="sxs-lookup"><span data-stu-id="d2014-103">Pointer-Attribute Type Inheritance</span></span>

<span data-ttu-id="d2014-104">In base alla specifica DCE, ogni file IDL deve definire gli attributi per i relativi puntatori.</span><span class="sxs-lookup"><span data-stu-id="d2014-104">According to the DCE specification, each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="d2014-105">Se un attributo esplicito non è assegnato a un puntatore, il puntatore utilizzerà il valore specificato dalla \[ parola chiave [ \_ default del puntatore](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="d2014-105">If an explicit attribute is not assigned to a pointer, the pointer uses the value specified by the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] keyword.</span></span> <span data-ttu-id="d2014-106">Alcune implementazioni di DCE non consentono puntatori senza attributi.</span><span class="sxs-lookup"><span data-stu-id="d2014-106">Some DCE implementations do not allow unattributed pointers.</span></span> <span data-ttu-id="d2014-107">Se un puntatore non ha un attributo esplicito, il file IDL deve avere una specifica **\[ \_ predefinita \] del puntatore** , in modo che sia possibile impostare l'attributo del puntatore.</span><span class="sxs-lookup"><span data-stu-id="d2014-107">If a pointer does not have an explicit attribute, the IDL file must have a **\[pointer\_default\]** specification so that the pointer attribute can be set.</span></span>

<span data-ttu-id="d2014-108">In modalità predefinita (Microsoft-Extensions) è possibile specificare l'attributo di un puntatore nel file IDL che importa il file IDL di definizione.</span><span class="sxs-lookup"><span data-stu-id="d2014-108">In default (Microsoft-extensions) mode, you can specify a pointer's attribute in the IDL file that imports the defining IDL file.</span></span> <span data-ttu-id="d2014-109">I puntatori definiti in un file IDL possono ereditare gli attributi specificati in altri file IDL.</span><span class="sxs-lookup"><span data-stu-id="d2014-109">Pointers defined in one IDL file can inherit attributes that are specified in other IDL files.</span></span> <span data-ttu-id="d2014-110">Inoltre, in modalità predefinita, i file IDL possono includere puntatori senza attributi.</span><span class="sxs-lookup"><span data-stu-id="d2014-110">Also, in default mode, IDL files can include unattributed pointers.</span></span> <span data-ttu-id="d2014-111">Se né la base né i file IDL importati specificano un attributo puntatore o un **\[ puntatore \_ predefinito \]**, i puntatori senza attributi vengono interpretati come puntatori univoci.</span><span class="sxs-lookup"><span data-stu-id="d2014-111">If neither the base nor the imported IDL files specify a pointer attribute or **\[pointer\_default\]**, unattributed pointers are interpreted as unique pointers.</span></span>

<span data-ttu-id="d2014-112">Il compilatore MIDL assegna gli attributi del puntatore ai puntatori usando le seguenti regole di priorità (1 è il più alto).</span><span class="sxs-lookup"><span data-stu-id="d2014-112">The MIDL compiler assigns pointer attributes to pointers using the following priority rules (1 is highest).</span></span>



| <span data-ttu-id="d2014-113">Priorità</span><span class="sxs-lookup"><span data-stu-id="d2014-113">Priority</span></span> | <span data-ttu-id="d2014-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2014-114">Description</span></span>                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2014-115">1</span><span class="sxs-lookup"><span data-stu-id="d2014-115">1</span></span>        | <span data-ttu-id="d2014-116">Gli attributi di puntatore espliciti vengono applicati al puntatore nella definizione o usano il sito.</span><span class="sxs-lookup"><span data-stu-id="d2014-116">Explicit pointer attributes are applied to the pointer at the definition or use site.</span></span>                                      |
| <span data-ttu-id="d2014-117">2</span><span class="sxs-lookup"><span data-stu-id="d2014-117">2</span></span>        | <span data-ttu-id="d2014-118">Il valore predefinito è l'attributo **\[ \_ predefinito \] del puntatore** nel file IDL che definisce il tipo.</span><span class="sxs-lookup"><span data-stu-id="d2014-118">The default is the **\[pointer\_default\]** attribute in the IDL file that defines the type.</span></span>                               |
| <span data-ttu-id="d2014-119">3</span><span class="sxs-lookup"><span data-stu-id="d2014-119">3</span></span>        | <span data-ttu-id="d2014-120">Il valore predefinito è l'attributo **\[ \_ predefinito \] del puntatore** nel file IDL che importa il tipo.</span><span class="sxs-lookup"><span data-stu-id="d2014-120">The default is the **\[pointer\_default\]** attribute in the IDL file that imports the type.</span></span>                               |
| <span data-ttu-id="d2014-121">4</span><span class="sxs-lookup"><span data-stu-id="d2014-121">4</span></span>        | <span data-ttu-id="d2014-122">Il valore predefinito è \[ [ptr](/windows/desktop/Midl/ptr) \] in modalità di compatibilità DCE o \[ [univoco](/windows/desktop/Midl/unique) \] in modalità estensioni Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2014-122">The default is \[ [ptr](/windows/desktop/Midl/ptr)\] in DCE-compatibility mode, or \[ [unique](/windows/desktop/Midl/unique)\] in Microsoft-extensions mode.</span></span> |



 

 

 