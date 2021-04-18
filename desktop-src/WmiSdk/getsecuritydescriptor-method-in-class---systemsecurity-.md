---
description: Ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi. Il descrittore di sicurezza viene restituito come un'istanza di \_ \_ securityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Metodo GetSecurityDescriptor della classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315224"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="ac638-104">Metodo GetSecurityDescriptor della \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="ac638-104">GetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="ac638-105">Il metodo **GetSecurityDescriptor** ottiene il descrittore di sicurezza che controlla l'accesso allo spazio dei nomi WMI a cui si è connessi.</span><span class="sxs-lookup"><span data-stu-id="ac638-105">The **GetSecurityDescriptor** method gets the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="ac638-106">Il descrittore di sicurezza viene restituito come un'istanza di [**\_ \_ securityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="ac638-106">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="ac638-107">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ac638-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac638-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac638-108">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="ac638-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac638-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac638-110">*Descrittore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac638-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac638-111">Descrittore di sicurezza associato allo spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="ac638-111">The security descriptor associated with the WMI namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac638-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac638-112">Return value</span></span>

<span data-ttu-id="ac638-113">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="ac638-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="ac638-114">Per ulteriori informazioni, vedere [codici restituiti WMI](wmi-return-codes.md) o [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ac638-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="ac638-115">**0**</span><span class="sxs-lookup"><span data-stu-id="ac638-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ac638-116">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="ac638-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-117">**2**</span><span class="sxs-lookup"><span data-stu-id="ac638-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ac638-118">L'utente non ha accesso alle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="ac638-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-119">**8**</span><span class="sxs-lookup"><span data-stu-id="ac638-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ac638-120">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ac638-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-121">**9**</span><span class="sxs-lookup"><span data-stu-id="ac638-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ac638-122">L'utente non dispone di privilegi sufficienti per eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="ac638-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="ac638-123">**21**</span><span class="sxs-lookup"><span data-stu-id="ac638-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ac638-124">Un parametro specificato nella chiamata al metodo non è valido.</span><span class="sxs-lookup"><span data-stu-id="ac638-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac638-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac638-125">Remarks</span></span>

<span data-ttu-id="ac638-126">L' [**istanza Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) rappresenta un tipo di dati di [**\_ \_ controllo del descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) e contiene un elenco di controllo di [*accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) e un elenco di controllo di accesso di [*sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="ac638-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="ac638-127">Per altre informazioni, vedere [elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="ac638-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="ac638-128">Se **SeSecurityPrivilege** non viene concesso o abilitato quando si recupera un descrittore di sicurezza, nel descrittore di sicurezza restituito viene restituito solo l'elenco DACL.</span><span class="sxs-lookup"><span data-stu-id="ac638-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="ac638-129">Per altre informazioni, vedere [**costanti Privilege**](privilege-constants.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ac638-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac638-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac638-130">Requirements</span></span>



| <span data-ttu-id="ac638-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac638-131">Requirement</span></span> | <span data-ttu-id="ac638-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ac638-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ac638-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac638-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ac638-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac638-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ac638-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac638-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ac638-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac638-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ac638-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac638-137">Namespace</span></span><br/>                | <span data-ttu-id="ac638-138">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="ac638-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ac638-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac638-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac638-140">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="ac638-140">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="ac638-141">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac638-141">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

