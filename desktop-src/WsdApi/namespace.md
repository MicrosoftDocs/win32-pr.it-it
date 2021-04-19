---
description: Descrive uno spazio dei nomi.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: Elemento nameSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2414919f699bb60c2cf1e48bc52030c36cf67a0
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380845"
---
# <a name="namespace-element"></a><span data-ttu-id="593be-103">Elemento nameSpace</span><span class="sxs-lookup"><span data-stu-id="593be-103">nameSpace element</span></span>

<span data-ttu-id="593be-104">Descrive uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="593be-104">Describes a namespace.</span></span> <span data-ttu-id="593be-105">Questo spazio dei nomi può essere usato per la generazione del codice o per la gestione \<wsdl:import> delle direttive .</span><span class="sxs-lookup"><span data-stu-id="593be-105">This namespace may be used for code generation or for handling \<wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="593be-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="593be-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="593be-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="593be-107">Attributes</span></span>



| <span data-ttu-id="593be-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="593be-108">Attribute</span></span>          | <span data-ttu-id="593be-109">Type</span><span class="sxs-lookup"><span data-stu-id="593be-109">Type</span></span>                         | <span data-ttu-id="593be-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="593be-110">Required</span></span>       | <span data-ttu-id="593be-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="593be-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="593be-112">**Uri**</span><span class="sxs-lookup"><span data-stu-id="593be-112">**uri**</span></span><br/> | <span data-ttu-id="593be-113">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="593be-113">character\_string</span></span><br/> | <span data-ttu-id="593be-114">Sì</span><span class="sxs-lookup"><span data-stu-id="593be-114">Yes</span></span><br/> | <span data-ttu-id="593be-115">URI univoco dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="593be-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="593be-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="593be-116">Child elements</span></span>



| <span data-ttu-id="593be-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="593be-117">Element</span></span>                                               | <span data-ttu-id="593be-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="593be-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="593be-119">**Codename**</span><span class="sxs-lookup"><span data-stu-id="593be-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="593be-120">Nome da utilizzare per identificare lo spazio dei nomi nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="593be-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="593be-121">**macroPrefix**</span><span class="sxs-lookup"><span data-stu-id="593be-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="593be-122">Prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi .</span><span class="sxs-lookup"><span data-stu-id="593be-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="593be-123">**Nome**</span><span class="sxs-lookup"><span data-stu-id="593be-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="593be-124">Nome completo nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="593be-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="593be-125">**preferredPrefix**</span><span class="sxs-lookup"><span data-stu-id="593be-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="593be-126">Prefisso a cui deve essere eseguito il mapping dello spazio dei nomi per rendere il codice XML più leggibile.</span><span class="sxs-lookup"><span data-stu-id="593be-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="593be-127">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="593be-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="593be-128">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="593be-128">Parent elements</span></span>



| <span data-ttu-id="593be-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="593be-129">Element</span></span>                                     | <span data-ttu-id="593be-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="593be-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="593be-131">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="593be-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="593be-132">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="593be-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="593be-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="593be-133">Remarks</span></span>

<span data-ttu-id="593be-134">Questo elemento può essere usato per fornire al generatore di codice informazioni aggiuntive sugli spazi dei nomi rilevati nei file WSDL e XSD o per introdurre nuovi spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="593be-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="593be-135">Gli spazi dei nomi implicati dalla reflection del tipo o specificati nei file WSDL e XSD vengono analizzati automaticamente dal generatore di codice e non devono essere definiti in modo esplicito nello script.</span><span class="sxs-lookup"><span data-stu-id="593be-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="593be-136">In alcuni casi, questo elemento può essere usato per aggiungere proprietà o nomi aggiuntivi a uno spazio dei nomi a cui fa riferimento la reflection del tipo o WSDL/XSD.</span><span class="sxs-lookup"><span data-stu-id="593be-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="593be-137">Il generatore di codice non considera questo tipo di conflitto.</span><span class="sxs-lookup"><span data-stu-id="593be-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="593be-138">Nel codice XML seguente viene illustrato un elemento nameSpace (con elementi figlio omessi per brevità).</span><span class="sxs-lookup"><span data-stu-id="593be-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="593be-139">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="593be-139">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="593be-140">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="593be-140">Minimum supported system</span></span><br/> | <span data-ttu-id="593be-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="593be-141">Windows Vista</span></span> |
| <span data-ttu-id="593be-142">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="593be-142">Can be empty</span></span>                        | <span data-ttu-id="593be-143">Sì</span><span class="sxs-lookup"><span data-stu-id="593be-143">Yes</span></span>           |



 

 




