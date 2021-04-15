---
title: Metodo Initialize IRDVTaskPlugin
description: Chiamato per inizializzare l'agente attività.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Inizializzare il metodo Servizi Desktop remoto
- Metodo Initialize Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, metodo Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400373"
---
# <a name="irdvtaskplugininitialize-method"></a><span data-ttu-id="cfe8c-106">Metodo IRDVTaskPlugin:: Initialize</span><span class="sxs-lookup"><span data-stu-id="cfe8c-106">IRDVTaskPlugin::Initialize method</span></span>

<span data-ttu-id="cfe8c-107">Chiamato per inizializzare l'agente attività.</span><span class="sxs-lookup"><span data-stu-id="cfe8c-107">Called to initialize the task agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe8c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfe8c-108">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a><span data-ttu-id="cfe8c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfe8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe8c-110">*pNotifySink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfe8c-110">*pNotifySink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe8c-111">Tipo: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _</span><span class="sxs-lookup"><span data-stu-id="cfe8c-111">Type: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\** _</span></span>

<span data-ttu-id="cfe8c-112">Puntatore a un'interfaccia [_ *IRDVTaskPluginNotifySink* \*](irdvtaskpluginnotifysink.md) che l'agente attività utilizza per comunicare con l'agente di trigger.</span><span class="sxs-lookup"><span data-stu-id="cfe8c-112">A pointer to an [_ *IRDVTaskPluginNotifySink*\*](irdvtaskpluginnotifysink.md) interface that the task agent uses to communicate with the trigger agent.</span></span> <span data-ttu-id="cfe8c-113">È necessario rilasciare questa interfaccia quando non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="cfe8c-113">You must release this interface when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe8c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfe8c-114">Return value</span></span>

<span data-ttu-id="cfe8c-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cfe8c-115">Type: **HRESULT**</span></span>

<span data-ttu-id="cfe8c-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cfe8c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cfe8c-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cfe8c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe8c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfe8c-118">Requirements</span></span>



| <span data-ttu-id="cfe8c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe8c-119">Requirement</span></span> | <span data-ttu-id="cfe8c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cfe8c-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="cfe8c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfe8c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe8c-122">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="cfe8c-122">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="cfe8c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfe8c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe8c-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfe8c-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfe8c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfe8c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe8c-126">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="cfe8c-126">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





