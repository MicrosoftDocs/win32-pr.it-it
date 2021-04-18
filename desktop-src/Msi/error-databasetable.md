---
description: La proprietà DatabaseTable di sola lettura dell'oggetto Error restituisce il nome della tabella nel database che ha causato l'errore.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Proprietà Error. DatabaseTable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324244"
---
# <a name="errordatabasetable-property"></a><span data-ttu-id="ec72d-103">Proprietà Error. DatabaseTable</span><span class="sxs-lookup"><span data-stu-id="ec72d-103">Error.DatabaseTable property</span></span>

<span data-ttu-id="ec72d-104">La proprietà **DatabaseTable** di sola lettura dell'oggetto [**Error**](error-object.md) restituisce il nome della tabella nel database che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="ec72d-104">The read-only **DatabaseTable** property of the [**Error**](error-object.md) object returns the name of the table in the database that caused the error.</span></span>

<span data-ttu-id="ec72d-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ec72d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec72d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec72d-106">Syntax</span></span>


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a><span data-ttu-id="ec72d-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ec72d-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ec72d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec72d-108">Remarks</span></span>

<span data-ttu-id="ec72d-109">La raccolta è vuota se i valori non sono validi per il tipo di errore.</span><span class="sxs-lookup"><span data-stu-id="ec72d-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="ec72d-110">È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ec72d-110">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="ec72d-111">C++</span><span class="sxs-lookup"><span data-stu-id="ec72d-111">C++</span></span>

<span data-ttu-id="ec72d-112">Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) la funzione DatabaseTable.</span><span class="sxs-lookup"><span data-stu-id="ec72d-112">See [**get\_DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec72d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec72d-113">Requirements</span></span>



| <span data-ttu-id="ec72d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec72d-114">Requirement</span></span> | <span data-ttu-id="ec72d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ec72d-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec72d-116">Versione</span><span class="sxs-lookup"><span data-stu-id="ec72d-116">Version</span></span><br/> | <span data-ttu-id="ec72d-117">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ec72d-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="ec72d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec72d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ec72d-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec72d-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec72d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ec72d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ec72d-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec72d-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

