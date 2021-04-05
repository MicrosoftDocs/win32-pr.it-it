---
title: Metodo IMsTscAxEvents OnServiceMessageReceived
description: Chiamato quando il client riceve un messaggio di sistema.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnServiceMessageReceived
- Metodo OnServiceMessageReceived Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnServiceMessageReceived
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742090"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a><span data-ttu-id="68529-106">Metodo IMsTscAxEvents:: OnServiceMessageReceived</span><span class="sxs-lookup"><span data-stu-id="68529-106">IMsTscAxEvents::OnServiceMessageReceived method</span></span>

<span data-ttu-id="68529-107">Chiamato quando il client riceve un messaggio di sistema.</span><span class="sxs-lookup"><span data-stu-id="68529-107">Called when the client receives a system message.</span></span>

## <a name="syntax"></a><span data-ttu-id="68529-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68529-108">Syntax</span></span>


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a><span data-ttu-id="68529-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="68529-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68529-110">*serviceMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68529-110">*serviceMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68529-111">Specifica il messaggio di sistema.</span><span class="sxs-lookup"><span data-stu-id="68529-111">Specifies the system message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68529-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68529-112">Return value</span></span>

<span data-ttu-id="68529-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="68529-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68529-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="68529-114">Remarks</span></span>

<span data-ttu-id="68529-115">Per ulteriori informazioni sui messaggi di sistema, vedere [configurare la messaggistica per un server Gateway Desktop remoto](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="68529-115">For more information about system messages, see [Configure Messaging for a Remote Desktop Gateway Server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span></span>

## <a name="requirements"></a><span data-ttu-id="68529-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68529-116">Requirements</span></span>



| <span data-ttu-id="68529-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="68529-117">Requirement</span></span> | <span data-ttu-id="68529-118">Valore</span><span class="sxs-lookup"><span data-stu-id="68529-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68529-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68529-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68529-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="68529-120">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="68529-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68529-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68529-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68529-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="68529-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="68529-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="68529-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68529-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68529-125">DLL</span><span class="sxs-lookup"><span data-stu-id="68529-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68529-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68529-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68529-127">IID</span><span class="sxs-lookup"><span data-stu-id="68529-127">IID</span></span><br/>                      | <span data-ttu-id="68529-128">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="68529-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="68529-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68529-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68529-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="68529-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

