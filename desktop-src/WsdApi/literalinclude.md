---
description: Inserisce un'istruzione di inclusione C o IDL nel codice generato.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313151"
---
# <a name="literalinclude-element"></a><span data-ttu-id="b242d-103">elemento literalInclude</span><span class="sxs-lookup"><span data-stu-id="b242d-103">literalInclude element</span></span>

<span data-ttu-id="b242d-104">Inserisce un'istruzione di inclusione C o IDL nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="b242d-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="b242d-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b242d-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="b242d-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="b242d-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b242d-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="b242d-107">Attribute</span></span></th>
<th><span data-ttu-id="b242d-108">Type</span><span class="sxs-lookup"><span data-stu-id="b242d-108">Type</span></span></th>
<th><span data-ttu-id="b242d-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b242d-109">Required</span></span></th>
<th><span data-ttu-id="b242d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b242d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b242d-111"><strong>Lingua</strong></span><span class="sxs-lookup"><span data-stu-id="b242d-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="b242d-112">stringa lingua</span><span class="sxs-lookup"><span data-stu-id="b242d-112">language string</span></span><br/></td>
<td><span data-ttu-id="b242d-113">No</span><span class="sxs-lookup"><span data-stu-id="b242d-113">No</span></span><br/></td>
<td><span data-ttu-id="b242d-114">Tipo di file di intestazione da includere.</span><span class="sxs-lookup"><span data-stu-id="b242d-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="b242d-115">
<dt><strong>C</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b242d-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="b242d-116">Includere un file di intestazione C.</span><span class="sxs-lookup"><span data-stu-id="b242d-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="b242d-117"><dt><strong>IDL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b242d-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="b242d-118">Includere un file IDL.</span><span class="sxs-lookup"><span data-stu-id="b242d-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b242d-119"><strong>Locale</strong></span><span class="sxs-lookup"><span data-stu-id="b242d-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="b242d-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="b242d-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="b242d-121">No</span><span class="sxs-lookup"><span data-stu-id="b242d-121">No</span></span><br/></td>
<td><span data-ttu-id="b242d-122">Questo attributo viene utilizzato solo quando la <strong>lingua</strong> è impostata su &quot; C &quot; .</span><span class="sxs-lookup"><span data-stu-id="b242d-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="b242d-123">
<dt><strong>True</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b242d-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="b242d-124">Cerca l'intestazione denominata nella directory corrente prima di cercare le directory di sistema.</span><span class="sxs-lookup"><span data-stu-id="b242d-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="b242d-125"><dt><strong>False</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b242d-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="b242d-126">Cerca solo le directory di sistema per l'intestazione denominata.</span><span class="sxs-lookup"><span data-stu-id="b242d-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b242d-127">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b242d-127">Child elements</span></span>

<span data-ttu-id="b242d-128">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b242d-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b242d-129">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b242d-129">Parent elements</span></span>



| <span data-ttu-id="b242d-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="b242d-130">Element</span></span>                         | <span data-ttu-id="b242d-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b242d-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b242d-132">**file**</span><span class="sxs-lookup"><span data-stu-id="b242d-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b242d-133">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="b242d-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b242d-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="b242d-134">Remarks</span></span>

<span data-ttu-id="b242d-135">Negli esempi seguenti viene illustrato il codice generato da elementi **literalInclude** diversi.</span><span class="sxs-lookup"><span data-stu-id="b242d-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="b242d-136">Esempio 1: generazione di un'istruzione di inclusione C</span><span class="sxs-lookup"><span data-stu-id="b242d-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="b242d-137">XML di input:</span><span class="sxs-lookup"><span data-stu-id="b242d-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="b242d-138">Codice di output:</span><span class="sxs-lookup"><span data-stu-id="b242d-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="b242d-139">Esempio 2: generazione di un'istruzione di inclusione C</span><span class="sxs-lookup"><span data-stu-id="b242d-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="b242d-140">XML di input:</span><span class="sxs-lookup"><span data-stu-id="b242d-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="b242d-141">Codice di output:</span><span class="sxs-lookup"><span data-stu-id="b242d-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="b242d-142">Esempio 3: generazione di un'istruzione Import IDL</span><span class="sxs-lookup"><span data-stu-id="b242d-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="b242d-143">XML di input:</span><span class="sxs-lookup"><span data-stu-id="b242d-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="b242d-144">Codice di output:</span><span class="sxs-lookup"><span data-stu-id="b242d-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="b242d-145">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b242d-145">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b242d-146">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b242d-146">Minimum supported system</span></span><br/> | <span data-ttu-id="b242d-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b242d-147">Windows Vista</span></span> |
| <span data-ttu-id="b242d-148">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="b242d-148">Can be empty</span></span>                        | <span data-ttu-id="b242d-149">Sì</span><span class="sxs-lookup"><span data-stu-id="b242d-149">Yes</span></span>           |



 

 




