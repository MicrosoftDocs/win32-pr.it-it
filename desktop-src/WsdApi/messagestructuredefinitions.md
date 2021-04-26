---
description: Genera definizioni di struttura C per i tipi di messaggio.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: elemento messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a116658fc7ce7f985b7b717c7a7b4ce38be4637
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993668"
---
# <a name="messagestructuredefinitions-element"></a><span data-ttu-id="c8a75-103">elemento messageStructureDefinitions</span><span class="sxs-lookup"><span data-stu-id="c8a75-103">messageStructureDefinitions element</span></span>

<span data-ttu-id="c8a75-104">Genera definizioni di struttura C per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="c8a75-104">Generates C structure definitions for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="c8a75-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c8a75-105">Usage</span></span>

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="c8a75-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="c8a75-106">Attributes</span></span>

<span data-ttu-id="c8a75-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="c8a75-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c8a75-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c8a75-108">Child elements</span></span>



| <span data-ttu-id="c8a75-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c8a75-109">Element</span></span>                                   | <span data-ttu-id="c8a75-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8a75-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c8a75-111">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="c8a75-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="c8a75-112">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="c8a75-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="c8a75-113">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="c8a75-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="c8a75-114">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="c8a75-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="c8a75-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c8a75-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="c8a75-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="c8a75-116">Parent elements</span></span>



| <span data-ttu-id="c8a75-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="c8a75-117">Element</span></span>                         | <span data-ttu-id="c8a75-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8a75-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c8a75-119">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="c8a75-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c8a75-120">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="c8a75-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c8a75-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8a75-121">Remarks</span></span>

<span data-ttu-id="c8a75-122">Il proxy generato e il codice stub fanno riferimento alle strutture dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="c8a75-122">Message structures are referenced by generated proxy and stub code.</span></span> <span data-ttu-id="c8a75-123">Questo elemento viene usato per generare file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="c8a75-123">This element is used to generate include files.</span></span>

## <a name="element-information"></a><span data-ttu-id="c8a75-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c8a75-124">Element information</span></span>



| <span data-ttu-id="c8a75-125">Label</span><span class="sxs-lookup"><span data-stu-id="c8a75-125">Label</span></span> | <span data-ttu-id="c8a75-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c8a75-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c8a75-127">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8a75-127">Minimum supported system</span></span><br/> | <span data-ttu-id="c8a75-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8a75-128">Windows Vista</span></span> |
| <span data-ttu-id="c8a75-129">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="c8a75-129">Can be empty</span></span>                        | <span data-ttu-id="c8a75-130">Sì</span><span class="sxs-lookup"><span data-stu-id="c8a75-130">Yes</span></span>           |



 

 




