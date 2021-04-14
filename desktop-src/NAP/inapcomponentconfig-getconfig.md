---
title: Metodo GetConfig INapComponentConfig (NapCommon. h)
description: Recupera la configurazione del componente convalida integrità sistema (convalida integrità sistema).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Metodo GetConfig NAP
- Metodo GetConfig NAP, interfaccia INapComponentConfig
- Interfaccia NAP di INapComponentConfig, metodo GetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478443"
---
# <a name="inapcomponentconfiggetconfig-method"></a><span data-ttu-id="ed24d-106">Metodo INapComponentConfig:: GetConfig</span><span class="sxs-lookup"><span data-stu-id="ed24d-106">INapComponentConfig::GetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="ed24d-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed24d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ed24d-108">Il metodo **GetConfig** recupera la configurazione del componente convalida integrità sistema (convalida integrità sistema).</span><span class="sxs-lookup"><span data-stu-id="ed24d-108">The **GetConfig** method retrieves the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed24d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed24d-109">Syntax</span></span>


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a><span data-ttu-id="ed24d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed24d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed24d-111">*bCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed24d-111">*bCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed24d-112">Dimensione, in byte, del BLOB di configurazione *dei dati* .</span><span class="sxs-lookup"><span data-stu-id="ed24d-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="ed24d-113">*dati* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ed24d-113">*data* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed24d-114">Puntatore all'indirizzo dei dati di configurazione del componente di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="ed24d-114">A pointer to the address of the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="ed24d-115">I dati di configurazione esportati da un computer x86 usando il metodo **GetConfig** possono essere importati in un computer x64 usando il metodo [**Seconfig**](inapcomponentconfig-setconfig.md) e viceversa.</span><span class="sxs-lookup"><span data-stu-id="ed24d-115">Configuration data exported from an x86 machine using the **GetConfig** method may be imported onto an x64 machine using the [**SetConfig**](inapcomponentconfig-setconfig.md) method, and vice versa.</span></span> <span data-ttu-id="ed24d-116">Di conseguenza, i dati di configurazione devono essere in un formato indipendente dall'architettura, ad esempio XML.</span><span class="sxs-lookup"><span data-stu-id="ed24d-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="ed24d-117">L'utilizzo di XML anziché di un flusso di byte rende più semplice l'utilizzo dei dati di configurazione in architetture diverse.</span><span class="sxs-lookup"><span data-stu-id="ed24d-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="ed24d-118">Gli elementi XML utilizzati nei dati di configurazione sono determinati dall'implementatore.</span><span class="sxs-lookup"><span data-stu-id="ed24d-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed24d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed24d-119">Return value</span></span>

<span data-ttu-id="ed24d-120">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="ed24d-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="ed24d-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ed24d-121">Return code</span></span>                                                                                     | <span data-ttu-id="ed24d-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed24d-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed24d-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed24d-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ed24d-124">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="ed24d-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="ed24d-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ed24d-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ed24d-126">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ed24d-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ed24d-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ed24d-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ed24d-128">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ed24d-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed24d-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed24d-129">Remarks</span></span>

<span data-ttu-id="ed24d-130">Il parametro data deve essere allocato dal chiamato (implementatore del componente) utilizzando **CoTaskMemAlloc** e liberato dal chiamante utilizzando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="ed24d-130">The data parameter must be allocated by the callee (component implementor) using **CoTaskMemAlloc** and freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed24d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed24d-131">Requirements</span></span>



| <span data-ttu-id="ed24d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed24d-132">Requirement</span></span> | <span data-ttu-id="ed24d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ed24d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed24d-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed24d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ed24d-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ed24d-135">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ed24d-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed24d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ed24d-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed24d-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ed24d-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed24d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed24d-139"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed24d-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed24d-140">IDL</span><span class="sxs-lookup"><span data-stu-id="ed24d-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed24d-141"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed24d-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed24d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed24d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed24d-143">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="ed24d-143">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="ed24d-144">**INapComponentConfig:: Seconfig**</span><span class="sxs-lookup"><span data-stu-id="ed24d-144">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





