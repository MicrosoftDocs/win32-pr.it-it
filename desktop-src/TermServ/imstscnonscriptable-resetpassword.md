---
title: Metodo IMsTscNonScriptable ResetPassword
description: Reimposta tutti gli Stati delle password nel controllo ActiveX Desktop remoto.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ResetPassword
- Metodo ResetPassword Servizi Desktop remoto, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, metodo ResetPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478881"
---
# <a name="imstscnonscriptableresetpassword-method"></a><span data-ttu-id="16a66-106">Metodo IMsTscNonScriptable:: ResetPassword</span><span class="sxs-lookup"><span data-stu-id="16a66-106">IMsTscNonScriptable::ResetPassword method</span></span>

<span data-ttu-id="16a66-107">Reimposta tutti gli Stati delle password nel controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="16a66-107">Resets all password states in the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="16a66-108">È possibile chiamare questo metodo per cancellare le password archiviate in uno dei tre formati supportati, ovvero testo non crittografato, codificato portatile o binario (non portabile) codificato.</span><span class="sxs-lookup"><span data-stu-id="16a66-108">You can call this method to clear passwords that are stored in any one of the three supported formats: plaintext, portable encoded, or binary (nonportable) encoded.</span></span> <span data-ttu-id="16a66-109">Si noti che le password codificate non devono essere considerate crittografate in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="16a66-109">Note that encoded passwords should not be considered securely encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a66-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16a66-110">Syntax</span></span>


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a><span data-ttu-id="16a66-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="16a66-111">Parameters</span></span>

<span data-ttu-id="16a66-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="16a66-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16a66-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16a66-113">Return value</span></span>

<span data-ttu-id="16a66-114">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="16a66-114">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="16a66-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="16a66-115">Remarks</span></span>

<span data-ttu-id="16a66-116">È possibile chiamare questo metodo per reimpostare la password del controllo dopo la disconnessione.</span><span class="sxs-lookup"><span data-stu-id="16a66-116">You can call this method to reset the control's password after disconnecting.</span></span> <span data-ttu-id="16a66-117">Ciò garantisce che le connessioni successive che usano la stessa istanza del controllo non accedano automaticamente con una password impostata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="16a66-117">This ensures that subsequent connections that use the same instance of the control do not automatically log on with a previously set password.</span></span>

<span data-ttu-id="16a66-118">È possibile chiamare questo metodo solo quando il Desktop remoto controllo ActiveX non si trova nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="16a66-118">You can only call this method when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="16a66-119">Questo metodo restituisce **E ha \_ esito negativo** se viene chiamato quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="16a66-119">This method returns **E\_FAIL** if called when the control is connected.</span></span> <span data-ttu-id="16a66-120">Per verificare lo stato connesso, chiamare il metodo [**get \_ Connected**](imstscax-connected.md) tramite l'interfaccia [**IMsTscAx**](imstscax-interface.md) o una delle interfacce che ereditano da esso.</span><span class="sxs-lookup"><span data-stu-id="16a66-120">To check for the connected state, call the [**get\_Connected**](imstscax-connected.md) method through the [**IMsTscAx**](imstscax-interface.md) interface or one of the interfaces that inherits from it.</span></span>

<span data-ttu-id="16a66-121">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="16a66-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16a66-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16a66-122">Requirements</span></span>



| <span data-ttu-id="16a66-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="16a66-123">Requirement</span></span> | <span data-ttu-id="16a66-124">Valore</span><span class="sxs-lookup"><span data-stu-id="16a66-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16a66-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16a66-125">Minimum supported client</span></span><br/> | <span data-ttu-id="16a66-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16a66-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="16a66-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16a66-127">Minimum supported server</span></span><br/> | <span data-ttu-id="16a66-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16a66-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="16a66-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="16a66-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="16a66-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16a66-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="16a66-131">DLL</span><span class="sxs-lookup"><span data-stu-id="16a66-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16a66-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16a66-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="16a66-133">IID</span><span class="sxs-lookup"><span data-stu-id="16a66-133">IID</span></span><br/>                      | <span data-ttu-id="16a66-134">IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="16a66-134">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16a66-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16a66-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a66-136">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="16a66-136">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





