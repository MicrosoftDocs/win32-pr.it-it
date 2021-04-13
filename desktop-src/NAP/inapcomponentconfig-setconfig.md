---
title: Metodo Seconfig INapComponentConfig (NapCommon. h)
description: Imposta la configurazione del componente convalida integrità sistema (convalida integrità sistema).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Metodo di configurazione NAP
- Metodo di configurazione NAP, interfaccia INapComponentConfig
- Interfaccia INapComponentConfig NAP, metodo Seconfig
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519285"
---
# <a name="inapcomponentconfigsetconfig-method"></a><span data-ttu-id="82403-106">Metodo INapComponentConfig:: Seconfig</span><span class="sxs-lookup"><span data-stu-id="82403-106">INapComponentConfig::SetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="82403-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="82403-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="82403-108">Il metodo **Seconfig** imposta la configurazione del componente convalida integrità sistema (convalida integrità sistema).</span><span class="sxs-lookup"><span data-stu-id="82403-108">The **SetConfig** method sets the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="82403-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82403-109">Syntax</span></span>


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="82403-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="82403-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82403-111">*bCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82403-111">*bCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82403-112">Dimensione, in byte, del BLOB di configurazione *dei dati* .</span><span class="sxs-lookup"><span data-stu-id="82403-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="82403-113">*dati* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="82403-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82403-114">Puntatore ai dati di configurazione del componente di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="82403-114">A pointer to the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="82403-115">I dati di configurazione esportati da un computer x86 usando il metodo [**GetConfig**](inapcomponentconfig-getconfig.md) possono essere importati in un computer x64 usando il metodo **Seconfig** e viceversa.</span><span class="sxs-lookup"><span data-stu-id="82403-115">Configuration data exported from an x86 machine using the [**GetConfig**](inapcomponentconfig-getconfig.md) method may be imported onto an x64 machine using the **SetConfig** method, and vice versa.</span></span> <span data-ttu-id="82403-116">Di conseguenza, i dati di configurazione devono essere in un formato indipendente dall'architettura, ad esempio XML.</span><span class="sxs-lookup"><span data-stu-id="82403-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="82403-117">L'utilizzo di XML anziché di un flusso di byte rende più semplice l'utilizzo dei dati di configurazione in architetture diverse.</span><span class="sxs-lookup"><span data-stu-id="82403-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="82403-118">Gli elementi XML utilizzati nei dati di configurazione sono determinati dall'implementatore.</span><span class="sxs-lookup"><span data-stu-id="82403-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82403-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82403-119">Return value</span></span>

<span data-ttu-id="82403-120">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="82403-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="82403-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="82403-121">Return code</span></span>                                                                                     | <span data-ttu-id="82403-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82403-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="82403-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82403-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="82403-124">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="82403-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="82403-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="82403-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="82403-126">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="82403-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="82403-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82403-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="82403-128">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="82403-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="82403-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="82403-129">Remarks</span></span>

<span data-ttu-id="82403-130">Le informazioni sul controllo delle versioni dei componenti devono essere incluse nel BLOB di configurazione *dati* .</span><span class="sxs-lookup"><span data-stu-id="82403-130">Component versioning information should be included in the *data* configuration blob.</span></span> <span data-ttu-id="82403-131">Le informazioni sul controllo delle versioni possono essere utilizzate durante la migrazione da una versione di convalida integrità di sistema a un'altra.</span><span class="sxs-lookup"><span data-stu-id="82403-131">The versioning information may be used when migrating from one SHV version to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="82403-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82403-132">Requirements</span></span>



| <span data-ttu-id="82403-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="82403-133">Requirement</span></span> | <span data-ttu-id="82403-134">Valore</span><span class="sxs-lookup"><span data-stu-id="82403-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82403-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82403-135">Minimum supported client</span></span><br/> | <span data-ttu-id="82403-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="82403-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="82403-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82403-137">Minimum supported server</span></span><br/> | <span data-ttu-id="82403-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82403-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="82403-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82403-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="82403-140"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82403-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="82403-141">IDL</span><span class="sxs-lookup"><span data-stu-id="82403-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82403-142"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82403-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82403-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82403-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82403-144">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="82403-144">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="82403-145">**INapConponentConfig:: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="82403-145">**INapConponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





