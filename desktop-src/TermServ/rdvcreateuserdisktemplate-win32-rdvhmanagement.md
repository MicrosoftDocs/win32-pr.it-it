---
title: Metodo RdvCreateUserDiskTemplate della classe Win32_RdvhManagement
description: Crea un modello di disco utente, con la dimensione massima specificata, nella posizione specificata.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RdvCreateUserDiskTemplate
- Metodo RdvCreateUserDiskTemplate Servizi Desktop remoto, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Servizi Desktop remoto, metodo RdvCreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743287"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="9cba9-106">Metodo RdvCreateUserDiskTemplate della \_ classe RdvhManagement Win32</span><span class="sxs-lookup"><span data-stu-id="9cba9-106">RdvCreateUserDiskTemplate method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="9cba9-107">Crea un modello di disco utente, con la dimensione massima specificata, nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="9cba9-107">Creates a user disk template, with the specified maximum size, at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cba9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cba9-108">Syntax</span></span>


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="9cba9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cba9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cba9-110">*UserDisksStorageUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cba9-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cba9-111">Percorso dell'archiviazione su disco dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9cba9-111">Location of the user disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="9cba9-112">*UserDiskMaxSizeInGB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cba9-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cba9-113">Dimensioni massime del disco utente, in GB.</span><span class="sxs-lookup"><span data-stu-id="9cba9-113">Maximum size of the user disk, in GB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cba9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cba9-114">Return value</span></span>

<span data-ttu-id="9cba9-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="9cba9-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9cba9-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9cba9-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cba9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cba9-117">Remarks</span></span>

<span data-ttu-id="9cba9-118">Tutti i dischi utente creati con questo modello avranno le stesse dimensioni massime del modello.</span><span class="sxs-lookup"><span data-stu-id="9cba9-118">All user disks created using this template will have the same maximum size as the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cba9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cba9-119">Requirements</span></span>



| <span data-ttu-id="9cba9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cba9-120">Requirement</span></span> | <span data-ttu-id="9cba9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9cba9-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cba9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cba9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9cba9-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9cba9-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="9cba9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cba9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9cba9-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9cba9-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="9cba9-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9cba9-126">Namespace</span></span><br/>                | <span data-ttu-id="9cba9-127">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9cba9-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="9cba9-128">MOF</span><span class="sxs-lookup"><span data-stu-id="9cba9-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cba9-129"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cba9-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="9cba9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9cba9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cba9-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cba9-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cba9-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cba9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cba9-133">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="9cba9-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





