---
description: Ottiene il descrittore di sicurezza che controlla chi può accedere a un'applicazione DCOM.
ms.assetid: 5ddd563b-f731-47ac-8a13-20940adfa86d
ms.tgt_platform: multiple
title: Metodo GetAccessSecurityDescriptor della classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e8d87150582a425d23988f70f88ea36bc356476a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304690"
---
# <a name="getaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="735a4-103">Metodo GetAccessSecurityDescriptor della \_ classe DCOMApplicationSetting Win32</span><span class="sxs-lookup"><span data-stu-id="735a4-103">GetAccessSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="735a4-104">Il metodo WMI **GetAccessSecurityDescriptor** ottiene il descrittore di sicurezza che controlla chi può accedere a un'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="735a4-104">The **GetAccessSecurityDescriptor** WMI method gets the security descriptor that controls who can access a DCOM application.</span></span> <span data-ttu-id="735a4-105">Il descrittore di sicurezza è un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="735a4-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="735a4-106">L'account che esegue lo script o l'applicazione che chiama questo metodo deve avere il privilegio **SeSecurityPrivilege** e **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="735a4-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privilege.</span></span> <span data-ttu-id="735a4-107">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="735a4-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="735a4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="735a4-108">Syntax</span></span>


```mof
uint32 GetAccessSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="735a4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="735a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="735a4-110">*Descrittore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="735a4-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="735a4-111">Descrittore di sicurezza da impostare per l'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="735a4-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="735a4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="735a4-112">Return value</span></span>

<span data-ttu-id="735a4-113">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="735a4-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="735a4-114">Per ulteriori informazioni, vedere [codici restituiti WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="735a4-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="735a4-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="735a4-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="735a4-116">0</span><span class="sxs-lookup"><span data-stu-id="735a4-116">0</span></span>

<span data-ttu-id="735a4-117">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="735a4-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="735a4-118">**2**</span><span class="sxs-lookup"><span data-stu-id="735a4-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="735a4-119">L'utente non ha accesso alle informazioni richieste</span><span class="sxs-lookup"><span data-stu-id="735a4-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="735a4-120">**8**</span><span class="sxs-lookup"><span data-stu-id="735a4-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="735a4-121">Errore sconosciuto</span><span class="sxs-lookup"><span data-stu-id="735a4-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="735a4-122">**9**</span><span class="sxs-lookup"><span data-stu-id="735a4-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="735a4-123">L'utente non dispone di privilegi sufficienti per eseguire il metodo</span><span class="sxs-lookup"><span data-stu-id="735a4-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="735a4-124">**21**</span><span class="sxs-lookup"><span data-stu-id="735a4-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="735a4-125">Un parametro specificato nella chiamata al metodo non è valido</span><span class="sxs-lookup"><span data-stu-id="735a4-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="735a4-126">**Altri**</span><span class="sxs-lookup"><span data-stu-id="735a4-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="735a4-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="735a4-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="735a4-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="735a4-128">Remarks</span></span>

<span data-ttu-id="735a4-129">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="735a4-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="735a4-130">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="735a4-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="735a4-131">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="735a4-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="735a4-132">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="735a4-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="735a4-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="735a4-133">Requirements</span></span>



| <span data-ttu-id="735a4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="735a4-134">Requirement</span></span> | <span data-ttu-id="735a4-135">Valore</span><span class="sxs-lookup"><span data-stu-id="735a4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="735a4-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="735a4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="735a4-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="735a4-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="735a4-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="735a4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="735a4-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="735a4-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="735a4-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="735a4-140">Namespace</span></span><br/>                | <span data-ttu-id="735a4-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="735a4-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="735a4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="735a4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="735a4-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="735a4-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="735a4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="735a4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="735a4-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="735a4-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="735a4-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="735a4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735a4-147">**\_DCOMApplicationSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="735a4-147">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="735a4-148">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="735a4-148">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="735a4-149">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="735a4-149">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="735a4-150">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="735a4-150">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

