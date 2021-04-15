---
title: Metodo Initialize INapEnforcementClientConnection (NapEnforcementClient. h)
description: Inizializza la connessione client.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapEnforcementClientConnection
- Interfaccia NAP di INapEnforcementClientConnection, metodo Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475994"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a><span data-ttu-id="e9c09-106">Metodo INapEnforcementClientConnection:: Initialize</span><span class="sxs-lookup"><span data-stu-id="e9c09-106">INapEnforcementClientConnection::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="e9c09-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="e9c09-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e9c09-108">Il metodo **INapEnforcementClientConnection:: Initialize** Inizializza la connessione client.</span><span class="sxs-lookup"><span data-stu-id="e9c09-108">The **INapEnforcementClientConnection::Initialize** method initializes the client connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c09-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9c09-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="e9c09-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9c09-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c09-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9c09-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c09-112">Puntatore a un [**EnforementEntityId**](nap-datatypes.md) che identifica il client di imposizione che richiede la connessione.</span><span class="sxs-lookup"><span data-stu-id="e9c09-112">A pointer to an [**EnforementEntityId**](nap-datatypes.md) that identifies the enforcement client requesting the connection.</span></span> <span data-ttu-id="e9c09-113">Questo valore viene impostato da NapAgent durante la creazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="e9c09-113">This value is set by the NapAgent during connection creation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9c09-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9c09-114">Return value</span></span>

<span data-ttu-id="e9c09-115">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="e9c09-115">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e9c09-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e9c09-116">Return code</span></span>                                                                                     | <span data-ttu-id="e9c09-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9c09-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9c09-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c09-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e9c09-119">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="e9c09-119">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e9c09-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c09-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e9c09-121">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="e9c09-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e9c09-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e9c09-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e9c09-123">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e9c09-123">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e9c09-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9c09-124">Requirements</span></span>



| <span data-ttu-id="e9c09-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9c09-125">Requirement</span></span> | <span data-ttu-id="e9c09-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e9c09-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c09-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9c09-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c09-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9c09-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e9c09-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9c09-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c09-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9c09-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e9c09-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9c09-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c09-132"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c09-132"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9c09-133">IDL</span><span class="sxs-lookup"><span data-stu-id="e9c09-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9c09-134"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9c09-134"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e9c09-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e9c09-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9c09-136"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9c09-136"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e9c09-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9c09-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c09-138">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e9c09-138">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





