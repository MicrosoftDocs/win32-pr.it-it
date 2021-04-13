---
description: La proprietà Privileges è un oggetto SWbemPrivilegeSet. Questa proprietà viene utilizzata per abilitare o disabilitare i privilegi di Windows specifici. Potrebbe essere necessario impostare uno di questi privilegi per eseguire attività specifiche mediante l'API Strumentazione gestione Windows (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Proprietà SWbemSecurity. Privileges (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226803"
---
# <a name="swbemsecurityprivileges-property"></a><span data-ttu-id="657a6-105">Proprietà SWbemSecurity. Privileges</span><span class="sxs-lookup"><span data-stu-id="657a6-105">SWbemSecurity.Privileges property</span></span>

<span data-ttu-id="657a6-106">La proprietà **Privileges** è un oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="657a6-106">The **Privileges** property is an [**SWbemPrivilegeSet**](swbemprivilegeset.md) object.</span></span> <span data-ttu-id="657a6-107">Questa proprietà viene utilizzata per abilitare o disabilitare i privilegi di Windows specifici.</span><span class="sxs-lookup"><span data-stu-id="657a6-107">This property is used to enable or disable specific Windows privileges.</span></span> <span data-ttu-id="657a6-108">Potrebbe essere necessario impostare uno di questi privilegi per eseguire attività specifiche mediante l'API Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="657a6-108">You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.</span></span>

<span data-ttu-id="657a6-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="657a6-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="657a6-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="657a6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="657a6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="657a6-111">Syntax</span></span>


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a><span data-ttu-id="657a6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="657a6-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="657a6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="657a6-113">Remarks</span></span>

<span data-ttu-id="657a6-114">Questa impostazione consente di concedere o revocare i privilegi come parte di una stringa del moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="657a6-114">This setting allows you to grant or revoke privileges as part of a WMI moniker string.</span></span> <span data-ttu-id="657a6-115">Per l'elenco completo dei valori applicabili, vedere [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="657a6-115">For the complete list of applicable values, see [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="657a6-116">È possibile modificare i privilegi definiti per gli oggetti [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) aggiungendo oggetti [**SWbemPrivilege**](swbemprivilege.md) alla proprietà **Privileges** .</span><span class="sxs-lookup"><span data-stu-id="657a6-116">You can change the privileges defined for the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by adding [**SWbemPrivilege**](swbemprivilege.md) objects to the **Privileges** property.</span></span>

<span data-ttu-id="657a6-117">Esistono differenze fondamentali nel modo in cui le diverse versioni di Windows gestiscono le modifiche ai privilegi.</span><span class="sxs-lookup"><span data-stu-id="657a6-117">There are fundamental differences in how different versions of Windows handle changes to privileges.</span></span> <span data-ttu-id="657a6-118">Se si sviluppa un'applicazione che viene usata solo nelle piattaforme Windows, è possibile impostare o revocare i privilegi in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="657a6-118">If you are developing an application that is only used on Windows platforms, you can set or revoke privileges at any time.</span></span>

<span data-ttu-id="657a6-119">Nell'esempio seguente viene impostato **SeDebugPrivilege** sulla connessione iniziale del moniker per ottenere un oggetto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="657a6-119">The following example sets the **SeDebugPrivilege** on the initial moniker connection to obtain an [**SWbemServices**](swbemservices.md) object.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



<span data-ttu-id="657a6-120">Per altre informazioni su come formattare la stringa di sicurezza per una connessione moniker, vedere [**costanti Privilege**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="657a6-120">For more information about how to format the security string for a moniker connection, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="657a6-121">Nell'esempio seguente viene eseguita la stessa attività, ma viene impostato il privilegio dopo l'accesso iniziale a WMI.</span><span class="sxs-lookup"><span data-stu-id="657a6-121">The following example performs the same task, but it sets the privilege after the initial log on to WMI.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



<span data-ttu-id="657a6-122">Si noti che per le chiamate a [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md), è necessario usare il nome completo del privilegio di sicurezza, ad esempio, "SeDebugPrivilege" invece di "debug".</span><span class="sxs-lookup"><span data-stu-id="657a6-122">Note that for calls to [**SwbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md), you must use the full name of the security privilege, for example, "SeDebugPrivilege" instead of "Debug".</span></span>

## <a name="requirements"></a><span data-ttu-id="657a6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="657a6-123">Requirements</span></span>



| <span data-ttu-id="657a6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="657a6-124">Requirement</span></span> | <span data-ttu-id="657a6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="657a6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="657a6-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="657a6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="657a6-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="657a6-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="657a6-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="657a6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="657a6-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="657a6-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="657a6-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="657a6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="657a6-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="657a6-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="657a6-132">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="657a6-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="657a6-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="657a6-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="657a6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="657a6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="657a6-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="657a6-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="657a6-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="657a6-136">CLSID</span></span><br/>                    | <span data-ttu-id="657a6-137">\_SWBEMSECURITY CLSID</span><span class="sxs-lookup"><span data-stu-id="657a6-137">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="657a6-138">IID</span><span class="sxs-lookup"><span data-stu-id="657a6-138">IID</span></span><br/>                      | <span data-ttu-id="657a6-139">\_ISWBEMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="657a6-139">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="657a6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="657a6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657a6-141">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="657a6-141">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="657a6-142">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="657a6-142">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="657a6-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="657a6-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> </dl>

 

 




