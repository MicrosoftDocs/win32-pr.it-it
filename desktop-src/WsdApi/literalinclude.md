---
description: Inserisce un'istruzione di inclusione C o IDL nel codice generato.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: Elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995128"
---
# <a name="literalinclude-element"></a><span data-ttu-id="27ef7-103">Elemento literalInclude</span><span class="sxs-lookup"><span data-stu-id="27ef7-103">literalInclude element</span></span>

<span data-ttu-id="27ef7-104">Inserisce un'istruzione di inclusione C o IDL nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="27ef7-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="27ef7-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="27ef7-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="27ef7-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="27ef7-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27ef7-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="27ef7-107">Attribute</span></span></th>
<th><span data-ttu-id="27ef7-108">Type</span><span class="sxs-lookup"><span data-stu-id="27ef7-108">Type</span></span></th>
<th><span data-ttu-id="27ef7-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="27ef7-109">Required</span></span></th>
<th><span data-ttu-id="27ef7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27ef7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27ef7-111"><strong>Lingua</strong></span><span class="sxs-lookup"><span data-stu-id="27ef7-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="27ef7-112">stringa del linguaggio</span><span class="sxs-lookup"><span data-stu-id="27ef7-112">language string</span></span><br/></td>
<td><span data-ttu-id="27ef7-113">No</span><span class="sxs-lookup"><span data-stu-id="27ef7-113">No</span></span><br/></td>
<td><span data-ttu-id="27ef7-114">Tipo di file di intestazione da includere.</span><span class="sxs-lookup"><span data-stu-id="27ef7-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="27ef7-115">
<dt><strong>C</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27ef7-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="27ef7-116">Includere un file di intestazione C.</span><span class="sxs-lookup"><span data-stu-id="27ef7-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="27ef7-117"><dt><strong>Idl</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27ef7-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="27ef7-118">Includere un file IDL.</span><span class="sxs-lookup"><span data-stu-id="27ef7-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27ef7-119"><strong>Locale</strong></span><span class="sxs-lookup"><span data-stu-id="27ef7-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="27ef7-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="27ef7-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="27ef7-121">No</span><span class="sxs-lookup"><span data-stu-id="27ef7-121">No</span></span><br/></td>
<td><span data-ttu-id="27ef7-122">Questo attributo viene usato solo quando <strong>Language</strong> è impostato su &quot; C &quot; .</span><span class="sxs-lookup"><span data-stu-id="27ef7-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="27ef7-123">
<dt><strong>Vero</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27ef7-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="27ef7-124">Cerca l'intestazione denominata nella directory corrente prima di cercare le directory di sistema.</span><span class="sxs-lookup"><span data-stu-id="27ef7-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="27ef7-125"><dt><strong>False</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27ef7-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="27ef7-126">Cercare solo le directory di sistema per l'intestazione denominata.</span><span class="sxs-lookup"><span data-stu-id="27ef7-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="27ef7-127">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="27ef7-127">Child elements</span></span>

<span data-ttu-id="27ef7-128">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="27ef7-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="27ef7-129">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="27ef7-129">Parent elements</span></span>



| <span data-ttu-id="27ef7-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="27ef7-130">Element</span></span>                         | <span data-ttu-id="27ef7-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27ef7-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="27ef7-132">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="27ef7-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="27ef7-133">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="27ef7-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="27ef7-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="27ef7-134">Remarks</span></span>

<span data-ttu-id="27ef7-135">Gli esempi seguenti illustrano il codice generato da **diversi elementi literalInclude.**</span><span class="sxs-lookup"><span data-stu-id="27ef7-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="27ef7-136">Esempio 1 - Generazione di un'istruzione C include</span><span class="sxs-lookup"><span data-stu-id="27ef7-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="27ef7-137">XML di input:</span><span class="sxs-lookup"><span data-stu-id="27ef7-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="27ef7-138">Codice di output:</span><span class="sxs-lookup"><span data-stu-id="27ef7-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="27ef7-139">Esempio 2 - Generazione di un'istruzione C include</span><span class="sxs-lookup"><span data-stu-id="27ef7-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="27ef7-140">XML di input:</span><span class="sxs-lookup"><span data-stu-id="27ef7-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="27ef7-141">Codice di output:</span><span class="sxs-lookup"><span data-stu-id="27ef7-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="27ef7-142">Esempio 3 - Generazione di un'istruzione IDL import</span><span class="sxs-lookup"><span data-stu-id="27ef7-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="27ef7-143">XML di input:</span><span class="sxs-lookup"><span data-stu-id="27ef7-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="27ef7-144">Codice di output:</span><span class="sxs-lookup"><span data-stu-id="27ef7-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="27ef7-145">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="27ef7-145">Element information</span></span>



| <span data-ttu-id="27ef7-146">Label</span><span class="sxs-lookup"><span data-stu-id="27ef7-146">Label</span></span> | <span data-ttu-id="27ef7-147">Valore</span><span class="sxs-lookup"><span data-stu-id="27ef7-147">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="27ef7-148">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27ef7-148">Minimum supported system</span></span><br/> | <span data-ttu-id="27ef7-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27ef7-149">Windows Vista</span></span> |
| <span data-ttu-id="27ef7-150">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="27ef7-150">Can be empty</span></span>                        | <span data-ttu-id="27ef7-151">Sì</span><span class="sxs-lookup"><span data-stu-id="27ef7-151">Yes</span></span>           |



 

 




