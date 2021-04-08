---
title: Metodo INapComponentConfig3 GetConfigFromID (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per ottenere i dati di configurazione per un ID configurazione specifico.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- NAP metodo GetConfigFromID
- Metodo GetConfigFromID NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740938"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a><span data-ttu-id="8b5cf-106">Metodo INapComponentConfig3:: GetConfigFromID</span><span class="sxs-lookup"><span data-stu-id="8b5cf-106">INapComponentConfig3::GetConfigFromID method</span></span>

> [!Note]  
> <span data-ttu-id="8b5cf-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8b5cf-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8b5cf-108">Il metodo **GetConfigFromID** viene implementato da convalida integrità sistema (SHV) per fornire un modo per ottenere i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-108">The **GetConfigFromID** method is implemented by system health validators (SHVs) to provide a way to obtain configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5cf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b5cf-109">Syntax</span></span>


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a><span data-ttu-id="8b5cf-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b5cf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b5cf-111">*configID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b5cf-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5cf-112">Valore che rappresenta la configurazione.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-112">A value that represents the configuration.</span></span> <span data-ttu-id="8b5cf-113">Se *ConfigID* è **0**, il servizio di convalida dell'integrità di sistema deve restituire i dati di configurazione predefiniti in *OutData*.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-113">If *ConfigID* is **0**, the SHV should return the default configuration data in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="8b5cf-114">*numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8b5cf-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5cf-115">Dimensione, in byte, dei dati di configurazione restituiti in *OutData*.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-115">The size, in bytes, of the configuration data returned in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="8b5cf-116">*dati OutData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b5cf-116">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b5cf-117">Al ritorno, matrice di BYTE che contiene i dati di configurazione rappresentati da *ConfigID*.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-117">On return, a BYTE array that contains the configuration data represented by *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b5cf-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b5cf-118">Return value</span></span>

<span data-ttu-id="8b5cf-119">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-119">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="8b5cf-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8b5cf-120">Return code</span></span>                                                                                                    | <span data-ttu-id="8b5cf-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b5cf-121">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="8b5cf-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b5cf-122"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="8b5cf-123">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-123">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="8b5cf-124"><dt>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ non \_ trovata**</dt></span><span class="sxs-lookup"><span data-stu-id="8b5cf-124"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="8b5cf-125">*ConfigID* non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-125">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="8b5cf-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b5cf-126">Remarks</span></span>

<span data-ttu-id="8b5cf-127">Il metodo [**NewConfig**](inapcomponentconfig3-newconfig.md) deve essere usato per allocare i dati di configurazione per *ConfigID* prima di poter chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8b5cf-127">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5cf-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b5cf-128">Requirements</span></span>



| <span data-ttu-id="8b5cf-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b5cf-129">Requirement</span></span> | <span data-ttu-id="8b5cf-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8b5cf-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5cf-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b5cf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8b5cf-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8b5cf-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8b5cf-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b5cf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8b5cf-134">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b5cf-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b5cf-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b5cf-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b5cf-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b5cf-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b5cf-137">IDL</span><span class="sxs-lookup"><span data-stu-id="8b5cf-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b5cf-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b5cf-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b5cf-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b5cf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5cf-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="8b5cf-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





