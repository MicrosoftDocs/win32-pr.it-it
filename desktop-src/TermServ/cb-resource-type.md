---
title: Enumerazione CB_RESOURCE_TYPE (Cbclient. h)
description: Specifica il tipo di risorsa a cui si connette la connessione in ingresso.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- Enumerazione CB_RESOURCE_TYPE Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740583"
---
# <a name="cb_resource_type-enumeration"></a><span data-ttu-id="2f816-104">Enumerazione del tipo di \_ risorsa CB \_</span><span class="sxs-lookup"><span data-stu-id="2f816-104">CB\_RESOURCE\_TYPE enumeration</span></span>

<span data-ttu-id="2f816-105">Specifica il tipo di risorsa a cui si connette la connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="2f816-105">Specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="2f816-106">Questa enumerazione viene utilizzata con la struttura delle [**\_ \_ informazioni di connessione CB**](cb-connection-info.md) .</span><span class="sxs-lookup"><span data-stu-id="2f816-106">This enumeration is used with the [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f816-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f816-107">Syntax</span></span>


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="2f816-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="2f816-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2f816-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**risorsa CB non \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="2f816-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB\_RESOURCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="2f816-110">Il tipo di risorsa non è definito.</span><span class="sxs-lookup"><span data-stu-id="2f816-110">The resource type is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="2f816-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_sessione di risorse CB \_**</span><span class="sxs-lookup"><span data-stu-id="2f816-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB\_RESOURCE\_SESSION**</span></span>
</dt> <dd>

<span data-ttu-id="2f816-112">La risorsa è una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="2f816-112">The resource is a remote session.</span></span>

</dd> <dt>

<span data-ttu-id="2f816-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_VM delle risorse CB \_**</span><span class="sxs-lookup"><span data-stu-id="2f816-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB\_RESOURCE\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="2f816-114">La risorsa è una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f816-114">The resource is a virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f816-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f816-115">Requirements</span></span>



| <span data-ttu-id="2f816-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f816-116">Requirement</span></span> | <span data-ttu-id="2f816-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2f816-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f816-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f816-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f816-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f816-119">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="2f816-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f816-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f816-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f816-121">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="2f816-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f816-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f816-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f816-123"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f816-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f816-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f816-125">**\_informazioni di connessione CB \_**</span><span class="sxs-lookup"><span data-stu-id="2f816-125">**CB\_CONNECTION\_INFO**</span></span>](cb-connection-info.md)
</dt> </dl>

 

 





