---
description: Include il contenuto di una macro o di un file nell'output generato.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057951"
---
# <a name="include-element"></a><span data-ttu-id="f8acb-103">include - elemento</span><span class="sxs-lookup"><span data-stu-id="f8acb-103">include element</span></span>

<span data-ttu-id="f8acb-104">Include il contenuto di una macro o di un file nell'output generato.</span><span class="sxs-lookup"><span data-stu-id="f8acb-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="f8acb-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f8acb-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="f8acb-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="f8acb-106">Attributes</span></span>



| <span data-ttu-id="f8acb-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="f8acb-107">Attribute</span></span>            | <span data-ttu-id="f8acb-108">Type</span><span class="sxs-lookup"><span data-stu-id="f8acb-108">Type</span></span>                         | <span data-ttu-id="f8acb-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f8acb-109">Required</span></span>      | <span data-ttu-id="f8acb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8acb-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="f8acb-111">**file**</span><span class="sxs-lookup"><span data-stu-id="f8acb-111">**file**</span></span><br/>  | <span data-ttu-id="f8acb-112">stringa di caratteri \_</span><span class="sxs-lookup"><span data-stu-id="f8acb-112">character\_string</span></span><br/> | <span data-ttu-id="f8acb-113">No</span><span class="sxs-lookup"><span data-stu-id="f8acb-113">No</span></span><br/> | <span data-ttu-id="f8acb-114">Percorso del file da includere.</span><span class="sxs-lookup"><span data-stu-id="f8acb-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="f8acb-115">**macro**</span><span class="sxs-lookup"><span data-stu-id="f8acb-115">**macro**</span></span><br/> | <span data-ttu-id="f8acb-116">stringa di caratteri \_</span><span class="sxs-lookup"><span data-stu-id="f8acb-116">character\_string</span></span><br/> | <span data-ttu-id="f8acb-117">No</span><span class="sxs-lookup"><span data-stu-id="f8acb-117">No</span></span><br/> | <span data-ttu-id="f8acb-118">Nome della macro da includere.</span><span class="sxs-lookup"><span data-stu-id="f8acb-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="f8acb-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f8acb-119">Child elements</span></span>

<span data-ttu-id="f8acb-120">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="f8acb-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f8acb-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f8acb-121">Parent elements</span></span>



| <span data-ttu-id="f8acb-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="f8acb-122">Element</span></span>                         | <span data-ttu-id="f8acb-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8acb-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8acb-124">**file**</span><span class="sxs-lookup"><span data-stu-id="f8acb-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f8acb-125">Indica al generatore di codice di generare un file e di specificare il nome del file di output.</span><span class="sxs-lookup"><span data-stu-id="f8acb-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f8acb-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8acb-126">Remarks</span></span>

<span data-ttu-id="f8acb-127">È necessario specificare l'attributo **macro** o l'attributo **file** .</span><span class="sxs-lookup"><span data-stu-id="f8acb-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="f8acb-128">Non specificare entrambi gli attributi.</span><span class="sxs-lookup"><span data-stu-id="f8acb-128">Do not specify both attributes.</span></span>

<span data-ttu-id="f8acb-129">WsdCodeGen definisce una macro denominata **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="f8acb-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="f8acb-130">Quando questa macro è inclusa, il codice generato contiene un blocco di commento con visibilità elevata che indica agli sviluppatori di non modificare il codice generato.</span><span class="sxs-lookup"><span data-stu-id="f8acb-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="f8acb-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="f8acb-131">Examples</span></span>

<span data-ttu-id="f8acb-132">Nel codice XML seguente viene illustrato come includere la macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="f8acb-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="f8acb-133">Questo XML può essere aggiunto a un file di configurazione XML per WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="f8acb-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="f8acb-134">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f8acb-134">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f8acb-135">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8acb-135">Minimum supported system</span></span><br/> | <span data-ttu-id="f8acb-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8acb-136">Windows Vista</span></span> |
| <span data-ttu-id="f8acb-137">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="f8acb-137">Can be empty</span></span>                        | <span data-ttu-id="f8acb-138">Sì</span><span class="sxs-lookup"><span data-stu-id="f8acb-138">Yes</span></span>           |



 

 




