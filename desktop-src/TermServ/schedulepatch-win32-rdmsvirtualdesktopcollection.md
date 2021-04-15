---
title: Metodo SchedulePatch della classe Win32_RDMSVirtualDesktopCollection
description: Pianifica un processo di provisioning degli aggiornamenti software che installa gli aggiornamenti software nelle macchine virtuali in un insieme di desktop virtuali.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SchedulePatch
- Metodo SchedulePatch Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo SchedulePatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476421"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="a233a-106">Metodo SchedulePatch della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="a233a-106">SchedulePatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="a233a-107">Pianifica un processo di provisioning degli aggiornamenti software che installa gli aggiornamenti software nelle macchine virtuali in un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="a233a-107">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a233a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a233a-108">Syntax</span></span>


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a><span data-ttu-id="a233a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a233a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a233a-110">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a233a-110">*StartTime* \[in\]</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="a233a-111">Il sistema non disconnette gli utenti delle macchine virtuali fino al momento specificato nel parametro *ForceLogOffTime* .</span><span class="sxs-lookup"><span data-stu-id="a233a-111">The system will not log off users of the virtual machines until the time specified in the *ForceLogOffTime* parameter.</span></span>

 

<span data-ttu-id="a233a-112">Data e ora in cui installare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="a233a-112">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="a233a-113">*ForceLogOffTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a233a-113">*ForceLogOffTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a233a-114">Data e ora in cui il sistema disconnetterà gli utenti delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="a233a-114">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="a233a-115">*JobInputXml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a233a-115">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a233a-116">Stringa in formato XML che contiene le informazioni sul processo di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="a233a-116">An XML formatted string that contains the software update job information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a233a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a233a-117">Return value</span></span>

<span data-ttu-id="a233a-118">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="a233a-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a233a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a233a-119">Requirements</span></span>



| <span data-ttu-id="a233a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a233a-120">Requirement</span></span> | <span data-ttu-id="a233a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a233a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a233a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a233a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a233a-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a233a-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a233a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a233a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a233a-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a233a-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a233a-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a233a-126">Namespace</span></span><br/>                | <span data-ttu-id="a233a-127">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="a233a-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a233a-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a233a-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a233a-129"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a233a-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a233a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a233a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a233a-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a233a-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a233a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a233a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a233a-133">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="a233a-133">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





