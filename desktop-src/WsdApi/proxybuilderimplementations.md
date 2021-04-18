---
description: Genera funzioni per la creazione di proxy tipizzati.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315988"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="d312a-103">elemento proxyBuilderImplementations</span><span class="sxs-lookup"><span data-stu-id="d312a-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="d312a-104">Genera funzioni per la creazione di proxy tipizzati.</span><span class="sxs-lookup"><span data-stu-id="d312a-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="d312a-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d312a-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="d312a-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="d312a-106">Attributes</span></span>

<span data-ttu-id="d312a-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="d312a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d312a-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d312a-108">Child elements</span></span>



| <span data-ttu-id="d312a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="d312a-109">Element</span></span>                                     | <span data-ttu-id="d312a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d312a-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d312a-111">**codeName**</span><span class="sxs-lookup"><span data-stu-id="d312a-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="d312a-112">Nome da utilizzare per il tipo di porta nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="d312a-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="d312a-113">Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="d312a-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="d312a-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="d312a-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="d312a-115">Tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="d312a-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="d312a-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="d312a-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="d312a-117">Nome della classe da generare dalla funzione del generatore proxy.</span><span class="sxs-lookup"><span data-stu-id="d312a-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="d312a-118">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d312a-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="d312a-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d312a-119">Parent elements</span></span>



| <span data-ttu-id="d312a-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="d312a-120">Element</span></span>                         | <span data-ttu-id="d312a-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d312a-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d312a-122">**file**</span><span class="sxs-lookup"><span data-stu-id="d312a-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="d312a-123">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="d312a-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="d312a-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d312a-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="d312a-125">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d312a-125">Minimum supported system</span></span><br/> | <span data-ttu-id="d312a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d312a-126">Windows Vista</span></span> |
| <span data-ttu-id="d312a-127">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="d312a-127">Can be empty</span></span>                        | <span data-ttu-id="d312a-128">No</span><span class="sxs-lookup"><span data-stu-id="d312a-128">No</span></span>            |



 

 




