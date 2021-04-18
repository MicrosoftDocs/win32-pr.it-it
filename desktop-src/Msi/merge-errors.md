---
description: La proprietà errori di sola lettura dell'oggetto merge restituisce una raccolta di oggetti Error che rappresenta il set di errori corrente.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Proprietà merge. Errors (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327804"
---
# <a name="mergeerrors-property"></a><span data-ttu-id="5396e-103">Merge. Errors (proprietà)</span><span class="sxs-lookup"><span data-stu-id="5396e-103">Merge.Errors property</span></span>

<span data-ttu-id="5396e-104">La proprietà **errori** di sola lettura dell'oggetto [**merge**](merge-object.md) restituisce una raccolta di oggetti [**Error**](error-object.md) che rappresenta il set di errori corrente.</span><span class="sxs-lookup"><span data-stu-id="5396e-104">The read-only **Errors** property of the [**Merge**](merge-object.md) object returns a collection of [**Error**](error-object.md) objects that is the current set of errors.</span></span>

<span data-ttu-id="5396e-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5396e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5396e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5396e-106">Syntax</span></span>


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a><span data-ttu-id="5396e-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5396e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5396e-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="5396e-108">Remarks</span></span>

<span data-ttu-id="5396e-109">Il recupero non è distruttivo.</span><span class="sxs-lookup"><span data-stu-id="5396e-109">The retrieval is non-destructive.</span></span> <span data-ttu-id="5396e-110">È possibile recuperare più istanze della raccolta Error chiamando ripetutamente questo metodo.</span><span class="sxs-lookup"><span data-stu-id="5396e-110">Multiple instances of the error collection may be retrieved by repeatedly calling this method.</span></span>

### <a name="c"></a><span data-ttu-id="5396e-111">C++</span><span class="sxs-lookup"><span data-stu-id="5396e-111">C++</span></span>

<span data-ttu-id="5396e-112">Vedere la funzione [**get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) .</span><span class="sxs-lookup"><span data-stu-id="5396e-112">See [**get\_Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5396e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5396e-113">Requirements</span></span>



| <span data-ttu-id="5396e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5396e-114">Requirement</span></span> | <span data-ttu-id="5396e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5396e-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5396e-116">Versione</span><span class="sxs-lookup"><span data-stu-id="5396e-116">Version</span></span><br/> | <span data-ttu-id="5396e-117">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5396e-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5396e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5396e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5396e-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="5396e-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5396e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="5396e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="5396e-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5396e-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
