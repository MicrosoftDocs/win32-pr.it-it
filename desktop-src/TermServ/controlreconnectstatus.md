---
title: Enumerazione ControlReconnectStatus
description: Specifica il risultato del metodo di riconnessione IMsRdpClient8.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione ControlReconnectStatus
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301132"
---
# <a name="controlreconnectstatus-enumeration"></a><span data-ttu-id="26b96-104">Enumerazione ControlReconnectStatus</span><span class="sxs-lookup"><span data-stu-id="26b96-104">ControlReconnectStatus enumeration</span></span>

<span data-ttu-id="26b96-105">Specifica il risultato del metodo [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="26b96-105">Specifies the result of the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b96-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26b96-106">Syntax</span></span>


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a><span data-ttu-id="26b96-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="26b96-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="26b96-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span><span class="sxs-lookup"><span data-stu-id="26b96-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span></span>
</dt> <dd>

<span data-ttu-id="26b96-109">L'operazione di riconnessione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="26b96-109">The reconnect operation was started.</span></span>

</dd> <dt>

<span data-ttu-id="26b96-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span><span class="sxs-lookup"><span data-stu-id="26b96-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span></span>
</dt> <dd>

<span data-ttu-id="26b96-111">Non è stato possibile avviare l'operazione di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="26b96-111">The reconnect operation could not be started.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26b96-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26b96-112">Requirements</span></span>



| <span data-ttu-id="26b96-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b96-113">Requirement</span></span> | <span data-ttu-id="26b96-114">Valore</span><span class="sxs-lookup"><span data-stu-id="26b96-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26b96-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26b96-115">Minimum supported client</span></span><br/> | <span data-ttu-id="26b96-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="26b96-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="26b96-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26b96-117">Minimum supported server</span></span><br/> | <span data-ttu-id="26b96-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26b96-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="26b96-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="26b96-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="26b96-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26b96-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b96-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26b96-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b96-122">**IMsRdpClient8:: Reconnect**</span><span class="sxs-lookup"><span data-stu-id="26b96-122">**IMsRdpClient8::Reconnect**</span></span>](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





