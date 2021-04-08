---
description: Avvia il debugger attualmente registrato per questo processo.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Metodo AttachDebugger della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877413"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a><span data-ttu-id="96800-103">Metodo AttachDebugger della classe di \_ processo Win32</span><span class="sxs-lookup"><span data-stu-id="96800-103">AttachDebugger method of the Win32\_Process class</span></span>

<span data-ttu-id="96800-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** avvia il debugger attualmente registrato per questo processo.</span><span class="sxs-lookup"><span data-stu-id="96800-104">The **AttachDebugger** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method starts the debugger that is currently registered for this process.</span></span>

<span data-ttu-id="96800-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="96800-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="96800-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="96800-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="96800-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96800-107">Syntax</span></span>


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a><span data-ttu-id="96800-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96800-108">Parameters</span></span>

<span data-ttu-id="96800-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="96800-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96800-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96800-110">Return value</span></span>

<span data-ttu-id="96800-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="96800-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="96800-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="96800-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="96800-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="96800-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="96800-114">**Operazione completata**</span><span class="sxs-lookup"><span data-stu-id="96800-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="96800-115">0</span><span class="sxs-lookup"><span data-stu-id="96800-115">0</span></span>

<span data-ttu-id="96800-116">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="96800-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="96800-117">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="96800-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="96800-118">2</span><span class="sxs-lookup"><span data-stu-id="96800-118">2</span></span>

<span data-ttu-id="96800-119">L'utente non ha accesso alle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="96800-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="96800-120">**Privilegio insufficiente**</span><span class="sxs-lookup"><span data-stu-id="96800-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="96800-121">3</span><span class="sxs-lookup"><span data-stu-id="96800-121">3</span></span>

<span data-ttu-id="96800-122">L'utente non dispone di privilegi sufficienti.</span><span class="sxs-lookup"><span data-stu-id="96800-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="96800-123">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="96800-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="96800-124">8</span><span class="sxs-lookup"><span data-stu-id="96800-124">8</span></span>

<span data-ttu-id="96800-125">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="96800-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="96800-126">**Impossibile trovare il percorso**</span><span class="sxs-lookup"><span data-stu-id="96800-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="96800-127">9</span><span class="sxs-lookup"><span data-stu-id="96800-127">9</span></span>

<span data-ttu-id="96800-128">Il percorso specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="96800-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="96800-129">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="96800-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="96800-130">21</span><span class="sxs-lookup"><span data-stu-id="96800-130">21</span></span>

<span data-ttu-id="96800-131">Il parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="96800-131">The specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="96800-132">**Altri**</span><span class="sxs-lookup"><span data-stu-id="96800-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="96800-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="96800-133">22 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96800-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96800-134">Requirements</span></span>



| <span data-ttu-id="96800-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="96800-135">Requirement</span></span> | <span data-ttu-id="96800-136">Valore</span><span class="sxs-lookup"><span data-stu-id="96800-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96800-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96800-137">Minimum supported client</span></span><br/> | <span data-ttu-id="96800-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96800-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96800-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96800-139">Minimum supported server</span></span><br/> | <span data-ttu-id="96800-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96800-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96800-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="96800-141">Namespace</span></span><br/>                | <span data-ttu-id="96800-142">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="96800-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="96800-143">MOF</span><span class="sxs-lookup"><span data-stu-id="96800-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96800-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96800-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="96800-145">DLL</span><span class="sxs-lookup"><span data-stu-id="96800-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96800-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96800-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96800-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96800-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="96800-148">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="96800-148">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="96800-149">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="96800-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

