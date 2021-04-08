---
title: Metodo QueryOfflineInformation della classe Win32_TSVm
description: Recupera le proprietà del server di desktop virtuale (VDS) corrente, ma solo quando il server è offline.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo QueryOfflineInformation
- Metodo QueryOfflineInformation Servizi Desktop remoto, classe Win32_TSVm
- Classe Win32_TSVm Servizi Desktop remoto, metodo QueryOfflineInformation
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874073"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a><span data-ttu-id="923cb-106">Metodo QueryOfflineInformation della \_ classe TSVm Win32</span><span class="sxs-lookup"><span data-stu-id="923cb-106">QueryOfflineInformation method of the Win32\_TSVm class</span></span>

<span data-ttu-id="923cb-107">Recupera le proprietà del server di desktop virtuale (VDS) corrente, ma solo quando il server è offline.</span><span class="sxs-lookup"><span data-stu-id="923cb-107">Retrieves the properties of the current virtual desktop server (VDS), but only when the server is offline.</span></span>

## <a name="syntax"></a><span data-ttu-id="923cb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="923cb-108">Syntax</span></span>


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="923cb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="923cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="923cb-110">*Compilazione* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-110">*Build* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-111">In seguito a un esito positivo, restituisce la versione build del VDS.</span><span class="sxs-lookup"><span data-stu-id="923cb-111">On a success, returns the build version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="923cb-112">*CurrentVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-112">*CurrentVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-113">In seguito a un esito positivo, restituisce la versione corrente del VDS.</span><span class="sxs-lookup"><span data-stu-id="923cb-113">On a success, returns the current version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="923cb-114">*INSTALLATIONTYPE* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-114">*InstallationType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-115">In seguito a un esito positivo, restituisce il tipo di installazione del VDS.</span><span class="sxs-lookup"><span data-stu-id="923cb-115">On a success, returns the installation type of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="923cb-116">*EditionID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-116">*EditionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-117">In seguito all'esito positivo, restituisce l'ID edizione del VDS.</span><span class="sxs-lookup"><span data-stu-id="923cb-117">On a success, returns the edition ID of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="923cb-118">*SysPrepImageState* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-118">*SysPrepImageState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-119">In seguito all'esito positivo, restituisce lo stato dell'immagine di preparazione del sistema VDS.</span><span class="sxs-lookup"><span data-stu-id="923cb-119">On success, returns the system prep image state of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="923cb-120">*SysPrepMode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-120">*SysPrepMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-121">In seguito a un esito positivo, restituisce la modalità di preparazione del sistema VDS.</span><span class="sxs-lookup"><span data-stu-id="923cb-121">On a success, returns the system prep mode of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="923cb-122">*ProcArch* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-122">*ProcArch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-123">In seguito a un esito positivo, restituisce un valore che indica l'architettura del processore.</span><span class="sxs-lookup"><span data-stu-id="923cb-123">On a success, returns a value indicating the processor architecture.</span></span>

<dt>

<span data-ttu-id="923cb-124">0</span><span class="sxs-lookup"><span data-stu-id="923cb-124">0</span></span>
</dt> <dd>

<span data-ttu-id="923cb-125">x86</span><span class="sxs-lookup"><span data-stu-id="923cb-125">x86</span></span>

</dd> <dt>

<span data-ttu-id="923cb-126">1</span><span class="sxs-lookup"><span data-stu-id="923cb-126">1</span></span>
</dt> <dd>

<span data-ttu-id="923cb-127">amd64</span><span class="sxs-lookup"><span data-stu-id="923cb-127">amd64</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="923cb-128">*fIsVmbusCapable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-128">*fIsVmbusCapable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-129">con esito positivo, indica se il sistema è in grado di supportare VMBus.</span><span class="sxs-lookup"><span data-stu-id="923cb-129">on a success, indicates whether the system is VMBus-capable.</span></span>

</dd> <dt>

<span data-ttu-id="923cb-130">*fIsRdvIcInstalled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="923cb-130">*fIsRdvIcInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="923cb-131">In caso di esito positivo, indica se RDVIC è installato.</span><span class="sxs-lookup"><span data-stu-id="923cb-131">On a success, indicates if RDVIC is installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="923cb-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="923cb-132">Return value</span></span>

<span data-ttu-id="923cb-133">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="923cb-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="923cb-134">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="923cb-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="923cb-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="923cb-135">Requirements</span></span>



| <span data-ttu-id="923cb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="923cb-136">Requirement</span></span> | <span data-ttu-id="923cb-137">Valore</span><span class="sxs-lookup"><span data-stu-id="923cb-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="923cb-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="923cb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="923cb-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="923cb-139">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="923cb-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="923cb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="923cb-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="923cb-141">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="923cb-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="923cb-142">Namespace</span></span><br/>                | <span data-ttu-id="923cb-143">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="923cb-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="923cb-144">MOF</span><span class="sxs-lookup"><span data-stu-id="923cb-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="923cb-145"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="923cb-145"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="923cb-146">DLL</span><span class="sxs-lookup"><span data-stu-id="923cb-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="923cb-147"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="923cb-147"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="923cb-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="923cb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923cb-149">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="923cb-149">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





