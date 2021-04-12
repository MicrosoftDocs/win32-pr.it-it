---
title: Metodo INapServerManagement RegisterSystemHealthValidator (NapServerManagement. h)
description: Registra un servizio di convalida dell'integrità.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- NAP metodo RegisterSystemHealthValidator
- Metodo RegisterSystemHealthValidator NAP, interfaccia INapServerManagement
- Interfaccia INapServerManagement NAP, metodo RegisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225247"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a><span data-ttu-id="b3c14-106">Metodo INapServerManagement:: RegisterSystemHealthValidator</span><span class="sxs-lookup"><span data-stu-id="b3c14-106">INapServerManagement::RegisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="b3c14-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="b3c14-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b3c14-108">Il metodo **INapServerManagement:: RegisterSystemHealthValidator** registra un servizio di convalida dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="b3c14-108">The **INapServerManagement::RegisterSystemHealthValidator** method registers an SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c14-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3c14-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a><span data-ttu-id="b3c14-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3c14-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c14-111">*validator* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b3c14-111">*validator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c14-112">Puntatore a una struttura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione di convalida integrità sistema.</span><span class="sxs-lookup"><span data-stu-id="b3c14-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="b3c14-113">*validatorClsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3c14-113">*validatorClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c14-114">Puntatore al CLSID della classe COM che implementa l'interfaccia [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c14-114">A pointer to the CLSID of the COM class that implements the [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c14-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3c14-115">Return value</span></span>

<span data-ttu-id="b3c14-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="b3c14-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b3c14-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b3c14-117">Return code</span></span>                                                                                            | <span data-ttu-id="b3c14-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3c14-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3c14-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c14-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="b3c14-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b3c14-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b3c14-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c14-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="b3c14-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="b3c14-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b3c14-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c14-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="b3c14-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b3c14-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b3c14-125"><dt>**protezione accesso alla rete \_ E \_ ID in conflitto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c14-125"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="b3c14-126">L'ID di convalida integrità sistema è già registrato.</span><span class="sxs-lookup"><span data-stu-id="b3c14-126">SHV id is already registered.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="b3c14-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3c14-127">Requirements</span></span>



| <span data-ttu-id="b3c14-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c14-128">Requirement</span></span> | <span data-ttu-id="b3c14-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b3c14-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c14-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3c14-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c14-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b3c14-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="b3c14-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3c14-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c14-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3c14-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b3c14-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3c14-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c14-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c14-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3c14-136">IDL</span><span class="sxs-lookup"><span data-stu-id="b3c14-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3c14-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3c14-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b3c14-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c14-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c14-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c14-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="b3c14-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3c14-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c14-141">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="b3c14-141">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





