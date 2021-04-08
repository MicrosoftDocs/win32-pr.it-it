---
description: Genera dichiarazioni di costanti C per XML Schema tabelle per i tipi di messaggio.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 700511d3c0a83badcb15b0e07491a14ade53f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968185"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="0fff3-103">elemento messageTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="0fff3-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="0fff3-104">Genera dichiarazioni di costanti C per XML Schema tabelle per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="0fff3-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="0fff3-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0fff3-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="0fff3-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="0fff3-106">Attributes</span></span>

<span data-ttu-id="0fff3-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="0fff3-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0fff3-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0fff3-108">Child elements</span></span>



| <span data-ttu-id="0fff3-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0fff3-109">Element</span></span>                                   | <span data-ttu-id="0fff3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fff3-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="0fff3-111">**operazione**</span><span class="sxs-lookup"><span data-stu-id="0fff3-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="0fff3-112">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="0fff3-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="0fff3-113">**portType**</span><span class="sxs-lookup"><span data-stu-id="0fff3-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="0fff3-114">Specifica il tipo di porta per il quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="0fff3-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0fff3-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0fff3-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="0fff3-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0fff3-116">Parent elements</span></span>



| <span data-ttu-id="0fff3-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="0fff3-117">Element</span></span>                         | <span data-ttu-id="0fff3-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fff3-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0fff3-119">**file**</span><span class="sxs-lookup"><span data-stu-id="0fff3-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0fff3-120">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="0fff3-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0fff3-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fff3-121">Remarks</span></span>

<span data-ttu-id="0fff3-122">Le definizioni dei tipi di porta fanno riferimento alle tabelle dello schema.</span><span class="sxs-lookup"><span data-stu-id="0fff3-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="0fff3-123">Questo elemento viene quindi in genere usato poco prima degli elementi [**portTypeDefinitions**](porttypedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="0fff3-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="0fff3-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0fff3-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0fff3-125">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fff3-125">Minimum supported system</span></span><br/> | <span data-ttu-id="0fff3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fff3-126">Windows Vista</span></span> |
| <span data-ttu-id="0fff3-127">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0fff3-127">Can be empty</span></span>                        | <span data-ttu-id="0fff3-128">Sì</span><span class="sxs-lookup"><span data-stu-id="0fff3-128">Yes</span></span>           |



 

 




