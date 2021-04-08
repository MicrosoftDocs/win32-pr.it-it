---
description: Ottiene il descrittore di sicurezza che controlla gli utenti autorizzati a configurare un'applicazione DCOM.
ms.assetid: 2858a7a0-1e5b-47aa-9967-0f578c3c22c1
ms.tgt_platform: multiple
title: Metodo GetConfigurationSecurityDescriptor della classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 320af05b352641c812c51353c2e7bda0da046bb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748130"
---
# <a name="getconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="45994-103">Metodo GetConfigurationSecurityDescriptor della \_ classe DCOMApplicationSetting Win32</span><span class="sxs-lookup"><span data-stu-id="45994-103">GetConfigurationSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="45994-104">Il metodo WMI **GetConfigurationSecurityDescriptor** ottiene il descrittore di sicurezza che controlla gli utenti autorizzati a configurare un'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="45994-104">The **GetConfigurationSecurityDescriptor** WMI method gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span> <span data-ttu-id="45994-105">Il descrittore di sicurezza è un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="45994-105">The security descriptor is a instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="45994-106">L'account che esegue lo script o l'applicazione che chiama questo metodo deve avere i privilegi **SeSecurityPrivilege** e **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="45994-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="45994-107">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="45994-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="45994-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45994-108">Syntax</span></span>


```mof
uint32 GetConfigurationSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="45994-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="45994-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45994-110">*Descrittore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="45994-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45994-111">Descrittore di sicurezza da impostare per l'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="45994-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45994-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45994-112">Return value</span></span>

<span data-ttu-id="45994-113">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="45994-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="45994-114">Per ulteriori informazioni, vedere [codici restituiti WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="45994-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="45994-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="45994-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="45994-116">0</span><span class="sxs-lookup"><span data-stu-id="45994-116">0</span></span>

<span data-ttu-id="45994-117">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="45994-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="45994-118">**2**</span><span class="sxs-lookup"><span data-stu-id="45994-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="45994-119">L'utente non ha accesso alle informazioni richieste</span><span class="sxs-lookup"><span data-stu-id="45994-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="45994-120">**8**</span><span class="sxs-lookup"><span data-stu-id="45994-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="45994-121">Errore sconosciuto</span><span class="sxs-lookup"><span data-stu-id="45994-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="45994-122">**9**</span><span class="sxs-lookup"><span data-stu-id="45994-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="45994-123">L'utente non dispone di privilegi sufficienti per eseguire il metodo</span><span class="sxs-lookup"><span data-stu-id="45994-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="45994-124">**21**</span><span class="sxs-lookup"><span data-stu-id="45994-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="45994-125">Un parametro specificato nella chiamata al metodo non è valido</span><span class="sxs-lookup"><span data-stu-id="45994-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="45994-126">**Altri**</span><span class="sxs-lookup"><span data-stu-id="45994-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="45994-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="45994-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45994-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="45994-128">Remarks</span></span>

<span data-ttu-id="45994-129">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="45994-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="45994-130">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="45994-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="45994-131">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="45994-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="45994-132">Per altre informazioni, vedere [**costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants) ed [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="45994-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="45994-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45994-133">Requirements</span></span>



| <span data-ttu-id="45994-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="45994-134">Requirement</span></span> | <span data-ttu-id="45994-135">Valore</span><span class="sxs-lookup"><span data-stu-id="45994-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45994-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45994-136">Minimum supported client</span></span><br/> | <span data-ttu-id="45994-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45994-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45994-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45994-138">Minimum supported server</span></span><br/> | <span data-ttu-id="45994-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45994-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45994-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45994-140">Namespace</span></span><br/>                | <span data-ttu-id="45994-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="45994-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45994-142">MOF</span><span class="sxs-lookup"><span data-stu-id="45994-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45994-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45994-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45994-144">DLL</span><span class="sxs-lookup"><span data-stu-id="45994-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45994-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45994-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45994-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45994-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45994-147">**\_DCOMApplicationSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="45994-147">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="45994-148">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="45994-148">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="45994-149">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="45994-149">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="45994-150">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="45994-150">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

