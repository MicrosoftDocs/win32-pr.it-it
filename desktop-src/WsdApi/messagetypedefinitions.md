---
description: Genera costanti C per XML Schema tabelle per i tipi di messaggio.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f86043cc28b527778c91772ad731d3a271921f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226921"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="18a82-103">elemento messageTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="18a82-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="18a82-104">Genera costanti C per XML Schema tabelle per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="18a82-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="18a82-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="18a82-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="18a82-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="18a82-106">Attributes</span></span>

<span data-ttu-id="18a82-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="18a82-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="18a82-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="18a82-108">Child elements</span></span>



| <span data-ttu-id="18a82-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="18a82-109">Element</span></span>                                   | <span data-ttu-id="18a82-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18a82-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="18a82-111">**operazione**</span><span class="sxs-lookup"><span data-stu-id="18a82-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="18a82-112">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="18a82-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="18a82-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="18a82-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="18a82-114">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="18a82-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="18a82-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="18a82-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="18a82-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="18a82-116">Parent elements</span></span>



| <span data-ttu-id="18a82-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="18a82-117">Element</span></span>                         | <span data-ttu-id="18a82-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18a82-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="18a82-119">**file**</span><span class="sxs-lookup"><span data-stu-id="18a82-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="18a82-120">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="18a82-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="18a82-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="18a82-121">Remarks</span></span>

<span data-ttu-id="18a82-122">Questo elemento viene in genere utilizzato nei file di origine C per fornire le tabelle dello schema dichiarate da [**messageTypeDeclarations**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="18a82-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="18a82-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="18a82-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="18a82-124">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18a82-124">Minimum supported system</span></span><br/> | <span data-ttu-id="18a82-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18a82-125">Windows Vista</span></span> |
| <span data-ttu-id="18a82-126">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="18a82-126">Can be empty</span></span>                        | <span data-ttu-id="18a82-127">Sì</span><span class="sxs-lookup"><span data-stu-id="18a82-127">Yes</span></span>           |



 

 




