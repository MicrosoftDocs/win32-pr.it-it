---
description: La proprietà ComponentRequestState dell'oggetto Session Ottiene o richiede una modifica nello stato dell'azione di una riga nella tabella dei componenti.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Proprietà Session. ComponentRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329110"
---
# <a name="sessioncomponentrequeststate-property"></a><span data-ttu-id="3db9b-103">Proprietà Session. ComponentRequestState</span><span class="sxs-lookup"><span data-stu-id="3db9b-103">Session.ComponentRequestState property</span></span>

<span data-ttu-id="3db9b-104">La proprietà **ComponentRequestState** dell'oggetto [**Session**](session-object.md) Ottiene o richiede una modifica nello stato dell'azione di una riga nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="3db9b-104">The **ComponentRequestState** property of the [**Session**](session-object.md) object obtains or requests a change in the Action state of a row in the [Component table](component-table.md).</span></span>

<span data-ttu-id="3db9b-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3db9b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db9b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3db9b-106">Syntax</span></span>


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a><span data-ttu-id="3db9b-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3db9b-107">Property value</span></span>

<span data-ttu-id="3db9b-108">Nome stringa obbligatorio dell'elemento componente, chiave primaria della tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="3db9b-108">Required string name of the component item, primary key of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="3db9b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3db9b-109">Remarks</span></span>



| <span data-ttu-id="3db9b-110">Stato selezione</span><span class="sxs-lookup"><span data-stu-id="3db9b-110">Selection state</span></span>        | <span data-ttu-id="3db9b-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3db9b-111">Value</span></span> | <span data-ttu-id="3db9b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3db9b-112">Description</span></span>                                                    |
|------------------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="3db9b-113">Null</span><span class="sxs-lookup"><span data-stu-id="3db9b-113">Null</span></span>                   | <span data-ttu-id="3db9b-114">Null</span><span class="sxs-lookup"><span data-stu-id="3db9b-114">Null</span></span>  | <span data-ttu-id="3db9b-115">Richiede che non venga eseguita alcuna azione per questo elemento.</span><span class="sxs-lookup"><span data-stu-id="3db9b-115">Requests that no action be taken for this item.</span></span>                |
| <span data-ttu-id="3db9b-116">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="3db9b-116">msiInstallStateAbsent</span></span>  | <span data-ttu-id="3db9b-117">2</span><span class="sxs-lookup"><span data-stu-id="3db9b-117">2</span></span>     | <span data-ttu-id="3db9b-118">L'elemento deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="3db9b-118">Item is to be removed.</span></span>                                         |
| <span data-ttu-id="3db9b-119">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="3db9b-119">msiInstallStateLocal</span></span>   | <span data-ttu-id="3db9b-120">3</span><span class="sxs-lookup"><span data-stu-id="3db9b-120">3</span></span>     | <span data-ttu-id="3db9b-121">L'elemento deve essere installato localmente.</span><span class="sxs-lookup"><span data-stu-id="3db9b-121">Item is to be installed locally.</span></span>                               |
| <span data-ttu-id="3db9b-122">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="3db9b-122">msiInstallStateSource</span></span>  | <span data-ttu-id="3db9b-123">4</span><span class="sxs-lookup"><span data-stu-id="3db9b-123">4</span></span>     | <span data-ttu-id="3db9b-124">L'elemento deve essere installato ed eseguito dal supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="3db9b-124">Item is to be installed and run from the source media.</span></span>         |
| <span data-ttu-id="3db9b-125">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="3db9b-125">msiInstallStateDefault</span></span> | <span data-ttu-id="3db9b-126">5</span><span class="sxs-lookup"><span data-stu-id="3db9b-126">5</span></span>     | <span data-ttu-id="3db9b-127">Se installato, l'elemento deve essere reinstallato nello stesso stato.</span><span class="sxs-lookup"><span data-stu-id="3db9b-127">If installed, the item is to be reinstalled in the same state.</span></span> |



 

<span data-ttu-id="3db9b-128">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="3db9b-128">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db9b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3db9b-129">Requirements</span></span>



| <span data-ttu-id="3db9b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3db9b-130">Requirement</span></span> | <span data-ttu-id="3db9b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3db9b-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3db9b-132">Versione</span><span class="sxs-lookup"><span data-stu-id="3db9b-132">Version</span></span><br/> | <span data-ttu-id="3db9b-133">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3db9b-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3db9b-134">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3db9b-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3db9b-135">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="3db9b-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3db9b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3db9b-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="3db9b-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3db9b-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3db9b-138">IID</span><span class="sxs-lookup"><span data-stu-id="3db9b-138">IID</span></span><br/>     | <span data-ttu-id="3db9b-139">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3db9b-139">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




