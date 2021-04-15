---
title: Metodo GetVirtualDesktopDetails della classe Win32_RDMSVirtualDesktop
description: Recupera le informazioni aggiuntive sul desktop virtuale.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetVirtualDesktopDetails
- Metodo GetVirtualDesktopDetails Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo GetVirtualDesktopDetails
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477446"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="73e19-106">Metodo GetVirtualDesktopDetails della \_ classe RDMSVirtualDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="73e19-106">GetVirtualDesktopDetails method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="73e19-107">Recupera le informazioni aggiuntive sul desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="73e19-107">Retrieves the additional information about the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e19-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73e19-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a><span data-ttu-id="73e19-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="73e19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e19-110">*RAMSizeInMB* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="73e19-110">*RAMSizeInMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73e19-111">Riceve la quantità di RAM assegnata al desktop virtuale, in byte.</span><span class="sxs-lookup"><span data-stu-id="73e19-111">Receives the amount of RAM assigned to the virtual desktop, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="73e19-112">*RemoteFXEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="73e19-112">*RemoteFXEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73e19-113">Riceve un valore che indica se RemoteFX è abilitato sul desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="73e19-113">Receives a value that indicates whether RemoteFX is enabled on the virtual desktop.</span></span> <span data-ttu-id="73e19-114">**True** se RemoteFX è abilitato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="73e19-114">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="73e19-115">*OSVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="73e19-115">*OSVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73e19-116">Riceve la versione del sistema operativo del desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="73e19-116">Receives the OS version of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e19-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73e19-117">Return value</span></span>

<span data-ttu-id="73e19-118">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="73e19-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e19-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73e19-119">Requirements</span></span>



| <span data-ttu-id="73e19-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e19-120">Requirement</span></span> | <span data-ttu-id="73e19-121">Valore</span><span class="sxs-lookup"><span data-stu-id="73e19-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e19-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73e19-122">Minimum supported client</span></span><br/> | <span data-ttu-id="73e19-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="73e19-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="73e19-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73e19-124">Minimum supported server</span></span><br/> | <span data-ttu-id="73e19-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73e19-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="73e19-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73e19-126">Namespace</span></span><br/>                | <span data-ttu-id="73e19-127">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="73e19-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="73e19-128">MOF</span><span class="sxs-lookup"><span data-stu-id="73e19-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73e19-129"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73e19-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="73e19-130">DLL</span><span class="sxs-lookup"><span data-stu-id="73e19-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73e19-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73e19-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="73e19-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73e19-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e19-133">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="73e19-133">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





