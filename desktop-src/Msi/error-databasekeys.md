---
description: La proprietà DatabaseKeys di sola lettura dell'oggetto Error restituisce una raccolta di stringhe contenente le chiavi primarie della riga del database che hanno causato l'errore. È presente una chiave per ogni voce nella raccolta.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Proprietà Error. DatabaseKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324245"
---
# <a name="errordatabasekeys-property"></a><span data-ttu-id="3fd31-104">Proprietà Error. DatabaseKeys</span><span class="sxs-lookup"><span data-stu-id="3fd31-104">Error.DatabaseKeys property</span></span>

<span data-ttu-id="3fd31-105">La proprietà **DatabaseKeys** di sola lettura dell'oggetto [**Error**](error-object.md) restituisce una raccolta di stringhe contenente le chiavi primarie della riga del database che hanno causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="3fd31-105">The read-only **DatabaseKeys** property of the [**Error**](error-object.md) object returns a string collection that contains the primary keys of the database row causing the error.</span></span> <span data-ttu-id="3fd31-106">È presente una chiave per ogni voce nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="3fd31-106">There is one key per entry in the collection.</span></span>

<span data-ttu-id="3fd31-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3fd31-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd31-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fd31-108">Syntax</span></span>


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a><span data-ttu-id="3fd31-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3fd31-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd31-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fd31-110">Remarks</span></span>

<span data-ttu-id="3fd31-111">Il client è responsabile del rilascio della raccolta di stringhe quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="3fd31-111">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="3fd31-112">La raccolta è vuota se i valori non sono validi per il tipo di errore.</span><span class="sxs-lookup"><span data-stu-id="3fd31-112">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="3fd31-113">È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd31-113">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="3fd31-114">C++</span><span class="sxs-lookup"><span data-stu-id="3fd31-114">C++</span></span>

<span data-ttu-id="3fd31-115">Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) la funzione DatabaseKeys.</span><span class="sxs-lookup"><span data-stu-id="3fd31-115">See [**get\_DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd31-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fd31-116">Requirements</span></span>



| <span data-ttu-id="3fd31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd31-117">Requirement</span></span> | <span data-ttu-id="3fd31-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd31-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd31-119">Versione</span><span class="sxs-lookup"><span data-stu-id="3fd31-119">Version</span></span><br/> | <span data-ttu-id="3fd31-120">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3fd31-120">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3fd31-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fd31-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3fd31-122"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd31-122"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3fd31-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3fd31-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="3fd31-124"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fd31-124"><dt>Mergemod.dll</dt></span></span> </dl> |



 

