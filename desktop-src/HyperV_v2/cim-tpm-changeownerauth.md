---
description: Modifica le credenziali di autorizzazione del proprietario del dispositivo TPM. Sono necessarie le password di autorizzazione del proprietario precedenti e nuove.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Metodo ChangeOwnerAuth della classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310574"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a><span data-ttu-id="ce510-104">Metodo ChangeOwnerAuth della classe del \_ TPM CIM</span><span class="sxs-lookup"><span data-stu-id="ce510-104">ChangeOwnerAuth method of the CIM\_TPM class</span></span>

<span data-ttu-id="ce510-105">Modifica le credenziali di autorizzazione del proprietario del dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="ce510-105">Changes the owner authorization credential of the TPM device.</span></span> <span data-ttu-id="ce510-106">Sono necessarie le password di autorizzazione del proprietario precedenti e nuove.</span><span class="sxs-lookup"><span data-stu-id="ce510-106">The old and new owner authorization passwords are required.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce510-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce510-107">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="ce510-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce510-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce510-109">*OldOwnerAuth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce510-109">*OldOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce510-110">Rappresenta le credenziali di autorizzazione del proprietario precedenti necessarie per assumere la proprietà del dispositivo TPM. La sottoclasse **CIM \_ SharedCredential** può essere obbligatoria con un valore non null del **\_ SharedCredential CIM**.**Proprietà Secret** per il parametro.</span><span class="sxs-lookup"><span data-stu-id="ce510-110">Represents the old owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce510-111">*NewOwnerAuth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce510-111">*NewOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce510-112">Rappresenta le nuove credenziali di autorizzazione del proprietario necessarie per assumere la proprietà del dispositivo TPM. La sottoclasse **CIM \_ SharedCredential** può essere obbligatoria con un valore non null del **\_ SharedCredential CIM**.**Proprietà Secret** per il parametro.</span><span class="sxs-lookup"><span data-stu-id="ce510-112">Represents the new owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce510-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce510-113">Return value</span></span>

<span data-ttu-id="ce510-114">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ce510-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ce510-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ce510-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ce510-116">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ce510-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ce510-117">**Errore sconosciuto/non specificato** (2)</span><span class="sxs-lookup"><span data-stu-id="ce510-117">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ce510-118">**DMTF riservato** (3.. 4095)</span><span class="sxs-lookup"><span data-stu-id="ce510-118">**DMTF Reserved** (3..4095)</span></span>
</dt> <dt>

<span data-ttu-id="ce510-119">**Metodo riservato** (4096.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ce510-119">**Method Reserved** (4096..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ce510-120">**Fornitore specificato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ce510-120">**Vendor Specified** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ce510-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce510-121">Requirements</span></span>



| <span data-ttu-id="ce510-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce510-122">Requirement</span></span> | <span data-ttu-id="ce510-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ce510-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce510-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce510-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ce510-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ce510-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ce510-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce510-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ce510-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ce510-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ce510-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ce510-128">Namespace</span></span><br/>                | <span data-ttu-id="ce510-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ce510-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ce510-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ce510-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce510-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce510-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce510-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ce510-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce510-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ce510-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ce510-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce510-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce510-135">**\_TPM CIM**</span><span class="sxs-lookup"><span data-stu-id="ce510-135">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




