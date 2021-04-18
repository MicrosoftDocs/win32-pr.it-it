---
description: GetOwnerSid&\# 8194; Il metodo della classe WMI recupera l'ID di sicurezza (SID) per il proprietario del processo.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Metodo GetOwnerSid della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304683"
---
# <a name="getownersid-method-of-the-win32_process-class"></a><span data-ttu-id="22acd-103">Metodo GetOwnerSid della classe di \_ processo Win32</span><span class="sxs-lookup"><span data-stu-id="22acd-103">GetOwnerSid method of the Win32\_Process class</span></span>

<span data-ttu-id="22acd-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** recupera l'ID di sicurezza (SID) per il proprietario del processo.</span><span class="sxs-lookup"><span data-stu-id="22acd-104">The **GetOwnerSid** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the security identifier (SID) for the owner of this process.</span></span>

<span data-ttu-id="22acd-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="22acd-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="22acd-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="22acd-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="22acd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22acd-107">Syntax</span></span>


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a><span data-ttu-id="22acd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="22acd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22acd-109">*SID* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="22acd-109">*Sid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22acd-110">Restituisce il descrittore dell'identificatore di sicurezza per questo processo.</span><span class="sxs-lookup"><span data-stu-id="22acd-110">Returns the security identifier descriptor for this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22acd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22acd-111">Return value</span></span>

<span data-ttu-id="22acd-112">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="22acd-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="22acd-113">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="22acd-113">Any other number indicates an error.</span></span> <span data-ttu-id="22acd-114">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="22acd-114">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="22acd-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="22acd-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="22acd-116">**Completamento** completato (0)</span><span class="sxs-lookup"><span data-stu-id="22acd-116">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22acd-117">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="22acd-117">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22acd-118">**Privilegio insufficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="22acd-118">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22acd-119">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="22acd-119">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="22acd-120">**Percorso non trovato** (9)</span><span class="sxs-lookup"><span data-stu-id="22acd-120">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="22acd-121">**Parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="22acd-121">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="22acd-122">**Altro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="22acd-122">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="22acd-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="22acd-123">Examples</span></span>

<span data-ttu-id="22acd-124">Nell'esempio di codice [trovare gli utenti connessi in un sistema remoto/s versione 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell viene eseguita una query sui computer remoti per verificare chi ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="22acd-124">The [Find the logged on users on a remote system/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell code example queries remote machines to see who is logged on.</span></span>

## <a name="requirements"></a><span data-ttu-id="22acd-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22acd-125">Requirements</span></span>



| <span data-ttu-id="22acd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="22acd-126">Requirement</span></span> | <span data-ttu-id="22acd-127">Valore</span><span class="sxs-lookup"><span data-stu-id="22acd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22acd-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22acd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="22acd-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22acd-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22acd-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22acd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="22acd-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22acd-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22acd-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="22acd-132">Namespace</span></span><br/>                | <span data-ttu-id="22acd-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="22acd-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22acd-134">MOF</span><span class="sxs-lookup"><span data-stu-id="22acd-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22acd-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22acd-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22acd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="22acd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22acd-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22acd-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22acd-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22acd-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="22acd-139">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22acd-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22acd-140">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="22acd-140">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

