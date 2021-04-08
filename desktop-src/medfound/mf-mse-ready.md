---
description: Definisce i diversi stati pronti dell'estensione di origine multimediale.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Enumerazione MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882229"
---
# <a name="mf_mse_ready-enumeration"></a><span data-ttu-id="98506-103">\_ \_ Enumerazione Ready di MF MSE</span><span class="sxs-lookup"><span data-stu-id="98506-103">MF\_MSE\_READY enumeration</span></span>

<span data-ttu-id="98506-104">Definisce i diversi stati pronti dell'estensione di origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="98506-104">Defines the different ready states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="98506-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98506-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a><span data-ttu-id="98506-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="98506-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="98506-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**pronto per MF \_ MSE \_ \_ chiuso**</span><span class="sxs-lookup"><span data-stu-id="98506-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF\_MSE\_READY\_CLOSED**</span></span>
</dt> <dd>

<span data-ttu-id="98506-108">Il codice sorgente multimediale è chiuso.</span><span class="sxs-lookup"><span data-stu-id="98506-108">The media source is closed.</span></span>

</dd> <dt>

<span data-ttu-id="98506-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**pronto per l'uso di MF \_ MSE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="98506-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF\_MSE\_READY\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="98506-110">L'origine multimediale è aperta.</span><span class="sxs-lookup"><span data-stu-id="98506-110">The media source is open.</span></span>

</dd> <dt>

<span data-ttu-id="98506-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**fine del supporto per MF \_ MSE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="98506-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF\_MSE\_READY\_ENDED**</span></span>
</dt> <dd>

<span data-ttu-id="98506-112">L'origine multimediale è terminata.</span><span class="sxs-lookup"><span data-stu-id="98506-112">The media source is ended.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98506-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98506-113">Requirements</span></span>



| <span data-ttu-id="98506-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98506-114">Requirement</span></span> | <span data-ttu-id="98506-115">Valore</span><span class="sxs-lookup"><span data-stu-id="98506-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="98506-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98506-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98506-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98506-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="98506-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98506-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98506-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="98506-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="98506-120">IDL</span><span class="sxs-lookup"><span data-stu-id="98506-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98506-121"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98506-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98506-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98506-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98506-123">Enumerazioni di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98506-123">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




