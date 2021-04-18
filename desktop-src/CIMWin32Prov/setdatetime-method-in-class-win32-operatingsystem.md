---
description: Valore DateTime&\# 8194; Il metodo della classe WMI imposta l'ora di sistema corrente nel computer.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Metodo sedatetime della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304513"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="bf406-103">Metodo sedatetime della classe Win32 \_ OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bf406-103">SetDateTime method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="bf406-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DateTime** imposta l'ora di sistema corrente nel computer.</span><span class="sxs-lookup"><span data-stu-id="bf406-104">The **SetDateTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the current system time on the computer.</span></span>

<span data-ttu-id="bf406-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="bf406-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bf406-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bf406-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf406-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf406-107">Syntax</span></span>


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a><span data-ttu-id="bf406-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf406-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf406-109">*LocalDatetime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf406-109">*LocalDatetime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf406-110">Valore dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="bf406-110">Value of the current time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf406-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf406-111">Return value</span></span>

<span data-ttu-id="bf406-112">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bf406-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="bf406-113">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="bf406-113">Any other number indicates an error.</span></span> <span data-ttu-id="bf406-114">Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bf406-114">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bf406-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="bf406-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bf406-116">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="bf406-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf406-117">**Altro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="bf406-117">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bf406-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf406-118">Remarks</span></span>

<span data-ttu-id="bf406-119">Il processo chiamante deve avere il \_ privilegio di \_ nome SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="bf406-119">The calling process must have the SE\_SYSTEMTIME\_NAME privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf406-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf406-120">Requirements</span></span>



| <span data-ttu-id="bf406-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf406-121">Requirement</span></span> | <span data-ttu-id="bf406-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bf406-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf406-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf406-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bf406-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf406-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf406-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf406-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bf406-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf406-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf406-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bf406-127">Namespace</span></span><br/>                | <span data-ttu-id="bf406-128">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bf406-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bf406-129">MOF</span><span class="sxs-lookup"><span data-stu-id="bf406-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf406-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf406-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf406-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bf406-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf406-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf406-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf406-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf406-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="bf406-134">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bf406-134">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bf406-135">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="bf406-135">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="bf406-136">Attività WMI: gestione desktop</span><span class="sxs-lookup"><span data-stu-id="bf406-136">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

