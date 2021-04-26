---
description: Genera costanti C per le tabelle xml schema per i tipi di messaggio.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: Elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998708"
---
# <a name="messagetypedefinitions-element"></a><span data-ttu-id="3fb51-103">Elemento messageTypeDefinitions</span><span class="sxs-lookup"><span data-stu-id="3fb51-103">messageTypeDefinitions element</span></span>

<span data-ttu-id="3fb51-104">Genera costanti C per le tabelle xml schema per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="3fb51-104">Generates C constants for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="3fb51-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3fb51-105">Usage</span></span>

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="3fb51-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="3fb51-106">Attributes</span></span>

<span data-ttu-id="3fb51-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="3fb51-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3fb51-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3fb51-108">Child elements</span></span>



| <span data-ttu-id="3fb51-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fb51-109">Element</span></span>                                   | <span data-ttu-id="3fb51-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fb51-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="3fb51-111">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="3fb51-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="3fb51-112">Specifica un'operazione per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="3fb51-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="3fb51-113">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="3fb51-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="3fb51-114">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="3fb51-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="3fb51-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3fb51-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="3fb51-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3fb51-116">Parent elements</span></span>



| <span data-ttu-id="3fb51-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fb51-117">Element</span></span>                         | <span data-ttu-id="3fb51-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fb51-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="3fb51-119">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="3fb51-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="3fb51-120">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="3fb51-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3fb51-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fb51-121">Remarks</span></span>

<span data-ttu-id="3fb51-122">Questo elemento viene in genere usato nei file di origine C per fornire le tabelle dello schema dichiarate da [**messageTypeDeclarations**](messagetypedeclarations.md).</span><span class="sxs-lookup"><span data-stu-id="3fb51-122">This element is generally used in C source files to provide the schema tables declared by [**messageTypeDeclarations**](messagetypedeclarations.md).</span></span>

## <a name="element-information"></a><span data-ttu-id="3fb51-123">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3fb51-123">Element information</span></span>



| <span data-ttu-id="3fb51-124">Label</span><span class="sxs-lookup"><span data-stu-id="3fb51-124">Label</span></span> | <span data-ttu-id="3fb51-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3fb51-125">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="3fb51-126">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb51-126">Minimum supported system</span></span><br/> | <span data-ttu-id="3fb51-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fb51-127">Windows Vista</span></span> |
| <span data-ttu-id="3fb51-128">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="3fb51-128">Can be empty</span></span>                        | <span data-ttu-id="3fb51-129">Sì</span><span class="sxs-lookup"><span data-stu-id="3fb51-129">Yes</span></span>           |



 

 




