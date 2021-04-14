---
title: Metodo Terminate IRDVTaskPlugin
description: Chiamato quando l'agente attività viene arrestato.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Termina il metodo Servizi Desktop remoto
- Metodo Terminate Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, metodo Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400731"
---
# <a name="irdvtaskpluginterminate-method"></a><span data-ttu-id="80e1c-106">Metodo IRDVTaskPlugin:: terminate</span><span class="sxs-lookup"><span data-stu-id="80e1c-106">IRDVTaskPlugin::Terminate method</span></span>

<span data-ttu-id="80e1c-107">Chiamato quando l'agente attività viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="80e1c-107">Called when the task agent is being shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e1c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80e1c-108">Syntax</span></span>


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="80e1c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="80e1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e1c-110">*risorse umane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80e1c-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e1c-111">Indica se l'arresto è dovuto a un arresto normale o a un errore.</span><span class="sxs-lookup"><span data-stu-id="80e1c-111">Indicates whether the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="80e1c-112">Se l'arresto è normale, questo contiene **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="80e1c-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="80e1c-113">In caso contrario, contiene un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80e1c-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e1c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80e1c-114">Return value</span></span>

<span data-ttu-id="80e1c-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="80e1c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80e1c-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80e1c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e1c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80e1c-117">Requirements</span></span>



| <span data-ttu-id="80e1c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e1c-118">Requirement</span></span> | <span data-ttu-id="80e1c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="80e1c-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="80e1c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80e1c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="80e1c-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="80e1c-121">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="80e1c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80e1c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="80e1c-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80e1c-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80e1c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80e1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e1c-125">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="80e1c-125">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





