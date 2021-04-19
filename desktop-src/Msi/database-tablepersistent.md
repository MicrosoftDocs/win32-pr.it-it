---
description: La proprietà TablePersistent dell'oggetto di database restituisce lo stato di persistenza della tabella come uno dei parametri seguenti.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Proprietà database. TablePersistent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333054"
---
# <a name="databasetablepersistent-property"></a><span data-ttu-id="82256-103">Proprietà database. TablePersistent</span><span class="sxs-lookup"><span data-stu-id="82256-103">Database.TablePersistent property</span></span>

<span data-ttu-id="82256-104">La proprietà **TablePersistent** dell'oggetto di [**database**](database-object.md) restituisce lo stato di persistenza della tabella come uno dei parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="82256-104">The **TablePersistent** property of the [**Database**](database-object.md) object returns the persistence state of the table as one of the following parameters.</span></span>



| <span data-ttu-id="82256-105">Stato tabella</span><span class="sxs-lookup"><span data-stu-id="82256-105">Table state</span></span>               | <span data-ttu-id="82256-106">Valore</span><span class="sxs-lookup"><span data-stu-id="82256-106">Value</span></span> | <span data-ttu-id="82256-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82256-107">Description</span></span>                    |
|---------------------------|-------|--------------------------------|
| <span data-ttu-id="82256-108">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="82256-108">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="82256-109">0</span><span class="sxs-lookup"><span data-stu-id="82256-109">0</span></span>     | <span data-ttu-id="82256-110">Tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="82256-110">Table is temporary.</span></span>            |
| <span data-ttu-id="82256-111">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="82256-111">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="82256-112">1</span><span class="sxs-lookup"><span data-stu-id="82256-112">1</span></span>     | <span data-ttu-id="82256-113">Tabella persistente.</span><span class="sxs-lookup"><span data-stu-id="82256-113">Table is persistent.</span></span>           |
| <span data-ttu-id="82256-114">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="82256-114">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="82256-115">2</span><span class="sxs-lookup"><span data-stu-id="82256-115">2</span></span>     | <span data-ttu-id="82256-116">La tabella non è presente nel database.</span><span class="sxs-lookup"><span data-stu-id="82256-116">Table is not in the database.</span></span>  |
| <span data-ttu-id="82256-117">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="82256-117">msiEvaluateConditionError</span></span> | <span data-ttu-id="82256-118">3</span><span class="sxs-lookup"><span data-stu-id="82256-118">3</span></span>     | <span data-ttu-id="82256-119">Nome di tabella non valido o mancante.</span><span class="sxs-lookup"><span data-stu-id="82256-119">Invalid or missing table name.</span></span> |



 

<span data-ttu-id="82256-120">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="82256-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82256-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82256-121">Syntax</span></span>


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a><span data-ttu-id="82256-122">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="82256-122">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="82256-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82256-123">Requirements</span></span>



| <span data-ttu-id="82256-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="82256-124">Requirement</span></span> | <span data-ttu-id="82256-125">Valore</span><span class="sxs-lookup"><span data-stu-id="82256-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82256-126">Versione</span><span class="sxs-lookup"><span data-stu-id="82256-126">Version</span></span><br/> | <span data-ttu-id="82256-127">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="82256-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="82256-128">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="82256-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="82256-129">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="82256-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="82256-130">DLL</span><span class="sxs-lookup"><span data-stu-id="82256-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="82256-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82256-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="82256-132">IID</span><span class="sxs-lookup"><span data-stu-id="82256-132">IID</span></span><br/>     | <span data-ttu-id="82256-133">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="82256-133">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




