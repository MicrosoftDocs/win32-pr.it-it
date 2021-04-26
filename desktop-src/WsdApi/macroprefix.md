---
description: Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi .
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998748"
---
# <a name="macroprefix-element"></a><span data-ttu-id="8cd36-103">macroPrefix - elemento</span><span class="sxs-lookup"><span data-stu-id="8cd36-103">macroPrefix element</span></span>

<span data-ttu-id="8cd36-104">Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi .</span><span class="sxs-lookup"><span data-stu-id="8cd36-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="8cd36-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8cd36-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="8cd36-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="8cd36-106">Attributes</span></span>

<span data-ttu-id="8cd36-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="8cd36-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8cd36-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8cd36-108">Child elements</span></span>

<span data-ttu-id="8cd36-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="8cd36-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8cd36-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8cd36-110">Parent elements</span></span>



| <span data-ttu-id="8cd36-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="8cd36-111">Element</span></span>                                   | <span data-ttu-id="8cd36-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cd36-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="8cd36-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8cd36-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="8cd36-114">Spazio dei nomi da utilizzare per la generazione di codice.</span><span class="sxs-lookup"><span data-stu-id="8cd36-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8cd36-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cd36-115">Remarks</span></span>

<span data-ttu-id="8cd36-116">Questo elemento esegue l'override del prefisso URI predefinito usato per le macro generate.</span><span class="sxs-lookup"><span data-stu-id="8cd36-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="8cd36-117">Ad esempio, se il prefisso della macro è "AV " e il nome è "Tuner", la macro generata per il nome completo sarà \_ "AV \_ Tuner".</span><span class="sxs-lookup"><span data-stu-id="8cd36-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="8cd36-118">Per impostazione predefinita, il codice generato crea un prefisso di macro preferito dall'URI.</span><span class="sxs-lookup"><span data-stu-id="8cd36-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="8cd36-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8cd36-119">Element information</span></span>



| <span data-ttu-id="8cd36-120">Label</span><span class="sxs-lookup"><span data-stu-id="8cd36-120">Label</span></span> | <span data-ttu-id="8cd36-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8cd36-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8cd36-122">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cd36-122">Minimum supported system</span></span><br/> | <span data-ttu-id="8cd36-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cd36-123">Windows Vista</span></span> |
| <span data-ttu-id="8cd36-124">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="8cd36-124">Can be empty</span></span>                        | <span data-ttu-id="8cd36-125">Sì</span><span class="sxs-lookup"><span data-stu-id="8cd36-125">Yes</span></span>           |



 

 




