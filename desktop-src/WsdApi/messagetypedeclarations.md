---
description: Genera dichiarazioni di costanti C per le tabelle di XML Schema per i tipi di messaggio.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998728"
---
# <a name="messagetypedeclarations-element"></a><span data-ttu-id="0042a-103">elemento messageTypeDeclarations</span><span class="sxs-lookup"><span data-stu-id="0042a-103">messageTypeDeclarations element</span></span>

<span data-ttu-id="0042a-104">Genera dichiarazioni di costanti C per le tabelle di XML Schema per i tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="0042a-104">Generates C constant declarations for XML schema tables for message types.</span></span>

## <a name="usage"></a><span data-ttu-id="0042a-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0042a-105">Usage</span></span>

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="0042a-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="0042a-106">Attributes</span></span>

<span data-ttu-id="0042a-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="0042a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0042a-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0042a-108">Child elements</span></span>



| <span data-ttu-id="0042a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0042a-109">Element</span></span>                                   | <span data-ttu-id="0042a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0042a-110">Description</span></span>                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="0042a-111">**Operazione**</span><span class="sxs-lookup"><span data-stu-id="0042a-111">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="0042a-112">Specifica un'operazione per la quale deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="0042a-112">Specifies an operation for which code is to be generated.</span></span><br/> <br/>  |
| [<span data-ttu-id="0042a-113">**Porttype**</span><span class="sxs-lookup"><span data-stu-id="0042a-113">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="0042a-114">Specifica il tipo di porta per cui deve essere generato il codice.</span><span class="sxs-lookup"><span data-stu-id="0042a-114">Specifies the port type for which code is to be generated.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0042a-115">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0042a-115">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a><span data-ttu-id="0042a-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0042a-116">Parent elements</span></span>



| <span data-ttu-id="0042a-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="0042a-117">Element</span></span>                         | <span data-ttu-id="0042a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0042a-118">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0042a-119">**ﬁle**</span><span class="sxs-lookup"><span data-stu-id="0042a-119">**file**</span></span>](file.md)<br/> | <span data-ttu-id="0042a-120">Restituisce un file dal generatore di codice.</span><span class="sxs-lookup"><span data-stu-id="0042a-120">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0042a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0042a-121">Remarks</span></span>

<span data-ttu-id="0042a-122">Le definizioni dei tipi di porta fanno riferimento alle tabelle dello schema.</span><span class="sxs-lookup"><span data-stu-id="0042a-122">Schema tables are referenced by port type definitions.</span></span> <span data-ttu-id="0042a-123">Questo elemento viene quindi usato in genere prima degli [**elementi portTypeDefinitions.**](porttypedefinitions.md)</span><span class="sxs-lookup"><span data-stu-id="0042a-123">This element is therefore generally used just prior to [**portTypeDefinitions**](porttypedefinitions.md) elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="0042a-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0042a-124">Element information</span></span>



| <span data-ttu-id="0042a-125">Label</span><span class="sxs-lookup"><span data-stu-id="0042a-125">Label</span></span> | <span data-ttu-id="0042a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0042a-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="0042a-127">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0042a-127">Minimum supported system</span></span><br/> | <span data-ttu-id="0042a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0042a-128">Windows Vista</span></span> |
| <span data-ttu-id="0042a-129">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="0042a-129">Can be empty</span></span>                        | <span data-ttu-id="0042a-130">Sì</span><span class="sxs-lookup"><span data-stu-id="0042a-130">Yes</span></span>           |



 

 




