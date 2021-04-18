---
title: Metodo INapComponentConfig3 SetConfigToID (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per impostare i dati di configurazione per un ID configurazione specifico.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- NAP metodo SetConfigToID
- Metodo SetConfigToID NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo SetConfigToID
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302719"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a><span data-ttu-id="2506d-106">Metodo INapComponentConfig3:: SetConfigToID</span><span class="sxs-lookup"><span data-stu-id="2506d-106">INapComponentConfig3::SetConfigToID method</span></span>

> [!Note]  
> <span data-ttu-id="2506d-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="2506d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2506d-108">Il metodo **SetConfigToID** viene implementato da convalida integrità sistema (SHV) per fornire un modo per impostare i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="2506d-108">The **SetConfigToID** method is implemented by system health validators (SHVs) to provide a way to set the configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="2506d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2506d-109">Syntax</span></span>


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="2506d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2506d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2506d-111">*configID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2506d-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2506d-112">Valore che rappresenta la configurazione.</span><span class="sxs-lookup"><span data-stu-id="2506d-112">A value that represents the configuration.</span></span> <span data-ttu-id="2506d-113">*ConfigID* viene assegnato dal servizio Server dei criteri di rete ed è univoco all'interno del servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="2506d-113">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span> <span data-ttu-id="2506d-114">Se *ConfigID* è 0, viene impostata la configurazione predefinita del servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="2506d-114">If *ConfigID* is 0, the default configuration of the SHV is set.</span></span>

</dd> <dt>

<span data-ttu-id="2506d-115">*numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2506d-115">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2506d-116">Dimensione, in byte, dei dati di configurazione nei *dati*.</span><span class="sxs-lookup"><span data-stu-id="2506d-116">The size, in bytes, of the configuration data in *data*.</span></span>

</dd> <dt>

<span data-ttu-id="2506d-117">*dati* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2506d-117">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2506d-118">In input, matrice di BYTE che contiene i dati di configurazione impostati su *ConfigID*.</span><span class="sxs-lookup"><span data-stu-id="2506d-118">On input, a BYTE array that contains the configuration data set to *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2506d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2506d-119">Return value</span></span>

<span data-ttu-id="2506d-120">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="2506d-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="2506d-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2506d-121">Return code</span></span>                                                                                                    | <span data-ttu-id="2506d-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2506d-122">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="2506d-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2506d-123"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="2506d-124">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="2506d-124">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="2506d-125"><dt>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ non \_ trovata**</dt></span><span class="sxs-lookup"><span data-stu-id="2506d-125"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="2506d-126">*ConfigID* non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="2506d-126">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="2506d-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2506d-127">Remarks</span></span>

<span data-ttu-id="2506d-128">Il metodo [**NewConfig**](inapcomponentconfig3-newconfig.md) deve essere usato per allocare i dati di configurazione per *ConfigID* prima di poter chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2506d-128">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="2506d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2506d-129">Requirements</span></span>



| <span data-ttu-id="2506d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2506d-130">Requirement</span></span> | <span data-ttu-id="2506d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2506d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2506d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2506d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2506d-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2506d-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2506d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2506d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2506d-135">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2506d-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2506d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2506d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2506d-137"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2506d-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="2506d-138">IDL</span><span class="sxs-lookup"><span data-stu-id="2506d-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2506d-139"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2506d-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2506d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2506d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2506d-141">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="2506d-141">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





