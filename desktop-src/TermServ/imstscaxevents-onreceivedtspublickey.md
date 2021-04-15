---
title: Metodo IMsTscAxEvents OnReceivedTSPublicKey
description: Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server. Questo evento viene chiamato solo se la proprietà NotifyTSPublicKey è VARIANT \_ true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnReceivedTSPublicKey
- Metodo OnReceivedTSPublicKey Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnReceivedTSPublicKey
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477434"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a><span data-ttu-id="bf8c0-107">Metodo IMsTscAxEvents:: OnReceivedTSPublicKey</span><span class="sxs-lookup"><span data-stu-id="bf8c0-107">IMsTscAxEvents::OnReceivedTSPublicKey method</span></span>

<span data-ttu-id="bf8c0-108">Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-108">Called during the connection sequence when the client retrieves the public key from the server.</span></span> <span data-ttu-id="bf8c0-109">Questo evento viene chiamato solo se la proprietà **NotifyTSPublicKey** è **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-109">This event is only called if the **NotifyTSPublicKey** property is **VARIANT\_TRUE**.</span></span> <span data-ttu-id="bf8c0-110">Questa operazione è successiva alla [**connessione**](imstscaxevents-onconnecting.md), ma prima di [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) e [**OnConnected**](imstscaxevents-onconnected.md).</span><span class="sxs-lookup"><span data-stu-id="bf8c0-110">This is after [**OnConnecting**](imstscaxevents-onconnecting.md), but before [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) and [**OnConnected**](imstscaxevents-onconnected.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf8c0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf8c0-111">Syntax</span></span>


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a><span data-ttu-id="bf8c0-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf8c0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf8c0-113">*publicKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf8c0-113">*publicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8c0-114">Contiene la chiave pubblica del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-114">Contains the public key of the remote machine.</span></span>

</dd> <dt>

<span data-ttu-id="bf8c0-115">*pfContinueLogon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bf8c0-115">*pfContinueLogon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8c0-116">Puntatore a una variabile **\_ bool Variant** che riceve se il processo di accesso deve continuare.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-116">A pointer to a **VARIANT\_BOOL** variable that receives whether the logon process should continue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf8c0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf8c0-117">Return value</span></span>

<span data-ttu-id="bf8c0-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bf8c0-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8c0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf8c0-119">Remarks</span></span>

<span data-ttu-id="bf8c0-120">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bf8c0-120">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf8c0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf8c0-121">Requirements</span></span>



| <span data-ttu-id="bf8c0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf8c0-122">Requirement</span></span> | <span data-ttu-id="bf8c0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bf8c0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8c0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf8c0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bf8c0-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf8c0-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bf8c0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf8c0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bf8c0-127">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="bf8c0-127">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="bf8c0-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bf8c0-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf8c0-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf8c0-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf8c0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bf8c0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf8c0-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf8c0-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf8c0-132">IID</span><span class="sxs-lookup"><span data-stu-id="bf8c0-132">IID</span></span><br/>                      | <span data-ttu-id="bf8c0-133">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="bf8c0-133">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bf8c0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf8c0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8c0-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="bf8c0-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





