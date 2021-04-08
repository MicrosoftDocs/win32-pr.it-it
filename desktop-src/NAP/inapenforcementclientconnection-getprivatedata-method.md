---
title: Metodo INapEnforcementClientConnection GetPrivateData (NapEnforcementClient. h)
description: Viene usato da NapAgent per ottenere i dati privati.
ms.assetid: d38ef523-b645-401f-b3a9-1315ef39931a
keywords:
- NAP metodo GetPrivateData
- Metodo GetPrivateData NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6618ff7b25ad57cbb943107e80f299d9b6a68bea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873558"
---
# <a name="inapenforcementclientconnectiongetprivatedata-method"></a><span data-ttu-id="98cfb-106">Metodo INapEnforcementClientConnection:: GetPrivateData</span><span class="sxs-lookup"><span data-stu-id="98cfb-106">INapEnforcementClientConnection::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="98cfb-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="98cfb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="98cfb-108">Il metodo **INapEnforcementClientConnection:: GetPrivateData** viene usato da napagent per ottenere i dati privati.</span><span class="sxs-lookup"><span data-stu-id="98cfb-108">The **INapEnforcementClientConnection::GetPrivateData** method is used by the NapAgent to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="98cfb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98cfb-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="98cfb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="98cfb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98cfb-111">*PrivateData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="98cfb-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98cfb-112">Puntatore a un puntatore a un BLOB di dati opachi [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che può essere interpretato solo da napagent.</span><span class="sxs-lookup"><span data-stu-id="98cfb-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98cfb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98cfb-113">Return value</span></span>

<span data-ttu-id="98cfb-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="98cfb-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="98cfb-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="98cfb-115">Return code</span></span>                                                                                     | <span data-ttu-id="98cfb-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98cfb-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="98cfb-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98cfb-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="98cfb-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="98cfb-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="98cfb-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="98cfb-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="98cfb-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="98cfb-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="98cfb-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="98cfb-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="98cfb-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="98cfb-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98cfb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98cfb-123">Requirements</span></span>



| <span data-ttu-id="98cfb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="98cfb-124">Requirement</span></span> | <span data-ttu-id="98cfb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="98cfb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98cfb-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98cfb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98cfb-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98cfb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="98cfb-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98cfb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98cfb-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98cfb-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="98cfb-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98cfb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="98cfb-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="98cfb-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="98cfb-132">IDL</span><span class="sxs-lookup"><span data-stu-id="98cfb-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98cfb-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98cfb-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="98cfb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="98cfb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98cfb-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98cfb-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="98cfb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98cfb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98cfb-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="98cfb-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





