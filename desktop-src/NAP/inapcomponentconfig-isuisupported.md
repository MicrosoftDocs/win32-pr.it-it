---
title: Metodo INapComponentConfig IsUISupported (NapCommon. h)
description: Specifica se il componente supporta un'interfaccia utente personalizzata.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- NAP metodo IsUISupported
- Metodo IsUISupported NAP, interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP, metodo IsUISupported
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301582"
---
# <a name="inapcomponentconfigisuisupported-method"></a><span data-ttu-id="d0438-106">Metodo INapComponentConfig:: IsUISupported</span><span class="sxs-lookup"><span data-stu-id="d0438-106">INapComponentConfig::IsUISupported method</span></span>

> [!Note]  
> <span data-ttu-id="d0438-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="d0438-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d0438-108">Il metodo **IsUISupported** specifica se il componente supporta un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d0438-108">The **IsUISupported** method specifies whether the component supports a customized user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0438-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0438-109">Syntax</span></span>


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a><span data-ttu-id="d0438-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0438-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0438-111">*supportato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d0438-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0438-112">Puntatore a un BOOL che è impostato su **true** se il componente supporta un'interfaccia utente personalizzata e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d0438-112">A pointer to a BOOL that is set to **TRUE** if the component supports a customized user interface and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0438-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0438-113">Return value</span></span>

<span data-ttu-id="d0438-114">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="d0438-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="d0438-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d0438-115">Return code</span></span>                                                                                     | <span data-ttu-id="d0438-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0438-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d0438-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d0438-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d0438-118">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="d0438-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="d0438-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d0438-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d0438-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d0438-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d0438-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d0438-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d0438-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d0438-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0438-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0438-123">Remarks</span></span>

<span data-ttu-id="d0438-124">L'interfaccia utente personalizzata di un componente deve essere avviata con [**INapComponentConfig:: InvokeUI**](inapcomponentconfig-invokeui.md).</span><span class="sxs-lookup"><span data-stu-id="d0438-124">A component's customized user interface should be launched using [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0438-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0438-125">Requirements</span></span>



| <span data-ttu-id="d0438-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0438-126">Requirement</span></span> | <span data-ttu-id="d0438-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d0438-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0438-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0438-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d0438-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d0438-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d0438-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0438-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d0438-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0438-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d0438-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0438-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0438-133"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0438-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0438-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d0438-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d0438-135"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d0438-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0438-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0438-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0438-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="d0438-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="d0438-138">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="d0438-138">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





