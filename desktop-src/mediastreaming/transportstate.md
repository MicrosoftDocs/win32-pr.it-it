---
title: Enumerazione TransportState
description: Definisce gli Stati di trasporto disponibili come definito dalle linee guida di UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API di streaming multimediale dell'enumerazione TransportState
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332882"
---
# <a name="transportstate-enumeration"></a><span data-ttu-id="7a623-104">Enumerazione TransportState</span><span class="sxs-lookup"><span data-stu-id="7a623-104">TransportState enumeration</span></span>

<span data-ttu-id="7a623-105">Definisce gli Stati di trasporto disponibili come definito dalle linee guida di UPnP.</span><span class="sxs-lookup"><span data-stu-id="7a623-105">Defines the available transport states as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a623-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a623-106">Syntax</span></span>


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a><span data-ttu-id="7a623-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="7a623-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7a623-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="7a623-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="7a623-109">Stato del dispositivo errato.</span><span class="sxs-lookup"><span data-stu-id="7a623-109">Erroneous device state.</span></span>

</dd> <dt>

<span data-ttu-id="7a623-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Fermato**</span><span class="sxs-lookup"><span data-stu-id="7a623-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped**</span></span>
</dt> <dd>

<span data-ttu-id="7a623-111">Il trasporto del dispositivo è in stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="7a623-111">The device s transport is in a stopped state.</span></span>

</dd> <dt>

<span data-ttu-id="7a623-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Riproduzione**</span><span class="sxs-lookup"><span data-stu-id="7a623-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Playing**</span></span>
</dt> <dd>

<span data-ttu-id="7a623-113">Il trasporto del dispositivo è in uno stato di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="7a623-113">The device s transport is in a playing state.</span></span>

</dd> <dt>

<span data-ttu-id="7a623-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione**</span><span class="sxs-lookup"><span data-stu-id="7a623-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning**</span></span>
</dt> <dd>

<span data-ttu-id="7a623-115">Il trasporto del dispositivo è in uno stato di transizione che comporterà un altro valore di stato.</span><span class="sxs-lookup"><span data-stu-id="7a623-115">The device s transport is in a transitioning state which will result in another state value.</span></span>

</dd> <dt>

<span data-ttu-id="7a623-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Pausa**</span><span class="sxs-lookup"><span data-stu-id="7a623-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused**</span></span>
</dt> <dd>

<span data-ttu-id="7a623-117">Il trasporto del dispositivo è in uno stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="7a623-117">The device s transport is in a paused state.</span></span>

</dd> <dt>

<span data-ttu-id="7a623-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Registrazione**</span><span class="sxs-lookup"><span data-stu-id="7a623-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Recording**</span></span>
</dt> <dd>

<span data-ttu-id="7a623-119">Il trasporto del dispositivo è in uno stato di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7a623-119">The device s transport is in a recording state.</span></span>

</dd> <dt>

<span data-ttu-id="7a623-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span><span class="sxs-lookup"><span data-stu-id="7a623-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span></span>
</dt> <dd>

<span data-ttu-id="7a623-121">Per il trasporto del dispositivo non è impostato un URI per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="7a623-121">The device s transport does not have an URI set for playback.</span></span>

</dd> <dt>

<span data-ttu-id="7a623-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Ultima**</span><span class="sxs-lookup"><span data-stu-id="7a623-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="7a623-123">Stato precedente del dispositivo allo stato del trasporto corrente.</span><span class="sxs-lookup"><span data-stu-id="7a623-123">The device s previous state to the current transport state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a623-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a623-124">Requirements</span></span>



| <span data-ttu-id="7a623-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a623-125">Requirement</span></span> | <span data-ttu-id="7a623-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7a623-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a623-127">IDL</span><span class="sxs-lookup"><span data-stu-id="7a623-127">IDL</span></span><br/> | <dl> <span data-ttu-id="7a623-128"><dt>Windows. Media. streaming. IDL (riferimento a Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="7a623-128"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





