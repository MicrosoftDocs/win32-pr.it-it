---
description: Include il contenuto di una macro o di un file nell'output generato.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995778"
---
# <a name="include-element"></a><span data-ttu-id="90c04-103">include - elemento</span><span class="sxs-lookup"><span data-stu-id="90c04-103">include element</span></span>

<span data-ttu-id="90c04-104">Include il contenuto di una macro o di un file nell'output generato.</span><span class="sxs-lookup"><span data-stu-id="90c04-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="90c04-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="90c04-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="90c04-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="90c04-106">Attributes</span></span>



| <span data-ttu-id="90c04-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="90c04-107">Attribute</span></span>            | <span data-ttu-id="90c04-108">Type</span><span class="sxs-lookup"><span data-stu-id="90c04-108">Type</span></span>                         | <span data-ttu-id="90c04-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="90c04-109">Required</span></span>      | <span data-ttu-id="90c04-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90c04-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="90c04-111">**file**</span><span class="sxs-lookup"><span data-stu-id="90c04-111">**file**</span></span><br/>  | <span data-ttu-id="90c04-112">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="90c04-112">character\_string</span></span><br/> | <span data-ttu-id="90c04-113">No</span><span class="sxs-lookup"><span data-stu-id="90c04-113">No</span></span><br/> | <span data-ttu-id="90c04-114">Percorso del file da includere.</span><span class="sxs-lookup"><span data-stu-id="90c04-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="90c04-115">**Macro**</span><span class="sxs-lookup"><span data-stu-id="90c04-115">**macro**</span></span><br/> | <span data-ttu-id="90c04-116">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="90c04-116">character\_string</span></span><br/> | <span data-ttu-id="90c04-117">No</span><span class="sxs-lookup"><span data-stu-id="90c04-117">No</span></span><br/> | <span data-ttu-id="90c04-118">Nome della macro da includere.</span><span class="sxs-lookup"><span data-stu-id="90c04-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="90c04-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="90c04-119">Child elements</span></span>

<span data-ttu-id="90c04-120">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="90c04-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="90c04-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="90c04-121">Parent elements</span></span>



| <span data-ttu-id="90c04-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="90c04-122">Element</span></span>                         | <span data-ttu-id="90c04-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90c04-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90c04-124">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="90c04-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="90c04-125">Indica al generatore di codice di generare un file e specifica il nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="90c04-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="90c04-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="90c04-126">Remarks</span></span>

<span data-ttu-id="90c04-127">È necessario **specificare l'attributo macro** **o l'attributo** file.</span><span class="sxs-lookup"><span data-stu-id="90c04-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="90c04-128">Non specificare entrambi gli attributi.</span><span class="sxs-lookup"><span data-stu-id="90c04-128">Do not specify both attributes.</span></span>

<span data-ttu-id="90c04-129">WsdCodeGen definisce una macro denominata **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="90c04-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="90c04-130">Quando questa macro è inclusa, il codice generato contiene un blocco di commenti ad alta visibilità che indica agli sviluppatori di non modificare il codice generato.</span><span class="sxs-lookup"><span data-stu-id="90c04-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="90c04-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="90c04-131">Examples</span></span>

<span data-ttu-id="90c04-132">Nel codice XML seguente viene illustrato come includere la macro **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="90c04-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="90c04-133">Questo codice XML può essere aggiunto a un file di configurazione XML per WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="90c04-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="90c04-134">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="90c04-134">Element information</span></span>



| <span data-ttu-id="90c04-135">Label</span><span class="sxs-lookup"><span data-stu-id="90c04-135">Label</span></span> | <span data-ttu-id="90c04-136">Valore</span><span class="sxs-lookup"><span data-stu-id="90c04-136">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="90c04-137">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90c04-137">Minimum supported system</span></span><br/> | <span data-ttu-id="90c04-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90c04-138">Windows Vista</span></span> |
| <span data-ttu-id="90c04-139">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="90c04-139">Can be empty</span></span>                        | <span data-ttu-id="90c04-140">Sì</span><span class="sxs-lookup"><span data-stu-id="90c04-140">Yes</span></span>           |



 

 




