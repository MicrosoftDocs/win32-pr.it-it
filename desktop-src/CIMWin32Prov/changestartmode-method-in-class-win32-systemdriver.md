---
description: Modifica la modalità di avvio di un \_ servizio Win32 SystemDriver.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Metodo ChangeStartMode della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523497"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="719cf-103">Metodo ChangeStartMode della \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="719cf-103">ChangeStartMode method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="719cf-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica la modalità di avvio di un servizio [**\_ SystemDriver Win32**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="719cf-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span>

<span data-ttu-id="719cf-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="719cf-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="719cf-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="719cf-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="719cf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="719cf-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="719cf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="719cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="719cf-109">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="719cf-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719cf-110">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="719cf-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="719cf-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Avvio **avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="719cf-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="719cf-112">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="719cf-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="719cf-113">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="719cf-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="719cf-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="719cf-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="719cf-115">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="719cf-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="719cf-116">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="719cf-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="719cf-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="719cf-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="719cf-118">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="719cf-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="719cf-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="719cf-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="719cf-120">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="719cf-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="719cf-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="719cf-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="719cf-122">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="719cf-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="719cf-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="719cf-123">Return value</span></span>

<span data-ttu-id="719cf-124">Restituisce un valore pari a 0 (zero) se il servizio è stato modificato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="719cf-124">Returns a value of 0 (zero) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="719cf-125">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="719cf-125">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-126">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="719cf-126">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-127">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="719cf-127">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-128">**Servizi dipendenti in esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="719cf-128">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-129">**Controllo del servizio non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="719cf-129">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-130">Il **servizio non può accettare il controllo** (5)</span><span class="sxs-lookup"><span data-stu-id="719cf-130">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-131">**Servizio non attivo** (6)</span><span class="sxs-lookup"><span data-stu-id="719cf-131">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-132">**Timeout richiesta di servizio** (7)</span><span class="sxs-lookup"><span data-stu-id="719cf-132">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-133">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="719cf-133">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-134">**Percorso non trovato** (9)</span><span class="sxs-lookup"><span data-stu-id="719cf-134">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-135">**Servizio già in esecuzione** (10)</span><span class="sxs-lookup"><span data-stu-id="719cf-135">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-136">**Database del servizio bloccato** (11)</span><span class="sxs-lookup"><span data-stu-id="719cf-136">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-137">**Dipendenza servizio eliminata** (12)</span><span class="sxs-lookup"><span data-stu-id="719cf-137">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-138">**Errore di dipendenza del servizio** (13)</span><span class="sxs-lookup"><span data-stu-id="719cf-138">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-139">**Servizio disabilitato** (14)</span><span class="sxs-lookup"><span data-stu-id="719cf-139">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-140">**Accesso al servizio non riuscito** (15)</span><span class="sxs-lookup"><span data-stu-id="719cf-140">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-141">**Servizio contrassegnato per l'eliminazione** (16)</span><span class="sxs-lookup"><span data-stu-id="719cf-141">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-142">**Servizio senza thread** (17)</span><span class="sxs-lookup"><span data-stu-id="719cf-142">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-143">**Stato dipendenza circolare** (18)</span><span class="sxs-lookup"><span data-stu-id="719cf-143">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-144">**Stato nome duplicato** (19)</span><span class="sxs-lookup"><span data-stu-id="719cf-144">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-145">**Stato nome non valido** (20)</span><span class="sxs-lookup"><span data-stu-id="719cf-145">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-146">**Stato parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="719cf-146">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-147">**Stato account del servizio non valido** (22)</span><span class="sxs-lookup"><span data-stu-id="719cf-147">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-148">Il **servizio di stato esiste** (23)</span><span class="sxs-lookup"><span data-stu-id="719cf-148">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-149">**Servizio già sospeso** (24)</span><span class="sxs-lookup"><span data-stu-id="719cf-149">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="719cf-150">**Altro** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="719cf-150">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="719cf-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="719cf-151">Requirements</span></span>



| <span data-ttu-id="719cf-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="719cf-152">Requirement</span></span> | <span data-ttu-id="719cf-153">Valore</span><span class="sxs-lookup"><span data-stu-id="719cf-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="719cf-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="719cf-154">Minimum supported client</span></span><br/> | <span data-ttu-id="719cf-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="719cf-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="719cf-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="719cf-156">Minimum supported server</span></span><br/> | <span data-ttu-id="719cf-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="719cf-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="719cf-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="719cf-158">Namespace</span></span><br/>                | <span data-ttu-id="719cf-159">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="719cf-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="719cf-160">MOF</span><span class="sxs-lookup"><span data-stu-id="719cf-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="719cf-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="719cf-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="719cf-162">DLL</span><span class="sxs-lookup"><span data-stu-id="719cf-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="719cf-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="719cf-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="719cf-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="719cf-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="719cf-165">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="719cf-165">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="719cf-166">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="719cf-166">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

