---
title: Metodo INapComponentConfig3 NewConfig (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per creare i dati di configurazione per un ID configurazione specifico.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- NAP metodo NewConfig
- Metodo NewConfig NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo NewConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119403"
---
# <a name="inapcomponentconfig3newconfig-method"></a><span data-ttu-id="4f463-106">Metodo INapComponentConfig3:: NewConfig</span><span class="sxs-lookup"><span data-stu-id="4f463-106">INapComponentConfig3::NewConfig method</span></span>

> [!Note]  
> <span data-ttu-id="4f463-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="4f463-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4f463-108">Il metodo **NewConfig** viene implementato da convalida integrità sistema (SHV) per fornire un modo per creare i dati di configurazione per un ID configurazione specifico.</span><span class="sxs-lookup"><span data-stu-id="4f463-108">The **NewConfig** method is implemented by system health validators (SHVs) to provide a way to create configuration data for a specific configuration ID.</span></span> <span data-ttu-id="4f463-109">Quando questa funzione viene chiamata, un servizio di convalida dell'integrità di sistema deve allocare nuovi dati di configurazione e popolarli con una copia dei dati di configurazione predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4f463-109">When this function is called, an SHV must allocate new configuration data and populate it with a copy of the default configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f463-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f463-110">Syntax</span></span>


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="4f463-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f463-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f463-112">*configID*</span><span class="sxs-lookup"><span data-stu-id="4f463-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="4f463-113">Valore che rappresenta la configurazione.</span><span class="sxs-lookup"><span data-stu-id="4f463-113">A value that represents the configuration.</span></span> <span data-ttu-id="4f463-114">*ConfigID* viene assegnato dal servizio Server dei criteri di rete ed è univoco all'interno del servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="4f463-114">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f463-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f463-115">Return value</span></span>

<span data-ttu-id="4f463-116">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="4f463-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="4f463-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4f463-117">Return code</span></span>                                                                                                 | <span data-ttu-id="4f463-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f463-118">Description</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f463-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f463-119"><dt>**S\_OK** </dt></span></span> </dl>                       | <span data-ttu-id="4f463-120">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="4f463-120">The operation is successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="4f463-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4f463-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="4f463-122">*ConfigID* è 0 (un valore riservato per la configurazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="4f463-122">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/>                  |
| <dl> <span data-ttu-id="4f463-123"><dt>**configurazione di protezione accesso alla rete \_ E \_ Convalida integrità sistema \_ \_ esistente**</dt></span><span class="sxs-lookup"><span data-stu-id="4f463-123"><dt>**NAP\_E\_SHV\_CONFIG\_EXISTED**</dt></span></span> </dl> | <span data-ttu-id="4f463-124">*ConfigID* esiste già.</span><span class="sxs-lookup"><span data-stu-id="4f463-124">*ConfigID* already exists.</span></span> <span data-ttu-id="4f463-125">L'elenco di ID noto a server dei criteri di servizio è diverso da quello di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="4f463-125">The list of IDs known to NPS is different from the SHV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f463-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f463-126">Remarks</span></span>

<span data-ttu-id="4f463-127">Dopo la creazione della nuova configurazione da parte di **NewConfig**, è consigliabile usare i metodi [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)e [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) per modificare la configurazione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="4f463-127">After the new configuration is created by **NewConfig**, the [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md), and [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) methods should be used to alter the configuration as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f463-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f463-128">Requirements</span></span>



| <span data-ttu-id="4f463-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f463-129">Requirement</span></span> | <span data-ttu-id="4f463-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4f463-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f463-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f463-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4f463-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f463-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4f463-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f463-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4f463-134">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f463-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f463-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f463-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f463-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f463-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f463-137">IDL</span><span class="sxs-lookup"><span data-stu-id="4f463-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f463-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f463-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f463-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f463-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f463-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="4f463-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





