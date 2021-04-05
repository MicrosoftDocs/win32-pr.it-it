---
title: Metodo INapEnforcementClientBinding CreateConnection (NapEnforcementClient. h)
description: Viene utilizzato dalle forze di esecuzione per creare oggetti connessione.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- NAP Metodo CreateConnection
- Metodo CreateConnection NAP, interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding NAP, Metodo CreateConnection
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048160"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a><span data-ttu-id="98d7a-106">Metodo INapEnforcementClientBinding:: CreateConnection</span><span class="sxs-lookup"><span data-stu-id="98d7a-106">INapEnforcementClientBinding::CreateConnection method</span></span>

> [!Note]  
> <span data-ttu-id="98d7a-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="98d7a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="98d7a-108">Il metodo factory **INapEnforcementClientBinding:: CreateConnection** viene usato dalle forze di esecuzione per creare gli oggetti di connessione.</span><span class="sxs-lookup"><span data-stu-id="98d7a-108">The **INapEnforcementClientBinding::CreateConnection** factory method is used by enforcers to create connection objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d7a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98d7a-109">Syntax</span></span>


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a><span data-ttu-id="98d7a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="98d7a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98d7a-111">*connessione* \[ a out\]</span><span class="sxs-lookup"><span data-stu-id="98d7a-111">*connection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98d7a-112">Puntatore COM a una nuova interfaccia [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) restituita dal sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="98d7a-112">A COM pointer to a new [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface returned by the NAP system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98d7a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98d7a-113">Return value</span></span>

<span data-ttu-id="98d7a-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="98d7a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="98d7a-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="98d7a-115">Return code</span></span>                                                                                     | <span data-ttu-id="98d7a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98d7a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="98d7a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98d7a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="98d7a-118">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="98d7a-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="98d7a-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="98d7a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="98d7a-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="98d7a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="98d7a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="98d7a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="98d7a-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="98d7a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98d7a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="98d7a-123">Remarks</span></span>

<span data-ttu-id="98d7a-124">Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="98d7a-124">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d7a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98d7a-125">Requirements</span></span>



| <span data-ttu-id="98d7a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="98d7a-126">Requirement</span></span> | <span data-ttu-id="98d7a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="98d7a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d7a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98d7a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="98d7a-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98d7a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="98d7a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98d7a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="98d7a-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98d7a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="98d7a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98d7a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="98d7a-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="98d7a-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="98d7a-134">IDL</span><span class="sxs-lookup"><span data-stu-id="98d7a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98d7a-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98d7a-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="98d7a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="98d7a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98d7a-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98d7a-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="98d7a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98d7a-138">See also</span></span>

<dl> <span data-ttu-id="98d7a-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="98d7a-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="98d7a-140">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="98d7a-140">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="98d7a-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="98d7a-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





