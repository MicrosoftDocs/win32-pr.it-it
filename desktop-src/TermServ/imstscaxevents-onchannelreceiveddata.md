---
title: Metodo IMsTscAxEvents OnChannelReceivedData
description: Chiamato quando il client riceve i dati su un canale virtuale con script.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnChannelReceivedData
- Metodo OnChannelReceivedData Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnChannelReceivedData
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119630"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a><span data-ttu-id="f690c-106">Metodo IMsTscAxEvents:: OnChannelReceivedData</span><span class="sxs-lookup"><span data-stu-id="f690c-106">IMsTscAxEvents::OnChannelReceivedData method</span></span>

<span data-ttu-id="f690c-107">Chiamato quando il client riceve i dati su un canale virtuale con script.</span><span class="sxs-lookup"><span data-stu-id="f690c-107">Called when the client receives data on a scriptable virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="f690c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f690c-108">Syntax</span></span>


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a><span data-ttu-id="f690c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f690c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f690c-110">*channame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f690c-110">*chanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f690c-111">Nome del canale virtuale in cui sono stati ricevuti i dati.</span><span class="sxs-lookup"><span data-stu-id="f690c-111">The name of the virtual channel on which data was received.</span></span> <span data-ttu-id="f690c-112">Questo nome corrisponde a uno dei canali creati dalla chiamata a [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="f690c-112">This name matches one of the channels created by the call to [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="f690c-113">*dati* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f690c-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f690c-114">Dati ricevuti sul canale virtuale con script.</span><span class="sxs-lookup"><span data-stu-id="f690c-114">The data received on the scriptable virtual channel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f690c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f690c-115">Return value</span></span>

<span data-ttu-id="f690c-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f690c-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f690c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f690c-117">Remarks</span></span>

<span data-ttu-id="f690c-118">Per ulteriori informazioni su questo evento, vedere l'articolo relativo all' [implementazione di canali virtuali utilizzabili tramite script con connessione Web Desktop remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) .</span><span class="sxs-lookup"><span data-stu-id="f690c-118">Refer to [Implementing Scriptable Virtual Channels using Remote Desktop Web Connection](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) for more information about this event.</span></span>

<span data-ttu-id="f690c-119">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f690c-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f690c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f690c-120">Requirements</span></span>



| <span data-ttu-id="f690c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f690c-121">Requirement</span></span> | <span data-ttu-id="f690c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f690c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f690c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f690c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f690c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f690c-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f690c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f690c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f690c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f690c-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f690c-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f690c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="f690c-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f690c-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f690c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f690c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f690c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f690c-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f690c-131">IID</span><span class="sxs-lookup"><span data-stu-id="f690c-131">IID</span></span><br/>                      | <span data-ttu-id="f690c-132">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="f690c-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f690c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f690c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f690c-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="f690c-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





