---
description: Definisce il testo o CDATA da riutilizzare nell'elemento include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: elemento macro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231814"
---
# <a name="macro-element"></a><span data-ttu-id="01dc9-103">elemento macro</span><span class="sxs-lookup"><span data-stu-id="01dc9-103">macro element</span></span>

<span data-ttu-id="01dc9-104">Definisce il testo o CDATA da riutilizzare nell'elemento [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="01dc9-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="01dc9-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="01dc9-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="01dc9-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="01dc9-106">Attributes</span></span>



| <span data-ttu-id="01dc9-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="01dc9-107">Attribute</span></span>           | <span data-ttu-id="01dc9-108">Type</span><span class="sxs-lookup"><span data-stu-id="01dc9-108">Type</span></span>                         | <span data-ttu-id="01dc9-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="01dc9-109">Required</span></span>       | <span data-ttu-id="01dc9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01dc9-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="01dc9-111">**nome**</span><span class="sxs-lookup"><span data-stu-id="01dc9-111">**name**</span></span><br/> | <span data-ttu-id="01dc9-112">stringa di caratteri \_</span><span class="sxs-lookup"><span data-stu-id="01dc9-112">character\_string</span></span><br/> | <span data-ttu-id="01dc9-113">Sì</span><span class="sxs-lookup"><span data-stu-id="01dc9-113">Yes</span></span><br/> | <span data-ttu-id="01dc9-114">Nome della macro.</span><span class="sxs-lookup"><span data-stu-id="01dc9-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="01dc9-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="01dc9-115">Child elements</span></span>

<span data-ttu-id="01dc9-116">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="01dc9-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="01dc9-117">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="01dc9-117">Parent elements</span></span>



| <span data-ttu-id="01dc9-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="01dc9-118">Element</span></span>                                     | <span data-ttu-id="01dc9-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01dc9-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="01dc9-120">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="01dc9-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="01dc9-121">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="01dc9-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="01dc9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="01dc9-122">Remarks</span></span>

<span data-ttu-id="01dc9-123">WsdCodeGen definisce una macro denominata **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="01dc9-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="01dc9-124">Quando questa macro è inclusa, il codice generato contiene un blocco di commento con visibilità elevata che indica agli sviluppatori di non modificare il codice generato.</span><span class="sxs-lookup"><span data-stu-id="01dc9-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="01dc9-125">Nel codice XML seguente viene illustrato come includere la macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="01dc9-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="01dc9-126">Questo XML può essere aggiunto a un file di configurazione XML per WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="01dc9-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="01dc9-127">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="01dc9-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="01dc9-128">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01dc9-128">Minimum supported system</span></span><br/> | <span data-ttu-id="01dc9-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01dc9-129">Windows Vista</span></span> |
| <span data-ttu-id="01dc9-130">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="01dc9-130">Can be empty</span></span>                        | <span data-ttu-id="01dc9-131">Sì</span><span class="sxs-lookup"><span data-stu-id="01dc9-131">Yes</span></span>           |



 

 




