---
description: Definisce il testo o CDATA che deve essere riutilizzato dall'elemento include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: elemento macro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994328"
---
# <a name="macro-element"></a><span data-ttu-id="46682-103">elemento macro</span><span class="sxs-lookup"><span data-stu-id="46682-103">macro element</span></span>

<span data-ttu-id="46682-104">Definisce il testo o CDATA che deve essere riutilizzato [**dall'elemento include.**](include.md)</span><span class="sxs-lookup"><span data-stu-id="46682-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="46682-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="46682-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="46682-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="46682-106">Attributes</span></span>



| <span data-ttu-id="46682-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="46682-107">Attribute</span></span>           | <span data-ttu-id="46682-108">Type</span><span class="sxs-lookup"><span data-stu-id="46682-108">Type</span></span>                         | <span data-ttu-id="46682-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="46682-109">Required</span></span>       | <span data-ttu-id="46682-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46682-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="46682-111">**nome**</span><span class="sxs-lookup"><span data-stu-id="46682-111">**name**</span></span><br/> | <span data-ttu-id="46682-112">stringa di \_ caratteri</span><span class="sxs-lookup"><span data-stu-id="46682-112">character\_string</span></span><br/> | <span data-ttu-id="46682-113">Sì</span><span class="sxs-lookup"><span data-stu-id="46682-113">Yes</span></span><br/> | <span data-ttu-id="46682-114">Nome della macro.</span><span class="sxs-lookup"><span data-stu-id="46682-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="46682-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="46682-115">Child elements</span></span>

<span data-ttu-id="46682-116">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="46682-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="46682-117">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="46682-117">Parent elements</span></span>



| <span data-ttu-id="46682-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="46682-118">Element</span></span>                                     | <span data-ttu-id="46682-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46682-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="46682-120">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="46682-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="46682-121">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="46682-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="46682-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="46682-122">Remarks</span></span>

<span data-ttu-id="46682-123">WsdCodeGen definisce una macro denominata **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="46682-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="46682-124">Quando questa macro è inclusa, il codice generato contiene un blocco di commenti ad alta visibilità che indica agli sviluppatori di non modificare il codice generato.</span><span class="sxs-lookup"><span data-stu-id="46682-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="46682-125">Il codice XML seguente illustra come includere la macro **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="46682-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="46682-126">Questo codice XML può essere aggiunto a un file di configurazione XML per WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="46682-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="46682-127">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="46682-127">Element information</span></span>



| <span data-ttu-id="46682-128">Label</span><span class="sxs-lookup"><span data-stu-id="46682-128">Label</span></span> | <span data-ttu-id="46682-129">Valore</span><span class="sxs-lookup"><span data-stu-id="46682-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="46682-130">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46682-130">Minimum supported system</span></span><br/> | <span data-ttu-id="46682-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46682-131">Windows Vista</span></span> |
| <span data-ttu-id="46682-132">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="46682-132">Can be empty</span></span>                        | <span data-ttu-id="46682-133">Sì</span><span class="sxs-lookup"><span data-stu-id="46682-133">Yes</span></span>           |



 

 




