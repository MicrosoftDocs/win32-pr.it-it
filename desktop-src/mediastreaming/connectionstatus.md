---
title: Enumerazione ConnectionStatus
description: Rappresenta lo stato del dispositivo nella rete come l'ultima volta.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- API di streaming multimediale dell'enumerazione ConnectionStatus
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328370"
---
# <a name="connectionstatus-enumeration"></a><span data-ttu-id="d163a-104">Enumerazione ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="d163a-104">ConnectionStatus enumeration</span></span>

<span data-ttu-id="d163a-105">Rappresenta lo stato del dispositivo nella rete come l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="d163a-105">Represents the state of the device in the network as last seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="d163a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d163a-106">Syntax</span></span>


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a><span data-ttu-id="d163a-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="d163a-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d163a-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**</span><span class="sxs-lookup"><span data-stu-id="d163a-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**</span></span>
</dt> <dd>

<span data-ttu-id="d163a-109">Il dispositivo è online e attivo sulla rete.</span><span class="sxs-lookup"><span data-stu-id="d163a-109">Device is online and active on the network.</span></span>

</dd> <dt>

<span data-ttu-id="d163a-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**</span><span class="sxs-lookup"><span data-stu-id="d163a-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**</span></span>
</dt> <dd>

<span data-ttu-id="d163a-111">Il dispositivo è offline.</span><span class="sxs-lookup"><span data-stu-id="d163a-111">Device is offline.</span></span>

</dd> <dt>

<span data-ttu-id="d163a-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**In sospensione**</span><span class="sxs-lookup"><span data-stu-id="d163a-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Sleeping**</span></span>
</dt> <dd>

<span data-ttu-id="d163a-113">Il dispositivo è attualmente offline ma potrebbe essere riattivato automaticamente quando viene effettuato un tentativo di comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="d163a-113">Device is currently offline but might automatically wake up when an attempt is made to communicate with it.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d163a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d163a-114">Requirements</span></span>



| <span data-ttu-id="d163a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d163a-115">Requirement</span></span> | <span data-ttu-id="d163a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d163a-116">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d163a-117">IDL</span><span class="sxs-lookup"><span data-stu-id="d163a-117">IDL</span></span><br/> | <dl> <span data-ttu-id="d163a-118"><dt>Windows. Media. streaming. IDL (riferimento a Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="d163a-118"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





