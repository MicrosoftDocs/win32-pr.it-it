---
title: Metodo INapServerInfo GetNapServerInfo (NapServerManagement. h)
description: Recupera le informazioni sul server NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- NAP metodo GetNapServerInfo
- Metodo GetNapServerInfo NAP, interfaccia INapServerInfo
- Interfaccia INapServerInfo NAP, metodo GetNapServerInfo
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743887"
---
# <a name="inapserverinfogetnapserverinfo-method"></a><span data-ttu-id="d38d6-106">Metodo INapServerInfo:: GetNapServerInfo</span><span class="sxs-lookup"><span data-stu-id="d38d6-106">INapServerInfo::GetNapServerInfo method</span></span>

> [!Note]  
> <span data-ttu-id="d38d6-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="d38d6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d38d6-108">Il metodo **INapServerInfo:: GetNapServerInfo** recupera le informazioni sul server NAP.</span><span class="sxs-lookup"><span data-stu-id="d38d6-108">The **INapServerInfo::GetNapServerInfo** method retrieves information about the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38d6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d38d6-109">Syntax</span></span>


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="d38d6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d38d6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d38d6-111">*nomeserver* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d38d6-111">*serverName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d38d6-112">Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente il nome del server.</span><span class="sxs-lookup"><span data-stu-id="d38d6-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server name.</span></span>

</dd> <dt>

<span data-ttu-id="d38d6-113">*Descrizione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d38d6-113">*serverDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d38d6-114">Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la descrizione del server.</span><span class="sxs-lookup"><span data-stu-id="d38d6-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server description.</span></span>

</dd> <dt>

<span data-ttu-id="d38d6-115">*protocolVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d38d6-115">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d38d6-116">Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la versione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="d38d6-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d38d6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d38d6-117">Return value</span></span>

<span data-ttu-id="d38d6-118">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="d38d6-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d38d6-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d38d6-119">Return code</span></span>                                                                                     | <span data-ttu-id="d38d6-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d38d6-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d38d6-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d38d6-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d38d6-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="d38d6-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d38d6-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d38d6-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d38d6-124">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d38d6-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d38d6-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d38d6-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d38d6-126">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d38d6-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d38d6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d38d6-127">Requirements</span></span>



| <span data-ttu-id="d38d6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d38d6-128">Requirement</span></span> | <span data-ttu-id="d38d6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d38d6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38d6-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d38d6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d38d6-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d38d6-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="d38d6-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d38d6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d38d6-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d38d6-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d38d6-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d38d6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d38d6-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="d38d6-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="d38d6-136">IDL</span><span class="sxs-lookup"><span data-stu-id="d38d6-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d38d6-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d38d6-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="d38d6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d38d6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d38d6-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d38d6-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="d38d6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d38d6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38d6-141">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="d38d6-141">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> <dt>

[<span data-ttu-id="d38d6-142">**CountedString**</span><span class="sxs-lookup"><span data-stu-id="d38d6-142">**CountedString**</span></span>](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





