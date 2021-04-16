---
title: Metodo INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient. h)
description: Utilizzato dall'agente NAP per eseguire una query sui validator di integrità di sistema installati (SHV) nel client.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- NAP metodo GetInstalledShvs
- Metodo GetInstalledShvs NAP, interfaccia INapEnforcementClientConnection2
- Interfaccia INapEnforcementClientConnection2 NAP, metodo GetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479355"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a><span data-ttu-id="b10e5-106">Metodo INapEnforcementClientConnection2:: GetInstalledShvs</span><span class="sxs-lookup"><span data-stu-id="b10e5-106">INapEnforcementClientConnection2::GetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="b10e5-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="b10e5-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b10e5-108">Il metodo **GetInstalledShvs** viene utilizzato dall'agente NAP per eseguire una query sui validator di integrità del sistema installati (SHV) nel client.</span><span class="sxs-lookup"><span data-stu-id="b10e5-108">The **GetInstalledShvs** method is used by the NAP Agent to query the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="b10e5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b10e5-109">Syntax</span></span>


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a><span data-ttu-id="b10e5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b10e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b10e5-111">*numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="b10e5-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b10e5-112">Puntatore a un valore [SystemHealthEntityCount](nap-datatypes.md) che specifica il numero di SHV installati negli *ID*.</span><span class="sxs-lookup"><span data-stu-id="b10e5-112">A pointer to a [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of installed SHVs in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="b10e5-113">*ID* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="b10e5-113">*ids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b10e5-114">Puntatore a una matrice di valori [SystemHealthEntityId](nap-datatypes.md) che contengono gli ID di convalida integrità di sistema installati.</span><span class="sxs-lookup"><span data-stu-id="b10e5-114">A pointer to an array of [SystemHealthEntityId](nap-datatypes.md) values that contain the installed SHV IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b10e5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b10e5-115">Return value</span></span>

<span data-ttu-id="b10e5-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="b10e5-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b10e5-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b10e5-117">Return code</span></span>                                                                                   | <span data-ttu-id="b10e5-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b10e5-118">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="b10e5-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b10e5-119"><dt>**S\_OK** </dt></span></span> </dl>         | <span data-ttu-id="b10e5-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b10e5-120">Operation succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="b10e5-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b10e5-121"><dt>**E\_INVALIDARG** </dt></span></span> </dl> | <span data-ttu-id="b10e5-122">Un argomento non valido è stato passato al metodo.</span><span class="sxs-lookup"><span data-stu-id="b10e5-122">An invalid argument was passed to the method.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b10e5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b10e5-123">Requirements</span></span>



| <span data-ttu-id="b10e5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b10e5-124">Requirement</span></span> | <span data-ttu-id="b10e5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b10e5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b10e5-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b10e5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b10e5-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b10e5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b10e5-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b10e5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b10e5-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b10e5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b10e5-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b10e5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b10e5-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b10e5-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b10e5-132">IDL</span><span class="sxs-lookup"><span data-stu-id="b10e5-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b10e5-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b10e5-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="b10e5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b10e5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b10e5-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b10e5-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b10e5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b10e5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b10e5-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="b10e5-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





