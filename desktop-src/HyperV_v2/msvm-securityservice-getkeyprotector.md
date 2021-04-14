---
description: Recupera la protezione con chiave per un sistema virtuale.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Metodo GetKeyProtector della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49f2479660d0402c7b3d428c76f9fe454ecf64cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350651"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="395c7-103">Metodo GetKeyProtector della classe MSVM \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="395c7-103">GetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="395c7-104">Recupera la protezione con chiave per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="395c7-104">Retrieves the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="395c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="395c7-105">Syntax</span></span>


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a><span data-ttu-id="395c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="395c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="395c7-107">*SecuritySettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="395c7-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="395c7-108">La stringa contiene un'istanza incorporata della classe [**\_ SecuritySettingData MSVM**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="395c7-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="395c7-109">*Protector* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="395c7-109">*KeyProtector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="395c7-110">Riceve la matrice di byte non elaborati che contiene la protezione con chiave attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="395c7-110">Receives the raw byte array that contains the key protector currently in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="395c7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="395c7-111">Return value</span></span>

<span data-ttu-id="395c7-112">Se l'operazione riesce, restituisce 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="395c7-112">On success, returns a 0 or 4096.</span></span> <span data-ttu-id="395c7-113">In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="395c7-113">Otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="395c7-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="395c7-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="395c7-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="395c7-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="395c7-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="395c7-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="395c7-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="395c7-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="395c7-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-122">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="395c7-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="395c7-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="395c7-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="395c7-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="395c7-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="395c7-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="395c7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="395c7-127">Requirements</span></span>



| <span data-ttu-id="395c7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="395c7-128">Requirement</span></span> | <span data-ttu-id="395c7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="395c7-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="395c7-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="395c7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="395c7-131">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="395c7-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="395c7-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="395c7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="395c7-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="395c7-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="395c7-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="395c7-134">Namespace</span></span><br/>                | <span data-ttu-id="395c7-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="395c7-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="395c7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="395c7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="395c7-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="395c7-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="395c7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="395c7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="395c7-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="395c7-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="395c7-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="395c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="395c7-141">**\_SecurityService MSVM**</span><span class="sxs-lookup"><span data-stu-id="395c7-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




