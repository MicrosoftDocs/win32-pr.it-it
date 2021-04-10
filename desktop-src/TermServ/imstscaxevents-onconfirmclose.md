---
title: Metodo IMsTscAxEvents OnConfirmClose
description: Chiamato quando il client chiama il Metodo RequestClose di IMsRdpClient.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnConfirmClose
- Metodo OnConfirmClose Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnConfirmClose
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121642"
---
# <a name="imstscaxeventsonconfirmclose-method"></a><span data-ttu-id="55a51-106">Metodo IMsTscAxEvents:: OnConfirmClose</span><span class="sxs-lookup"><span data-stu-id="55a51-106">IMsTscAxEvents::OnConfirmClose method</span></span>

<span data-ttu-id="55a51-107">Chiamato quando il client chiama il metodo [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) .</span><span class="sxs-lookup"><span data-stu-id="55a51-107">Called when the client calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method.</span></span> <span data-ttu-id="55a51-108">In risposta a questo evento, all'utente viene richiesto di confermare la chiusura della connessione.</span><span class="sxs-lookup"><span data-stu-id="55a51-108">In response to this event, the user should be prompted to confirm closing the connection.</span></span> <span data-ttu-id="55a51-109">Per ulteriori informazioni, vedere la sezione Osservazioni successiva.</span><span class="sxs-lookup"><span data-stu-id="55a51-109">For more information, see the following Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a51-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55a51-110">Syntax</span></span>


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a><span data-ttu-id="55a51-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="55a51-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a51-112">*pfAllowClose* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="55a51-112">*pfAllowClose* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55a51-113">Se **Variant \_ true**, il valore predefinito indica che l'utente desidera chiudere la connessione.</span><span class="sxs-lookup"><span data-stu-id="55a51-113">If **VARIANT\_TRUE**, the default, indicates that the user wants to close the connection.</span></span> <span data-ttu-id="55a51-114">Se **Variant \_ false** indica che l'utente non desidera chiudere la connessione.</span><span class="sxs-lookup"><span data-stu-id="55a51-114">If **VARIANT\_FALSE**, indicates that the user does not want to close the connection.</span></span> <span data-ttu-id="55a51-115">Per ulteriori informazioni, vedere la sezione Osservazioni successiva.</span><span class="sxs-lookup"><span data-stu-id="55a51-115">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a51-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55a51-116">Return value</span></span>

<span data-ttu-id="55a51-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="55a51-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55a51-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="55a51-118">Remarks</span></span>

<span data-ttu-id="55a51-119">Quando un'applicazione contenitore chiama il metodo [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) , il metodo restituisce un valore che indica se il contenitore deve attendere che si verifichi un evento **OnConfirmClose** prima di chiudere la connessione al controllo.</span><span class="sxs-lookup"><span data-stu-id="55a51-119">When a container application calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method, that method returns a value indicating whether the container should wait for an **OnConfirmClose** event to occur before closing the control connection.</span></span> <span data-ttu-id="55a51-120">Se **RequestClose** restituisce **controlCloseWaitForEvents** e l'utente è connesso e connesso alla sessione di Servizi Desktop remoto, viene generato l'evento **OnConfirmClose** .</span><span class="sxs-lookup"><span data-stu-id="55a51-120">If **RequestClose** returns **controlCloseWaitForEvents**, and the user is connected and logged on to their Remote Desktop Services session, the **OnConfirmClose** event fires.</span></span> <span data-ttu-id="55a51-121">A questo punto l'applicazione contenitore può richiedere conferma all'utente, chiedendo se l'utente desidera chiudere la connessione.</span><span class="sxs-lookup"><span data-stu-id="55a51-121">At that point the container application can prompt the user, asking whether the user wants to close the connection.</span></span> <span data-ttu-id="55a51-122">Se l'utente desidera chiudere la connessione, l'applicazione deve impostare il parametro *pfAllowClose* su **Variant \_ true** e procedere alla chiusura della connessione.</span><span class="sxs-lookup"><span data-stu-id="55a51-122">If the user wants to close the connection, the application should set the *pfAllowClose* parameter to **VARIANT\_TRUE** and proceed with closing the connection.</span></span> <span data-ttu-id="55a51-123">Se l'utente non desidera chiudere, l'applicazione deve impostare *pfAllowClose* su **Variant \_ false** e lasciare aperta la connessione.</span><span class="sxs-lookup"><span data-stu-id="55a51-123">If the user does not want to close, the application should set *pfAllowClose* to **VARIANT\_FALSE** and leave the connection open.</span></span>

<span data-ttu-id="55a51-124">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="55a51-124">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55a51-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55a51-125">Requirements</span></span>



| <span data-ttu-id="55a51-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="55a51-126">Requirement</span></span> | <span data-ttu-id="55a51-127">Valore</span><span class="sxs-lookup"><span data-stu-id="55a51-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55a51-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55a51-128">Minimum supported client</span></span><br/> | <span data-ttu-id="55a51-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55a51-129">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="55a51-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55a51-130">Minimum supported server</span></span><br/> | <span data-ttu-id="55a51-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55a51-131">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="55a51-132">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="55a51-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="55a51-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a51-133"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="55a51-134">DLL</span><span class="sxs-lookup"><span data-stu-id="55a51-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a51-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a51-135"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="55a51-136">IID</span><span class="sxs-lookup"><span data-stu-id="55a51-136">IID</span></span><br/>                      | <span data-ttu-id="55a51-137">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="55a51-137">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="55a51-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55a51-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a51-139">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="55a51-139">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





