---
title: Metodo GetPendingStartServerList della classe Win32_RDSHServer
description: Recupera un elenco di server in attesa di avvio.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetPendingStartServerList
- Metodo GetPendingStartServerList Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, metodo GetPendingStartServerList
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400673"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="7f5a0-106">Metodo GetPendingStartServerList della \_ classe RDSHServer Win32</span><span class="sxs-lookup"><span data-stu-id="7f5a0-106">GetPendingStartServerList method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="7f5a0-107">Recupera un elenco di server in attesa di avvio.</span><span class="sxs-lookup"><span data-stu-id="7f5a0-107">Retrieves a list of server waiting to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f5a0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f5a0-108">Syntax</span></span>


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a><span data-ttu-id="7f5a0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f5a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f5a0-110">*maxServers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f5a0-110">*maxServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f5a0-111">Numero massimo di server da restituire nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7f5a0-111">The maximum number of servers to return in the list.</span></span>

</dd> <dt>

<span data-ttu-id="7f5a0-112">*ServerFQDNs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7f5a0-112">*ServerFQDNs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f5a0-113">Se l'operazione ha esito positivo, contiene una raccolta di nomi di dominio completi dei server in attesa di avvio.</span><span class="sxs-lookup"><span data-stu-id="7f5a0-113">On success, contains a collection of fully-qualified domain names of the servers waiting to start.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f5a0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f5a0-114">Remarks</span></span>

<span data-ttu-id="7f5a0-115">L'elenco dei server viene reimpostato dopo ogni chiamata, in modo che la chiamata successiva non otterrà un server duplicato.</span><span class="sxs-lookup"><span data-stu-id="7f5a0-115">The list of servers is reset after every call, so that the next call will not get a duplicate server.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f5a0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f5a0-116">Requirements</span></span>



| <span data-ttu-id="7f5a0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f5a0-117">Requirement</span></span> | <span data-ttu-id="7f5a0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7f5a0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f5a0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f5a0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f5a0-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7f5a0-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7f5a0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f5a0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f5a0-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7f5a0-122">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="7f5a0-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7f5a0-123">Namespace</span></span><br/>                | <span data-ttu-id="7f5a0-124">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="7f5a0-124">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7f5a0-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7f5a0-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f5a0-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f5a0-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f5a0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7f5a0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f5a0-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f5a0-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7f5a0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f5a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f5a0-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="7f5a0-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





