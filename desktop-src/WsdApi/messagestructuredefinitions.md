---
description: Genera definizioni della struttura C per i tipi di messaggio.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: elemento messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310291"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="15f3e-103">elemento messageStructureDefinitions</span><span class="sxs-lookup"><span data-stu-id="15f3e-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="15f3e-104">Genera definizioni della struttura C per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="15f3e-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="15f3e-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="15f3e-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="15f3e-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="15f3e-106">Attributes</span></span>

<span data-ttu-id="15f3e-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="15f3e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="15f3e-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="15f3e-108">Child elements</span></span>



| <span data-ttu-id="15f3e-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="15f3e-109">Element</span></span>                                   | <span data-ttu-id="15f3e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15f3e-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="15f3e-111">**operazione**</span><span class="sxs-lookup"><span data-stu-id="15f3e-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="15f3e-112">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="15f3e-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="15f3e-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="15f3e-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="15f3e-114">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="15f3e-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="15f3e-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="15f3e-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="15f3e-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="15f3e-116">Parent elements</span></span>



| <span data-ttu-id="15f3e-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="15f3e-117">Element</span></span>                         | <span data-ttu-id="15f3e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15f3e-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="15f3e-119">**file**</span><span class="sxs-lookup"><span data-stu-id="15f3e-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="15f3e-120">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="15f3e-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="15f3e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="15f3e-121">Remarks</span></span>

<span data-ttu-id="15f3e-122">Il codice stub e il proxy generato fanno riferimento a strutture di messaggio.</span><span class="sxs-lookup"><span data-stu-id="15f3e-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="15f3e-123">Questo elemento viene utilizzato per generare file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="15f3e-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="15f3e-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="15f3e-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="15f3e-125">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15f3e-125">Minimum supported system</span></span><br/> | <span data-ttu-id="15f3e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15f3e-126">Windows Vista</span></span> |
| <span data-ttu-id="15f3e-127">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="15f3e-127">Can be empty</span></span>                        | <span data-ttu-id="15f3e-128">Sì</span><span class="sxs-lookup"><span data-stu-id="15f3e-128">Yes</span></span>           |



 

 




