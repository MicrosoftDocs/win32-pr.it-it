---
description: La proprietà ComponentCosts dell'oggetto Session restituisce un oggetto recordset che enumera lo spazio su disco per ogni unità richiesta per l'installazione di un componente.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Proprietà Session. ComponentCosts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327799"
---
# <a name="sessioncomponentcosts-property"></a><span data-ttu-id="a78cf-103">Proprietà Session. ComponentCosts</span><span class="sxs-lookup"><span data-stu-id="a78cf-103">Session.ComponentCosts property</span></span>

<span data-ttu-id="a78cf-104">La proprietà ComponentCosts dell'oggetto [**Session**](session-object.md) [**restituisce un oggetto**](recordlist-object.md) recordset che enumera lo spazio su disco per ogni unità richiesta per l'installazione di un componente.</span><span class="sxs-lookup"><span data-stu-id="a78cf-104">The ComponentCosts property of the [**Session**](session-object.md) object returns a [**RecordList**](recordlist-object.md) object enumerating the disk space per drive required to install a component.</span></span> <span data-ttu-id="a78cf-105">Queste informazioni vengono utilizzate dall'interfaccia utente per visualizzare lo spazio su disco necessario per tutte le unità.</span><span class="sxs-lookup"><span data-stu-id="a78cf-105">This information is used by the user interface to display the disk space required for all drives.</span></span> <span data-ttu-id="a78cf-106">I costi di spazio su disco restituiti sono in multipli di 512 byte.</span><span class="sxs-lookup"><span data-stu-id="a78cf-106">The returned disk space costs are in multiples of 512 bytes.</span></span>

<span data-ttu-id="a78cf-107">La proprietà ComponentCosts deve essere utilizzata solo dopo che il programma di installazione ha completato il [costo del file](file-costing.md) e dopo l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="a78cf-107">The ComponentCosts property should only be used after the installer has completed [file costing](file-costing.md) and after the [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="a78cf-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a78cf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a78cf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a78cf-109">Syntax</span></span>


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a><span data-ttu-id="a78cf-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a78cf-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a78cf-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a78cf-111">Remarks</span></span>

<span data-ttu-id="a78cf-112">Per ottenere il costo totale, aggiungere i costi per tutti i componenti più il costo del motore di installazione (componente = "").</span><span class="sxs-lookup"><span data-stu-id="a78cf-112">To obtain the total cost, add the costs for all components plus the installer engine cost (Component = "").</span></span>

<span data-ttu-id="a78cf-113">ComponentCosts restituisce un [**oggetto di registrazione**](recordlist-object.md).</span><span class="sxs-lookup"><span data-stu-id="a78cf-113">ComponentCosts returns a [**RecordList object**](recordlist-object.md).</span></span> <span data-ttu-id="a78cf-114">Ogni record nell'oggetto di registrazione restituito presenta i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a78cf-114">Each record in the returned RecordList object has the following fields:</span></span>



| <span data-ttu-id="a78cf-115">Campo</span><span class="sxs-lookup"><span data-stu-id="a78cf-115">Field</span></span> | <span data-ttu-id="a78cf-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a78cf-116">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="a78cf-117">1</span><span class="sxs-lookup"><span data-stu-id="a78cf-117">1</span></span>     | <span data-ttu-id="a78cf-118">Nome volume/unità</span><span class="sxs-lookup"><span data-stu-id="a78cf-118">Volume/Drive name</span></span>                                    |
| <span data-ttu-id="a78cf-119">2</span><span class="sxs-lookup"><span data-stu-id="a78cf-119">2</span></span>     | <span data-ttu-id="a78cf-120">Costo dello spazio su disco finale in multipli di 512 byte.</span><span class="sxs-lookup"><span data-stu-id="a78cf-120">Final disk space cost in multiples of 512 bytes.</span></span>     |
| <span data-ttu-id="a78cf-121">3</span><span class="sxs-lookup"><span data-stu-id="a78cf-121">3</span></span>     | <span data-ttu-id="a78cf-122">Costo di spazio su disco temporaneo in multipli di 512 byte.</span><span class="sxs-lookup"><span data-stu-id="a78cf-122">Temporary disk space cost in multiples of 512 bytes.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a78cf-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a78cf-123">Requirements</span></span>



| <span data-ttu-id="a78cf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a78cf-124">Requirement</span></span> | <span data-ttu-id="a78cf-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a78cf-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a78cf-126">Versione</span><span class="sxs-lookup"><span data-stu-id="a78cf-126">Version</span></span><br/> | <span data-ttu-id="a78cf-127">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a78cf-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a78cf-128">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a78cf-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a78cf-129">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a78cf-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a78cf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a78cf-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="a78cf-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a78cf-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a78cf-132">IID</span><span class="sxs-lookup"><span data-stu-id="a78cf-132">IID</span></span><br/>     | <span data-ttu-id="a78cf-133">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a78cf-133">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




