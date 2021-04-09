---
title: Enumerazione RAS_PARAMS_FORMAT (rassapi. h)
description: Il \_ \_ tipo di enumerazione del formato params RAS viene usato nella \_ struttura dei parametri RAS per indicare il tipo di dati associato a una chiave specifica del supporto.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS enumerazione RAS_PARAMS_FORMAT
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120246"
---
# <a name="ras_params_format-enumeration"></a><span data-ttu-id="98240-104">\_Enumerazione del formato params RAS \_</span><span class="sxs-lookup"><span data-stu-id="98240-104">RAS\_PARAMS\_FORMAT enumeration</span></span>

<span data-ttu-id="98240-105">\[L'enumerazione del **\_ \_ formato params RAS** non è supportata in Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="98240-105">\[The **RAS\_PARAMS\_FORMAT** enumeration is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="98240-106">Il tipo di enumerazione del **\_ \_ formato params RAS** viene usato nella struttura dei [**\_ parametri RAS**](ras-parameters-str.md) per indicare il tipo di dati associato a una chiave specifica del supporto.</span><span class="sxs-lookup"><span data-stu-id="98240-106">The **RAS\_PARAMS\_FORMAT** enumeration type is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to indicate the type of data associated with a media-specific key.</span></span>

## <a name="syntax"></a><span data-ttu-id="98240-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98240-107">Syntax</span></span>


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="98240-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="98240-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="98240-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span><span class="sxs-lookup"><span data-stu-id="98240-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span></span>
</dt> <dd>

<span data-ttu-id="98240-110">Indica che i dati associati alla chiave sono numerici.</span><span class="sxs-lookup"><span data-stu-id="98240-110">Indicates that the data associated with the key is a number.</span></span>

</dd> <dt>

<span data-ttu-id="98240-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span><span class="sxs-lookup"><span data-stu-id="98240-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span></span>
</dt> <dd>

<span data-ttu-id="98240-112">Indica che i dati associati alla chiave sono una stringa.</span><span class="sxs-lookup"><span data-stu-id="98240-112">Indicates that the data associated with the key is a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98240-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98240-113">Requirements</span></span>



| <span data-ttu-id="98240-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98240-114">Requirement</span></span> | <span data-ttu-id="98240-115">Valore</span><span class="sxs-lookup"><span data-stu-id="98240-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="98240-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98240-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98240-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98240-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="98240-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98240-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98240-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98240-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="98240-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="98240-120">End of client support</span></span><br/>    | <span data-ttu-id="98240-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="98240-121">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="98240-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="98240-122">End of server support</span></span><br/>    | <span data-ttu-id="98240-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="98240-123">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="98240-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98240-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="98240-125"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="98240-125"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98240-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98240-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98240-127">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="98240-127">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="98240-128">Enumerazioni di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="98240-128">RAS Server Administration Enumerations</span></span>](ras-server-administration-enumerations.md)
</dt> <dt>

[<span data-ttu-id="98240-129">**\_parametri RAS**</span><span class="sxs-lookup"><span data-stu-id="98240-129">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> </dl>

 

 





