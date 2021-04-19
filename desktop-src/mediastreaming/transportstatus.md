---
title: Enumerazione TransportStatus
description: Definisce lo stato del trasporto disponibile come definito dalle linee guida di UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API di streaming multimediale dell'enumerazione TransportStatus
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332881"
---
# <a name="transportstatus-enumeration"></a><span data-ttu-id="ceddd-104">Enumerazione TransportStatus</span><span class="sxs-lookup"><span data-stu-id="ceddd-104">TransportStatus enumeration</span></span>

<span data-ttu-id="ceddd-105">Definisce lo stato del trasporto disponibile come definito dalle linee guida di UPnP.</span><span class="sxs-lookup"><span data-stu-id="ceddd-105">Defines the available transport status as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceddd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ceddd-106">Syntax</span></span>


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a><span data-ttu-id="ceddd-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="ceddd-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ceddd-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="ceddd-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="ceddd-109">Stato del dispositivo errato.</span><span class="sxs-lookup"><span data-stu-id="ceddd-109">Erroneous device status.</span></span>

</dd> <dt>

<span data-ttu-id="ceddd-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**</span><span class="sxs-lookup"><span data-stu-id="ceddd-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**</span></span>
</dt> <dd>

<span data-ttu-id="ceddd-111">Il dispositivo è in uno stato valido.</span><span class="sxs-lookup"><span data-stu-id="ceddd-111">The device is in a good status.</span></span>

</dd> <dt>

<span data-ttu-id="ceddd-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span><span class="sxs-lookup"><span data-stu-id="ceddd-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span></span>
</dt> <dd>

<span data-ttu-id="ceddd-113">Si è verificato un errore nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ceddd-113">An error occurred on the device.</span></span>

</dd> <dt>

<span data-ttu-id="ceddd-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Ultima**</span><span class="sxs-lookup"><span data-stu-id="ceddd-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="ceddd-115">Stato precedente del dispositivo allo stato del trasporto corrente.</span><span class="sxs-lookup"><span data-stu-id="ceddd-115">The device s previous status to the current transport status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ceddd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ceddd-116">Requirements</span></span>



| <span data-ttu-id="ceddd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceddd-117">Requirement</span></span> | <span data-ttu-id="ceddd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ceddd-118">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceddd-119">IDL</span><span class="sxs-lookup"><span data-stu-id="ceddd-119">IDL</span></span><br/> | <dl> <span data-ttu-id="ceddd-120"><dt>Windows. Media. streaming. IDL (riferimento a Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="ceddd-120"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





