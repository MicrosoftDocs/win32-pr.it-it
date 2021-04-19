---
description: Recupera una matrice contenente i dati della proprietà del pacchetto per il tratto specificato.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'Metodo IContextNode:: GetStrokePacketDataById (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307432"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a><span data-ttu-id="26c5d-103">Metodo IContextNode:: GetStrokePacketDataById</span><span class="sxs-lookup"><span data-stu-id="26c5d-103">IContextNode::GetStrokePacketDataById method</span></span>

<span data-ttu-id="26c5d-104">Recupera una matrice contenente i dati della proprietà del pacchetto per il tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="26c5d-104">Retrieves an array containing the packet property data for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c5d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26c5d-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="26c5d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26c5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c5d-107">*strokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26c5d-107">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26c5d-108">Identificatore del tratto.</span><span class="sxs-lookup"><span data-stu-id="26c5d-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="26c5d-109">*pStrokePacketDataCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="26c5d-109">*pStrokePacketDataCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26c5d-110">Lunghezza della matrice di dati del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="26c5d-110">The length of the packet data array.</span></span>

</dd> <dt>

<span data-ttu-id="26c5d-111">*pplStrokePacketData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="26c5d-111">*pplStrokePacketData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26c5d-112">Puntatore ai dati del pacchetto per il tratto.</span><span class="sxs-lookup"><span data-stu-id="26c5d-112">A pointer to the packet data for the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26c5d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26c5d-113">Return value</span></span>

<span data-ttu-id="26c5d-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="26c5d-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26c5d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="26c5d-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="26c5d-116">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *pplStrokePacketData* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="26c5d-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokePacketData* when you no longer need the information.</span></span>

 

<span data-ttu-id="26c5d-117">*plStrokePacketData* contiene i dati dei pacchetti per tutti i punti del tratto.</span><span class="sxs-lookup"><span data-stu-id="26c5d-117">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="26c5d-118">Per ottenere i tipi di dati dei pacchetti inclusi per ogni punto del tratto, utilizzare [**IContextNode:: GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span><span class="sxs-lookup"><span data-stu-id="26c5d-118">To get the types of packet data included for each point in the stroke, use [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26c5d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26c5d-119">Requirements</span></span>



| <span data-ttu-id="26c5d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="26c5d-120">Requirement</span></span> | <span data-ttu-id="26c5d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="26c5d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26c5d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26c5d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26c5d-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="26c5d-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26c5d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26c5d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26c5d-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="26c5d-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="26c5d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26c5d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="26c5d-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="26c5d-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="26c5d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="26c5d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26c5d-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26c5d-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="26c5d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26c5d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c5d-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="26c5d-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="26c5d-132">**IContextNode::GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="26c5d-132">**IContextNode::GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[<span data-ttu-id="26c5d-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="26c5d-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

