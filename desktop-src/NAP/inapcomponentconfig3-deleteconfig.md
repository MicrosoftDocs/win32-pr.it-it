---
title: Metodo INapComponentConfig3 DeleteConfig (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per eliminare i dati di configurazione per un ID configurazione specifico.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- NAP metodo DeleteConfig
- Metodo DeleteConfig NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo DeleteConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740946"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a><span data-ttu-id="243a5-106">INapComponentConfig3::D Metodo eleteConfig</span><span class="sxs-lookup"><span data-stu-id="243a5-106">INapComponentConfig3::DeleteConfig method</span></span>

> [!Note]  
> <span data-ttu-id="243a5-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="243a5-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="243a5-108">Il metodo **DeleteConfig** viene implementato da convalida integrità sistema (SHV) per fornire un modo per eliminare i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="243a5-108">The **DeleteConfig** method is implemented by system health validators (SHVs) to provide a way to delete configuration data for a specific configuration ID.</span></span> <span data-ttu-id="243a5-109">È possibile riutilizzare l'ID dopo l'eliminazione dei dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="243a5-109">The ID may be reused after the configuration data has been deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="243a5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="243a5-110">Syntax</span></span>


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="243a5-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="243a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="243a5-112">*configID*</span><span class="sxs-lookup"><span data-stu-id="243a5-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="243a5-113">Valore che rappresenta i dati di configurazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="243a5-113">A value that represents the configuration data to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="243a5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="243a5-114">Return value</span></span>

<span data-ttu-id="243a5-115">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="243a5-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="243a5-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="243a5-116">Return code</span></span>                                                                                                    | <span data-ttu-id="243a5-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="243a5-117">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="243a5-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="243a5-118"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="243a5-119">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="243a5-119">The operation is successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="243a5-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="243a5-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="243a5-121">*ConfigID* è 0 (un valore riservato per la configurazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="243a5-121">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/> |
| <dl> <span data-ttu-id="243a5-122"><dt>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ non \_ trovata**</dt></span><span class="sxs-lookup"><span data-stu-id="243a5-122"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="243a5-123">*ConfigID* non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="243a5-123">*ConfigID* cannot be found.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="243a5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="243a5-124">Requirements</span></span>



| <span data-ttu-id="243a5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="243a5-125">Requirement</span></span> | <span data-ttu-id="243a5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="243a5-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="243a5-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="243a5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="243a5-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="243a5-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="243a5-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="243a5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="243a5-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="243a5-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="243a5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="243a5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="243a5-132"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="243a5-132"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="243a5-133">IDL</span><span class="sxs-lookup"><span data-stu-id="243a5-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="243a5-134"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="243a5-134"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="243a5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="243a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243a5-136">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="243a5-136">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





