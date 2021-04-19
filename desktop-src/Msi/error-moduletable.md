---
description: La proprietà ModuleTable di sola lettura restituisce il nome della tabella nel modulo che ha causato l'errore.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Proprietà Error. ModuleTable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326385"
---
# <a name="errormoduletable-property"></a><span data-ttu-id="21fa8-103">Proprietà Error. ModuleTable</span><span class="sxs-lookup"><span data-stu-id="21fa8-103">Error.ModuleTable property</span></span>

<span data-ttu-id="21fa8-104">La proprietà **ModuleTable** di sola lettura restituisce il nome della tabella nel modulo che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="21fa8-104">The read-only **ModuleTable** Property returns the name of the table in the module that caused the error.</span></span>

<span data-ttu-id="21fa8-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="21fa8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21fa8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21fa8-106">Syntax</span></span>


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a><span data-ttu-id="21fa8-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="21fa8-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="21fa8-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="21fa8-108">Remarks</span></span>

<span data-ttu-id="21fa8-109">La raccolta è vuota se i valori non sono validi per il tipo di errore.</span><span class="sxs-lookup"><span data-stu-id="21fa8-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="21fa8-110">È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="21fa8-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="21fa8-111">C++</span><span class="sxs-lookup"><span data-stu-id="21fa8-111">C++</span></span>

<span data-ttu-id="21fa8-112">Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) la funzione ModuleTable.</span><span class="sxs-lookup"><span data-stu-id="21fa8-112">See [**get\_ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="21fa8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21fa8-113">Requirements</span></span>



| <span data-ttu-id="21fa8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="21fa8-114">Requirement</span></span> | <span data-ttu-id="21fa8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="21fa8-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21fa8-116">Versione</span><span class="sxs-lookup"><span data-stu-id="21fa8-116">Version</span></span><br/> | <span data-ttu-id="21fa8-117">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="21fa8-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="21fa8-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21fa8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="21fa8-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="21fa8-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="21fa8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="21fa8-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="21fa8-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21fa8-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

