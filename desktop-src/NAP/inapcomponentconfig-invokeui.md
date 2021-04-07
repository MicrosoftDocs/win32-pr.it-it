---
title: Metodo INapComponentConfig InvokeUI (NapCommon. h)
description: Avvia un'interfaccia utente personalizzata per un componente del servizio di convalida dell'integrità di sistema (convalida integrità sistema).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- NAP metodo InvokeUI
- Metodo InvokeUI NAP, interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP, metodo InvokeUI
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964016"
---
# <a name="inapcomponentconfiginvokeui-method"></a><span data-ttu-id="0ba28-106">Metodo INapComponentConfig:: InvokeUI</span><span class="sxs-lookup"><span data-stu-id="0ba28-106">INapComponentConfig::InvokeUI method</span></span>

> [!Note]  
> <span data-ttu-id="0ba28-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="0ba28-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0ba28-108">Il metodo **InvokeUI** avvia un'interfaccia utente personalizzata per un componente del servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="0ba28-108">The **InvokeUI** method launches a customized user interface for a system health validator (SHV) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba28-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ba28-109">Syntax</span></span>


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a><span data-ttu-id="0ba28-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ba28-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba28-111">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ba28-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ba28-112">Handle per la finestra padre o proprietario.</span><span class="sxs-lookup"><span data-stu-id="0ba28-112">A handle to the parent or owner window.</span></span> <span data-ttu-id="0ba28-113">È necessario specificare un handle di finestra valido.</span><span class="sxs-lookup"><span data-stu-id="0ba28-113">A valid window handle must be supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba28-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ba28-114">Return value</span></span>

<span data-ttu-id="0ba28-115">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0ba28-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="0ba28-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0ba28-116">Return code</span></span>                                                                                     | <span data-ttu-id="0ba28-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ba28-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba28-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba28-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0ba28-119">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="0ba28-119">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="0ba28-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba28-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0ba28-121">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="0ba28-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0ba28-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba28-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0ba28-123">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0ba28-123">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0ba28-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba28-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>       | <span data-ttu-id="0ba28-125">Il servizio di convalida dell'integrità di sistema non supporta un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0ba28-125">The SHV does not support a customized UI.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="0ba28-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ba28-126">Remarks</span></span>

<span data-ttu-id="0ba28-127">Questa chiamata al metodo deve essere bloccata fino alla chiusura dell'interfaccia utente di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="0ba28-127">This method call should block until the SHV user interface exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba28-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ba28-128">Requirements</span></span>



| <span data-ttu-id="0ba28-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba28-129">Requirement</span></span> | <span data-ttu-id="0ba28-130">Valore</span><span class="sxs-lookup"><span data-stu-id="0ba28-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba28-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ba28-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba28-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0ba28-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0ba28-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ba28-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba28-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ba28-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0ba28-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ba28-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ba28-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba28-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ba28-137">IDL</span><span class="sxs-lookup"><span data-stu-id="0ba28-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ba28-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ba28-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba28-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ba28-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba28-140">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="0ba28-140">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="0ba28-141">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="0ba28-141">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





