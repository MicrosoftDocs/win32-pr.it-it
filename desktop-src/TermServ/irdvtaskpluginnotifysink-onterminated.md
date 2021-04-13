---
title: Metodo onterminated IRDVTaskPluginNotifySink (Sbtsv. h)
description: Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo onterminated
- Servizi Desktop remoto metodo onterminated, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, metodo onterminated
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518934"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a><span data-ttu-id="db23d-106">Metodo IRDVTaskPluginNotifySink:: onTerminate</span><span class="sxs-lookup"><span data-stu-id="db23d-106">IRDVTaskPluginNotifySink::OnTerminated method</span></span>

<span data-ttu-id="db23d-107">Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="db23d-107">Called by the task agent to request that the task agent be shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="db23d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db23d-108">Syntax</span></span>


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="db23d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="db23d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db23d-110">*risorse umane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db23d-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db23d-111">Indica se l'arresto è dovuto a un arresto normale o a un errore.</span><span class="sxs-lookup"><span data-stu-id="db23d-111">Indicates if the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="db23d-112">Se l'arresto è normale, questo contiene **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db23d-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="db23d-113">In caso contrario, contiene un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db23d-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db23d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db23d-114">Return value</span></span>

<span data-ttu-id="db23d-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db23d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db23d-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db23d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db23d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db23d-117">Requirements</span></span>



| <span data-ttu-id="db23d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="db23d-118">Requirement</span></span> | <span data-ttu-id="db23d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="db23d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db23d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db23d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db23d-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="db23d-121">Windows 7 Enterprise</span></span><br/>                                                    |
| <span data-ttu-id="db23d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db23d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db23d-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db23d-123">Windows Server 2008 R2</span></span><br/>                                                  |
| <span data-ttu-id="db23d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db23d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db23d-125"><dt>Sbtsv. h</dt></span><span class="sxs-lookup"><span data-stu-id="db23d-125"><dt>Sbtsv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db23d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db23d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db23d-127">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="db23d-127">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





