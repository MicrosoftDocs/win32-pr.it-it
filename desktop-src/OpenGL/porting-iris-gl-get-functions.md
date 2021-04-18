---
title: Porting delle funzioni Get di IRIS GL
description: IRIS GL \ 0034; Get \ 0034; le funzioni hanno il formato seguente
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Porting di IRIS GL, funzioni Get
- porting da IRIS GL, Get Functions
- porting in OpenGL da IRIS GL, funzioni Get
- Porting OpenGL da IRIS GL, funzioni Get
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298544"
---
# <a name="porting-iris-gl-get-functions"></a><span data-ttu-id="b4782-107">Porting delle funzioni Get di IRIS GL</span><span class="sxs-lookup"><span data-stu-id="b4782-107">Porting IRIS GL Get Functions</span></span>

<span data-ttu-id="b4782-108">Le funzioni "Get" di IRIS GL hanno il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="b4782-108">IRIS GL "get" functions take the following form:</span></span>

``` syntax
int getthing();
```

<span data-ttu-id="b4782-109">e</span><span class="sxs-lookup"><span data-stu-id="b4782-109">and</span></span>

``` syntax
int getthings( int *a, int *b);
```

<span data-ttu-id="b4782-110">Il codice di IRIS GL include probabilmente le chiamate di funzione Get che hanno un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="b4782-110">Your IRIS GL code probably includes get function calls that look something like:</span></span>

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

<span data-ttu-id="b4782-111">In OpenGL si usa uno dei quattro tipi seguenti di funzioni [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) al posto delle funzioni Get di Iris GL equivalenti:</span><span class="sxs-lookup"><span data-stu-id="b4782-111">In OpenGL you use one of the following four types of [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) functions in place of equivalent IRIS GL get functions:</span></span>

-   <span data-ttu-id="b4782-112">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="b4782-112">**glGetBooleanv**</span></span>
-   <span data-ttu-id="b4782-113">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="b4782-113">**glGetIntegerv**</span></span>
-   <span data-ttu-id="b4782-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="b4782-114">**glGetFloatv**</span></span>
-   <span data-ttu-id="b4782-115">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="b4782-115">**glGetDoublev**</span></span>

<span data-ttu-id="b4782-116">Le funzioni presentano la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="b4782-116">The functions have the following syntax:</span></span>

``` syntax
glGet<Datatype>v( value, *data );
```

<span data-ttu-id="b4782-117">dove *value* è di tipo **GLEnum** e i dati sono di tipo **GLdatatype**.</span><span class="sxs-lookup"><span data-stu-id="b4782-117">where *value* is of type **GLenum** and data is of type **GLdatatype**.</span></span> <span data-ttu-id="b4782-118">Quando si chiama **glGet** e viene restituito un tipo diverso dal tipo previsto, il tipo viene convertito in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="b4782-118">When you call **glGet** and it returns a type different from the type expected, the type is converted appropriately.</span></span> <span data-ttu-id="b4782-119">Per un elenco completo dei parametri **glGet** , vedere [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="b4782-119">For a complete list of **glGet** parameters, see [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span></span>

 

 




