---
description: Si tratta della Proprietà IntegerData dell'oggetto record. Questa proprietà di lettura/scrittura trasferisce i dati Integer a 32 bit all'interno o all'esterno di un campo specificato all'interno del record. Se il valore di un campo non può essere convertito in un numero intero, viene restituito msiDatabaseNullInteger.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Proprietà record. IntegerData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328768"
---
# <a name="recordintegerdata-property"></a><span data-ttu-id="e53b4-105">Proprietà record. IntegerData</span><span class="sxs-lookup"><span data-stu-id="e53b4-105">Record.IntegerData property</span></span>

<span data-ttu-id="e53b4-106">Si tratta della proprietà **IntegerData** dell'oggetto [**record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e53b4-106">This is the **IntegerData** property of the [**Record**](record-object.md) object.</span></span> <span data-ttu-id="e53b4-107">Questa proprietà di lettura/scrittura trasferisce i dati Integer a 32 bit all'interno o all'esterno di un campo specificato all'interno del record.</span><span class="sxs-lookup"><span data-stu-id="e53b4-107">This read-write property transfers 32-bit integer data in to or out of a specified field within the record.</span></span> <span data-ttu-id="e53b4-108">Se il valore di un campo non può essere convertito in un numero intero, viene restituito msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="e53b4-108">If a field value cannot be converted to an integer, msiDatabaseNullInteger is returned.</span></span>

<span data-ttu-id="e53b4-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e53b4-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53b4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e53b4-110">Syntax</span></span>


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="e53b4-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e53b4-111">Property value</span></span>

<span data-ttu-id="e53b4-112">Numero di campo obbligatorio del valore all'interno del record, basato su 1.</span><span class="sxs-lookup"><span data-stu-id="e53b4-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="e53b4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e53b4-113">Remarks</span></span>

<span data-ttu-id="e53b4-114">Per impostare un campo record Integer su null, utilizzare msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="e53b4-114">To set a record integer field to null, use msiDatabaseNullInteger.</span></span> <span data-ttu-id="e53b4-115">Il valore restituito di un campo inesistente è msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="e53b4-115">The returned value of a nonexistent field is msiDatabaseNullInteger.</span></span> <span data-ttu-id="e53b4-116">Il tentativo di archiviare un valore in un campo inesistente causa un errore.</span><span class="sxs-lookup"><span data-stu-id="e53b4-116">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53b4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e53b4-117">Requirements</span></span>



| <span data-ttu-id="e53b4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e53b4-118">Requirement</span></span> | <span data-ttu-id="e53b4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e53b4-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e53b4-120">Versione</span><span class="sxs-lookup"><span data-stu-id="e53b4-120">Version</span></span><br/> | <span data-ttu-id="e53b4-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e53b4-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e53b4-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e53b4-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e53b4-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e53b4-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e53b4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e53b4-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="e53b4-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e53b4-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e53b4-126">IID</span><span class="sxs-lookup"><span data-stu-id="e53b4-126">IID</span></span><br/>     | <span data-ttu-id="e53b4-127">IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e53b4-127">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




