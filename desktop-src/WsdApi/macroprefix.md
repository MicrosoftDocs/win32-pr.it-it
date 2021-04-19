---
description: Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310292"
---
# <a name="macroprefix-element"></a><span data-ttu-id="091d6-103">elemento macroPrefix</span><span class="sxs-lookup"><span data-stu-id="091d6-103">macroPrefix element</span></span>

<span data-ttu-id="091d6-104">Definisce il prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="091d6-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="091d6-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="091d6-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="091d6-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="091d6-106">Attributes</span></span>

<span data-ttu-id="091d6-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="091d6-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="091d6-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="091d6-108">Child elements</span></span>

<span data-ttu-id="091d6-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="091d6-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="091d6-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="091d6-110">Parent elements</span></span>



| <span data-ttu-id="091d6-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="091d6-111">Element</span></span>                                   | <span data-ttu-id="091d6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="091d6-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="091d6-113">**nameSpace**</span><span class="sxs-lookup"><span data-stu-id="091d6-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="091d6-114">Spazio dei nomi da utilizzare per la generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="091d6-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="091d6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="091d6-115">Remarks</span></span>

<span data-ttu-id="091d6-116">Questo elemento sostituisce il prefisso URI predefinito usato per le macro generate.</span><span class="sxs-lookup"><span data-stu-id="091d6-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="091d6-117">Se, ad esempio, il prefisso della macro è "AV \_ " e il nome è "Tuner", la macro generata per il nome completo sarà " \_ Tuner AV".</span><span class="sxs-lookup"><span data-stu-id="091d6-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="091d6-118">Per impostazione predefinita, il codice generato crea un prefisso di macro preferito dall'URI.</span><span class="sxs-lookup"><span data-stu-id="091d6-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="091d6-119">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="091d6-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="091d6-120">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="091d6-120">Minimum supported system</span></span><br/> | <span data-ttu-id="091d6-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="091d6-121">Windows Vista</span></span> |
| <span data-ttu-id="091d6-122">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="091d6-122">Can be empty</span></span>                        | <span data-ttu-id="091d6-123">Sì</span><span class="sxs-lookup"><span data-stu-id="091d6-123">Yes</span></span>           |



 

 




