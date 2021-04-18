---
description: Recupera una matrice contenente gli identificatori di proprietà del pacchetto per il tratto specificato.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'Metodo IContextNode:: GetStrokePacketDescriptionById (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307430"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a><span data-ttu-id="7b03a-103">Metodo IContextNode:: GetStrokePacketDescriptionById</span><span class="sxs-lookup"><span data-stu-id="7b03a-103">IContextNode::GetStrokePacketDescriptionById method</span></span>

<span data-ttu-id="7b03a-104">Recupera una matrice contenente gli identificatori di proprietà del pacchetto per il tratto specificato.</span><span class="sxs-lookup"><span data-stu-id="7b03a-104">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b03a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b03a-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a><span data-ttu-id="7b03a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b03a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b03a-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b03a-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b03a-108">Identificatore del tratto.</span><span class="sxs-lookup"><span data-stu-id="7b03a-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="7b03a-109">*pulStrokePacketDescriptionCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7b03a-109">*pulStrokePacketDescriptionCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b03a-110">Numero di proprietà dei pacchetti in ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7b03a-110">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="7b03a-111">*ppStrokePacketDescriptionGuids* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7b03a-111">*ppStrokePacketDescriptionGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b03a-112">Matrice contenente gli identificatori di proprietà del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7b03a-112">An array containing the packet property identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b03a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b03a-113">Return value</span></span>

<span data-ttu-id="7b03a-114">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7b03a-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b03a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b03a-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7b03a-116">Per evitare una perdita di memoria, usare [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare la memoria da \* *ppStrokePacketDescriptionGuids* quando le informazioni non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="7b03a-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppStrokePacketDescriptionGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="7b03a-117">\**ppStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto del tratto.</span><span class="sxs-lookup"><span data-stu-id="7b03a-117">\**ppStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="7b03a-118">Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7b03a-118">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b03a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b03a-119">Requirements</span></span>



| <span data-ttu-id="7b03a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b03a-120">Requirement</span></span> | <span data-ttu-id="7b03a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7b03a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b03a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b03a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7b03a-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b03a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b03a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b03a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7b03a-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7b03a-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7b03a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b03a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b03a-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b03a-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b03a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7b03a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b03a-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b03a-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7b03a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b03a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b03a-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="7b03a-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7b03a-132">**IContextNode::GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="7b03a-132">**IContextNode::GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[<span data-ttu-id="7b03a-133">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="7b03a-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

