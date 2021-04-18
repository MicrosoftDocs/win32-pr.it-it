---
description: I \_ \_ valori di enumerazione degli Stati dell'operazione WPD descrivono lo stato corrente di un'operazione in corso.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Enumerazione WPD_OPERATION_STATES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330561"
---
# <a name="wpd_operation_states-enumeration"></a><span data-ttu-id="897cb-103">\_ \_ Enumerazione degli Stati dell'operazione WPD</span><span class="sxs-lookup"><span data-stu-id="897cb-103">WPD\_OPERATION\_STATES enumeration</span></span>

<span data-ttu-id="897cb-104">I valori di enumerazione **\_ \_ degli Stati dell'operazione WPD** descrivono lo stato corrente di un'operazione in corso.</span><span class="sxs-lookup"><span data-stu-id="897cb-104">The **WPD\_OPERATION\_STATES** enumeration values describe the current state of an operation in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="897cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="897cb-105">Syntax</span></span>


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a><span data-ttu-id="897cb-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="897cb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="897cb-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**stato dell'operazione WPD non \_ \_ \_ specificato**</span><span class="sxs-lookup"><span data-stu-id="897cb-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**WPD\_OPERATION\_STATE\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="897cb-108">L'operazione corrente è in uno stato non specificato (non impostato) ed è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="897cb-108">The current operation is in an unspecified state (not set) and unknown.</span></span>

</dd> <dt>

<span data-ttu-id="897cb-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**\_stato dell'operazione WPD \_ \_ avviato**</span><span class="sxs-lookup"><span data-stu-id="897cb-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD\_OPERATION\_STATE\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="897cb-110">L'operazione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="897cb-110">The operation is started.</span></span>

</dd> <dt>

<span data-ttu-id="897cb-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**\_stato dell'operazione WPD \_ \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="897cb-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD\_OPERATION\_STATE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="897cb-112">L'operazione è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="897cb-112">The operation is running.</span></span>

</dd> <dt>

<span data-ttu-id="897cb-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**\_stato dell'operazione WPD \_ \_ sospeso**</span><span class="sxs-lookup"><span data-stu-id="897cb-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD\_OPERATION\_STATE\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="897cb-114">L'operazione è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="897cb-114">The operation is paused.</span></span>

</dd> <dt>

<span data-ttu-id="897cb-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**\_stato dell'operazione WPD \_ \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="897cb-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD\_OPERATION\_STATE\_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="897cb-116">L'operazione è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="897cb-116">The operation is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="897cb-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**\_stato dell'operazione WPD \_ \_ terminato**</span><span class="sxs-lookup"><span data-stu-id="897cb-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD\_OPERATION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="897cb-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="897cb-118">The operation is finished.</span></span>

</dd> <dt>

<span data-ttu-id="897cb-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**\_stato dell'operazione WPD \_ \_ interrotto**</span><span class="sxs-lookup"><span data-stu-id="897cb-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD\_OPERATION\_STATE\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="897cb-120">Operazione interrotta.</span><span class="sxs-lookup"><span data-stu-id="897cb-120">The operation is aborted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="897cb-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="897cb-121">Remarks</span></span>

<span data-ttu-id="897cb-122">Questi valori vengono ricevuti nel callback definito dall'applicazione ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span><span class="sxs-lookup"><span data-stu-id="897cb-122">These values are received in the application-defined callback ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span></span>

## <a name="requirements"></a><span data-ttu-id="897cb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="897cb-123">Requirements</span></span>



| <span data-ttu-id="897cb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="897cb-124">Requirement</span></span> | <span data-ttu-id="897cb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="897cb-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="897cb-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="897cb-126">Header</span></span><br/> | <dl> <span data-ttu-id="897cb-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="897cb-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="897cb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="897cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="897cb-129">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="897cb-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




