---
description: Il metodo CreateObject dell'oggetto Microsoft. Windows. ActCtx crea un oggetto nel contesto del manifesto corrente.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: Metodo ActCtx. CreateObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232049"
---
# <a name="actctxcreateobject-method"></a><span data-ttu-id="18ecc-103">Metodo ActCtx. CreateObject</span><span class="sxs-lookup"><span data-stu-id="18ecc-103">ActCtx.CreateObject method</span></span>

<span data-ttu-id="18ecc-104">Il metodo **CreateObject** dell'oggetto [**Microsoft. Windows. ACTCTX**](microsoft-windows-actctx-object.md) crea un oggetto nel contesto del manifesto corrente.</span><span class="sxs-lookup"><span data-stu-id="18ecc-104">The **CreateObject** method of the [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object creates an object in the context of the current manifest.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ecc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18ecc-105">Syntax</span></span>


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a><span data-ttu-id="18ecc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18ecc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ecc-107">*objectId*</span><span class="sxs-lookup"><span data-stu-id="18ecc-107">*objectId*</span></span> 
</dt> <dd>

<span data-ttu-id="18ecc-108">Stringa che specifica il tipo di oggetto da creare.</span><span class="sxs-lookup"><span data-stu-id="18ecc-108">A string that specifies the type of object to create.</span></span> <span data-ttu-id="18ecc-109">Ad esempio, un ProgID COM.</span><span class="sxs-lookup"><span data-stu-id="18ecc-109">For example, a COM ProgID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ecc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18ecc-110">Return value</span></span>

<span data-ttu-id="18ecc-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="18ecc-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ecc-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18ecc-112">Requirements</span></span>



| <span data-ttu-id="18ecc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ecc-113">Requirement</span></span> | <span data-ttu-id="18ecc-114">Valore</span><span class="sxs-lookup"><span data-stu-id="18ecc-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="18ecc-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18ecc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="18ecc-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18ecc-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="18ecc-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18ecc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="18ecc-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="18ecc-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="18ecc-119">DLL</span><span class="sxs-lookup"><span data-stu-id="18ecc-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18ecc-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18ecc-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="18ecc-121">IID</span><span class="sxs-lookup"><span data-stu-id="18ecc-121">IID</span></span><br/>                      | <span data-ttu-id="18ecc-122">IID \_ IActCtx è definito come 8FA7728F-B69B-4ee5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="18ecc-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="18ecc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18ecc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ecc-124">**Metodo GetObject**</span><span class="sxs-lookup"><span data-stu-id="18ecc-124">**GetObject Method**</span></span>](getobject.md)
</dt> </dl>

 

 




