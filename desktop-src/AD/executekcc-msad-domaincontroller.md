---
title: Metodo ExecuteKCC della classe MSAD_DomainController
description: Chiama la funzione DsReplicaConsistencyCheck, che richiama il controllo di coerenza informazioni (KCC) per verificare la topologia di replica.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Active Directory del metodo ExecuteKCC
- Metodo ExecuteKCC Active Directory, classe MSAD_DomainController
- Classe MSAD_DomainController Active Directory, metodo ExecuteKCC
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301944"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a><span data-ttu-id="cdd0a-106">Metodo ExecuteKCC della \_ classe DomainController MSAD</span><span class="sxs-lookup"><span data-stu-id="cdd0a-106">ExecuteKCC method of the MSAD\_DomainController class</span></span>

<span data-ttu-id="cdd0a-107">Chiama la funzione [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , che richiama il controllo di coerenza informazioni (KCC) per verificare la topologia di replica.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-107">Calls the [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) function, which invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd0a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdd0a-108">Syntax</span></span>


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cdd0a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdd0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd0a-110">*TaskId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd0a-110">*TaskID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd0a-111">Attività che deve essere eseguita dal KCC.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-111">The task that the KCC should execute.</span></span> <span data-ttu-id="cdd0a-112">Servizi di **dominio Active Directory \_ La \_ \_ \_ topologia di aggiornamento taskId di KCC** è l'unico valore attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-112">**DS\_KCC\_TASKID\_UPDATE\_TOPOLOGY** is the only value that is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="cdd0a-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd0a-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd0a-114">Set di flag che modificano il comportamento del metodo **ExecuteKCC** .</span><span class="sxs-lookup"><span data-stu-id="cdd0a-114">A set of flags that modify the behavior of the **ExecuteKCC** method.</span></span> <span data-ttu-id="cdd0a-115">Questo parametro può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-115">This parameter can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span data-ttu-id="cdd0a-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS \_ KCC \_ flag \_ Async \_ op**</span><span class="sxs-lookup"><span data-stu-id="cdd0a-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS\_KCC\_FLAG\_ASYNC\_OP**</span></span>


</dt> <dd>

<span data-ttu-id="cdd0a-117">L'attività viene accodata, quindi la funzione restituisce senza attendere il completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-117">The task is queued and then the function returns without waiting for the task to complete.</span></span>

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span data-ttu-id="cdd0a-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**\_flag KCC \_ DS \_ smorzato**</span><span class="sxs-lookup"><span data-stu-id="cdd0a-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS\_KCC\_FLAG\_DAMPED**</span></span>


</dt> <dd>

<span data-ttu-id="cdd0a-119">L'attività non verrà aggiunta alla coda se un'altra attività accodata verrà eseguita a breve.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-119">The task will not be added to the queue if another queued task will run soon.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd0a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdd0a-120">Return value</span></span>

<span data-ttu-id="cdd0a-121">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-121">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd0a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdd0a-122">Requirements</span></span>



| <span data-ttu-id="cdd0a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdd0a-123">Requirement</span></span> | <span data-ttu-id="cdd0a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cdd0a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd0a-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdd0a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd0a-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cdd0a-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cdd0a-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdd0a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd0a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdd0a-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cdd0a-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cdd0a-129">Namespace</span></span><br/>                | <span data-ttu-id="cdd0a-130">\\MicrosoftActiveDirectory radice</span><span class="sxs-lookup"><span data-stu-id="cdd0a-130">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="cdd0a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cdd0a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdd0a-132"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdd0a-132"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdd0a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cdd0a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdd0a-134"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdd0a-134"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd0a-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdd0a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd0a-136">**MSAD \_ DomainController**</span><span class="sxs-lookup"><span data-stu-id="cdd0a-136">**MSAD\_DomainController**</span></span>](msad-domaincontroller.md)
</dt> </dl>

 

 





