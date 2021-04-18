---
description: Indica un tipo di modifica dello stato del servizio per il monitoraggio e la creazione di report.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Enumerazione SC_EVENT_TYPE (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318222"
---
# <a name="sc_event_type-enumeration"></a><span data-ttu-id="1ddc4-103">Enumerazione del tipo di \_ evento SC \_</span><span class="sxs-lookup"><span data-stu-id="1ddc4-103">SC\_EVENT\_TYPE enumeration</span></span>

<span data-ttu-id="1ddc4-104">Indica un tipo di modifica dello stato del servizio per il monitoraggio e la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-104">Indicates a type of service status change for monitoring and reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ddc4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ddc4-105">Syntax</span></span>


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1ddc4-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="1ddc4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1ddc4-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**\_ \_ modifica database eventi \_ SC**</span><span class="sxs-lookup"><span data-stu-id="1ddc4-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC\_EVENT\_DATABASE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="1ddc4-108">Un servizio è stato aggiunto o eliminato.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-108">A service has been added or deleted.</span></span> <span data-ttu-id="1ddc4-109">Il parametro *hService* della funzione [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve essere un handle per SCM.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-109">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the SCM.</span></span>

</dd> <dt>

<span data-ttu-id="1ddc4-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**\_ \_ modifica proprietà evento \_ SC**</span><span class="sxs-lookup"><span data-stu-id="1ddc4-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC\_EVENT\_PROPERTY\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="1ddc4-111">Una o più proprietà del servizio sono state aggiornate.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-111">One or more of service properties have been updated.</span></span> <span data-ttu-id="1ddc4-112">Il parametro *hService* della funzione [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve essere un handle per il servizio.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-112">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1ddc4-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_ \_ modifica dello stato dell'evento SC \_**</span><span class="sxs-lookup"><span data-stu-id="1ddc4-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC\_EVENT\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="1ddc4-114">Lo stato di un servizio è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-114">The status of a service has changed.</span></span> <span data-ttu-id="1ddc4-115">Il parametro *hService* della funzione [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) deve essere un handle per il servizio.</span><span class="sxs-lookup"><span data-stu-id="1ddc4-115">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ddc4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ddc4-116">Requirements</span></span>



| <span data-ttu-id="1ddc4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ddc4-117">Requirement</span></span> | <span data-ttu-id="1ddc4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1ddc4-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddc4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ddc4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ddc4-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1ddc4-120">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="1ddc4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ddc4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ddc4-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ddc4-122">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="1ddc4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ddc4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ddc4-124"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ddc4-124"><dt>Winsvcp.h</dt></span></span> </dl> |



 

 




