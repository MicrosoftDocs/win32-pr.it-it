---
description: Genera funzioni per creare proxy tipiati.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: Elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996468"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="993ea-103">Elemento proxyBuilderImplementations</span><span class="sxs-lookup"><span data-stu-id="993ea-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="993ea-104">Genera funzioni per creare proxy tipiati.</span><span class="sxs-lookup"><span data-stu-id="993ea-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="993ea-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="993ea-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="993ea-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="993ea-106">Attributes</span></span>

<span data-ttu-id="993ea-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="993ea-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="993ea-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="993ea-108">Child elements</span></span>



| <span data-ttu-id="993ea-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="993ea-109">Element</span></span>                                     | <span data-ttu-id="993ea-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="993ea-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="993ea-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="993ea-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="993ea-112">Nome da utilizzare per il tipo di porta nel codice generato.</span><span class="sxs-lookup"><span data-stu-id="993ea-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="993ea-113">Per impostazione predefinita, il nome del codice viene generato dal nome completo del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="993ea-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="993ea-114">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="993ea-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="993ea-115">Tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="993ea-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="993ea-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="993ea-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="993ea-117">Nome della classe da generare dalla funzione del generatore di proxy.</span><span class="sxs-lookup"><span data-stu-id="993ea-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="993ea-118">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="993ea-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="993ea-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="993ea-119">Parent elements</span></span>



| <span data-ttu-id="993ea-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="993ea-120">Element</span></span>                         | <span data-ttu-id="993ea-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="993ea-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="993ea-122">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="993ea-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="993ea-123">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="993ea-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="993ea-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="993ea-124">Element information</span></span>



| <span data-ttu-id="993ea-125">Label</span><span class="sxs-lookup"><span data-stu-id="993ea-125">Label</span></span> | <span data-ttu-id="993ea-126">Valore</span><span class="sxs-lookup"><span data-stu-id="993ea-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="993ea-127">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="993ea-127">Minimum supported system</span></span><br/> | <span data-ttu-id="993ea-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="993ea-128">Windows Vista</span></span> |
| <span data-ttu-id="993ea-129">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="993ea-129">Can be empty</span></span>                        | <span data-ttu-id="993ea-130">No</span><span class="sxs-lookup"><span data-stu-id="993ea-130">No</span></span>            |



 

 




