---
title: Metodo IMsRdpClient8 SendRemoteAction
description: Comporta l'esecuzione di un'azione nella sessione remota.
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendRemoteAction
- Metodo SendRemoteAction Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo SendRemoteAction
- Metodo SendRemoteAction Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo SendRemoteAction
- Metodo SendRemoteAction Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo SendRemoteAction
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28fc9695686402e0a8e98ed17fc1bc6a47939d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479301"
---
# <a name="imsrdpclient8sendremoteaction-method"></a><span data-ttu-id="a7eae-110">Metodo IMsRdpClient8:: SendRemoteAction</span><span class="sxs-lookup"><span data-stu-id="a7eae-110">IMsRdpClient8::SendRemoteAction method</span></span>

<span data-ttu-id="a7eae-111">Comporta l'esecuzione di un'azione nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="a7eae-111">Causes an action to be performed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7eae-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7eae-112">Syntax</span></span>


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a><span data-ttu-id="a7eae-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7eae-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7eae-114">*ActionType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7eae-114">*actionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7eae-115">Valore dell'enumerazione [**RemoteSessionActionType**](remotesessionactiontype.md) che specifica l'azione da inviare alla sessione remota.</span><span class="sxs-lookup"><span data-stu-id="a7eae-115">A value of the [**RemoteSessionActionType**](remotesessionactiontype.md) enumeration that specifies the action to send to the remote session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7eae-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7eae-116">Return value</span></span>

<span data-ttu-id="a7eae-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a7eae-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7eae-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7eae-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7eae-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7eae-119">Requirements</span></span>



| <span data-ttu-id="a7eae-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7eae-120">Requirement</span></span> | <span data-ttu-id="a7eae-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a7eae-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7eae-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7eae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a7eae-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a7eae-123">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="a7eae-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7eae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a7eae-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7eae-125">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="a7eae-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a7eae-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7eae-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7eae-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7eae-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a7eae-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7eae-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7eae-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7eae-130">IID</span><span class="sxs-lookup"><span data-stu-id="a7eae-130">IID</span></span><br/>                      | <span data-ttu-id="a7eae-131">IID \_ IMsRdpClient8 è definito come 4247E044-9271-43a9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="a7eae-131">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a7eae-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7eae-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7eae-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a7eae-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a7eae-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a7eae-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a7eae-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a7eae-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





