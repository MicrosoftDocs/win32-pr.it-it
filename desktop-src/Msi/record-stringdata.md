---
description: La proprietà StringData dell'oggetto record è una proprietà di lettura/scrittura che trasferisce i dati stringa in o da un campo specificato all'interno del record. Se è stato archiviato un intero o un oggetto, viene restituito il relativo valore stringa.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Proprietà record. StringData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328762"
---
# <a name="recordstringdata-property"></a><span data-ttu-id="53c55-104">Proprietà record. StringData</span><span class="sxs-lookup"><span data-stu-id="53c55-104">Record.StringData property</span></span>

<span data-ttu-id="53c55-105">La proprietà **StringData** dell'oggetto [**record**](record-object.md) è una proprietà di lettura/scrittura che trasferisce i dati stringa in o da un campo specificato all'interno del record.</span><span class="sxs-lookup"><span data-stu-id="53c55-105">The **StringData** property of the [**Record**](record-object.md) object is a read-write property that transfers string data in to or out of a specified field within the record.</span></span> <span data-ttu-id="53c55-106">Se è stato archiviato un intero o un oggetto, viene restituito il relativo valore stringa.</span><span class="sxs-lookup"><span data-stu-id="53c55-106">If an integer or object has been stored, its string value is returned.</span></span>

<span data-ttu-id="53c55-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="53c55-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c55-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53c55-108">Syntax</span></span>


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="53c55-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="53c55-109">Property value</span></span>

<span data-ttu-id="53c55-110">Numero di campo obbligatorio del valore all'interno del record, basato su 1.</span><span class="sxs-lookup"><span data-stu-id="53c55-110">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c55-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="53c55-111">Remarks</span></span>

<span data-ttu-id="53c55-112">Il valore restituito di un campo inesistente è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="53c55-112">The returned value of a nonexistent field is an empty string.</span></span> <span data-ttu-id="53c55-113">Per impostare un campo della stringa di record su null, utilizzare una stringa Variant vuota o vuota.</span><span class="sxs-lookup"><span data-stu-id="53c55-113">To set a record string field to null, use either an empty variant or an empty string.</span></span> <span data-ttu-id="53c55-114">Il tentativo di archiviare un valore in un campo inesistente causa un errore.</span><span class="sxs-lookup"><span data-stu-id="53c55-114">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c55-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53c55-115">Requirements</span></span>



| <span data-ttu-id="53c55-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c55-116">Requirement</span></span> | <span data-ttu-id="53c55-117">Valore</span><span class="sxs-lookup"><span data-stu-id="53c55-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c55-118">Versione</span><span class="sxs-lookup"><span data-stu-id="53c55-118">Version</span></span><br/> | <span data-ttu-id="53c55-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="53c55-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="53c55-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="53c55-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="53c55-121">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="53c55-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="53c55-122">DLL</span><span class="sxs-lookup"><span data-stu-id="53c55-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="53c55-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53c55-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="53c55-124">IID</span><span class="sxs-lookup"><span data-stu-id="53c55-124">IID</span></span><br/>     | <span data-ttu-id="53c55-125">IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="53c55-125">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




